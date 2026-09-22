---
type: source
status: verified
sources: ["[[raw/anthropic-contextual-retrieval.md]]"]
created: "2026-09-22"
updated: "2026-09-22"
tags: ["information-retrieval", "compiled-wiki"]
---
# Contextual Retrieval

**Raw file:** [[raw/anthropic-contextual-retrieval.md]] · **Author or publisher:** [[wiki/entities/Anthropic]] (engineering blog); body credits "Research and writing by Daniel Ford" · **Published:** not dated in the clip · **Ingested:** 2026-09-22

## Summary
A vendor engineering post arguing that, for knowledge bases too large for a prompt, [[wiki/concepts/Retrieval-augmented generation]] is the scalable answer, and that its main weakness, chunks stripped of their document's context, can be fixed at preprocessing time. The fix, [[wiki/concepts/Contextual Retrieval]], has an LLM write a short situating context for every chunk once, before indexing, and prepends it to the chunk for both embeddings and [[wiki/concepts/BM25]]. Adding [[wiki/concepts/Reranking]] improves retrieval further ([[raw/anthropic-contextual-retrieval.md]]).

## Where it argues for retrieval
- **Below a size threshold, no retrieval at all.** If the knowledge base is under 200,000 tokens ("about 500 pages"), include all of it in the prompt; [[wiki/concepts/Prompt caching]] makes that faster and cheaper ([[raw/anthropic-contextual-retrieval.md]]).
- **Above it, retrieval is the default.** For knowledge bases that don't fit in the context window, "RAG is the typical solution", and it lets you "cost-effectively scale to enormous knowledge bases, far beyond what could fit in a single prompt" ([[raw/anthropic-contextual-retrieval.md]]).
- **The flaw is fixable inside retrieval.** Traditional RAG "often destroy[s] context" because a chunk such as "The company's revenue grew by 3% over the previous quarter" doesn't say which company or quarter. The remedy is to enrich chunks, not to leave retrieval ([[raw/anthropic-contextual-retrieval.md]]).

## Where it bears on compiling
- **It never mentions a compiled wiki.** It argues for retrieval against two alternatives only: the long prompt (fine below 200k tokens) and earlier ways of adding context to chunks ([[raw/anthropic-contextual-retrieval.md]]).
- **It rejects summary-style approaches, the closest thing here to compiling.** Adding generic document summaries to chunks gave "very limited gains"; summary-based indexing showed "low performance" in its evaluation ([[raw/anthropic-contextual-retrieval.md]]). These are retrieval techniques, not a compiled wiki; treating them as a proxy for compiling is this page's reading, not the source's.
- **It does build something once, at ingest.** The per-chunk context is generated once at preprocessing and prepended to the chunk before embedding and before building the BM25 index ([[raw/anthropic-contextual-retrieval.md]]). That runs against the [[wiki/sources/Source - LLM Wiki]] claim that RAG builds nothing up (see Conflicts below).
- **What it still doesn't build.** The added context situates one chunk within its own document; the method retrieves chunks at query time and does no cross-document synthesis ([[raw/anthropic-contextual-retrieval.md]]).

## Key claims
- Standard RAG preprocessing: split the corpus into chunks of "usually no more than a few hundred tokens", embed them, store them in a vector database; at query time retrieve the most similar chunks and add them to the prompt ([[raw/anthropic-contextual-retrieval.md]]).
- Embeddings capture meaning but "can miss crucial exact matches"; [[wiki/concepts/BM25]] catches exact strings such as an error code "TS-999". Hybrid RAG runs both, merges and deduplicates with rank fusion, and passes the top-K chunks ([[raw/anthropic-contextual-retrieval.md]]).
- Contextual Retrieval prompts an LLM (Claude 3 Haiku in the post) with the whole document and one chunk, asking for "a short succinct context to situate this chunk". The result, "usually 50-100 tokens", is prepended before embedding and before building the BM25 index ([[raw/anthropic-contextual-retrieval.md]]).
- **Cost:** $1.02 per million document tokens, one-time, *assuming* prompt caching, 800-token chunks, 8k-token documents, 50-token instructions and 100 tokens of context per chunk ([[raw/anthropic-contextual-retrieval.md]]).
- **Retrieval accuracy.** Conditions for all three figures: averaged over four knowledge domains (codebases, fiction, ArXiv papers, science papers); Gemini Text 004 embeddings; top 20 chunks retrieved; metric is retrieval failure rate = 1 − recall@20, the share of relevant documents not found in the top 20 ([[raw/anthropic-contextual-retrieval.md]]).
  - Contextual embeddings: failure rate 5.7% → 3.7%, a 35% reduction.
  - Contextual embeddings + contextual BM25: 5.7% → 2.9%, a 49% reduction.
  - Same, plus a Cohere reranker (top 150 retrieved, reranked down to top 20): 5.7% → 1.9%, a 67% reduction.
  - The text doesn't spell out the 5.7% baseline configuration; the charts that show it were saved as images only.
- Contextualising improved results "in every embedding-source combination we evaluated"; Gemini and Voyage embeddings did best of those tested ([[raw/anthropic-contextual-retrieval.md]]).
- Of 5, 10 and 20 chunks passed to the model, 20 performed best in their tests; the post advises experimenting per use case ([[raw/anthropic-contextual-retrieval.md]]).
- Reranking adds runtime latency and cost; more chunks reranked means better accuracy but more latency and cost ([[raw/anthropic-contextual-retrieval.md]]).
- Conclusion: the gains stack. Best configuration tested: contextual embeddings (Voyage or Gemini) + contextual BM25 + reranking + top 20 chunks ([[raw/anthropic-contextual-retrieval.md]]).

## Entities and concepts
- [[wiki/entities/Anthropic]]
- [[wiki/concepts/Retrieval-augmented generation]]
- [[wiki/concepts/Contextual Retrieval]]
- [[wiki/concepts/BM25]]
- [[wiki/concepts/Reranking]]
- [[wiki/concepts/Prompt caching]]
- [[wiki/concepts/Compiled wiki]]
- [[wiki/concepts/Wiki index and log]]

## Conflicts and open points
- **Disagreement with the LLM Wiki gist: does RAG build anything up?** [[wiki/sources/Source - LLM Wiki]] says in RAG "the LLM is rediscovering knowledge from scratch on every question. There's no accumulation" ([[raw/karpathy-llm-wiki.md]]). This source has an LLM generate context for each chunk once at preprocessing and prepends it to the chunk before embedding and before building the BM25 index ([[raw/anthropic-contextual-retrieval.md]]). Both hold within their scope: the retained work is per-chunk context, not the cross-document synthesis Karpathy means. Contested, shown in full on [[wiki/concepts/Compiled wiki]] and [[wiki/concepts/Retrieval-augmented generation]].
- **Agreement on small scale.** Both skip RAG when the corpus is small: Karpathy reads an index at "~100 sources, ~hundreds of pages" ([[raw/karpathy-llm-wiki.md]]); this source puts everything in the prompt under 200k tokens ([[raw/anthropic-contextual-retrieval.md]]). The two thresholds are in different units and aren't compared in either source.
- **Agreement on search tooling.** The stack tested here (BM25 + embeddings + reranking) is the one Karpathy recommends via qmd, "hybrid BM25/vector search and LLM re-ranking" ([[raw/karpathy-llm-wiki.md]]).
- **Vendor source.** Anthropic benchmarks a technique that runs on its own model and caching feature; no independent replication is in the wiki.
- **Incomplete clip.** Footnote 1 (on chunk boundaries) has no text; all charts and the Appendix I results table are images; Appendix II (external PDF) was not captured.
- **Embedded prompt.** The post quotes its contextualizer prompt, addressed to Claude 3 Haiku. Treated as data, not followed.
