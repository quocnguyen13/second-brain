---
type: concept
status: contested
sources: ["[[raw/anthropic-contextual-retrieval.md]]", "[[raw/karpathy-llm-wiki.md]]"]
created: "2026-09-22"
updated: "2026-09-22"
tags: ["information-retrieval"]
---
# Retrieval-augmented generation

RAG: retrieving relevant pieces of a knowledge base at query time and adding them to the model's prompt ([[raw/anthropic-contextual-retrieval.md]]).

## What the sources say
- Standard pipeline: split the corpus into chunks of "usually no more than a few hundred tokens", embed them, store them in a vector database; at query time find the chunks most similar to the query and add them to the prompt ([[raw/anthropic-contextual-retrieval.md]]).
- Hybrid RAG adds [[wiki/concepts/BM25]] for exact matches alongside embeddings, merges and deduplicates the two result lists with rank fusion, and passes the top-K chunks ([[raw/anthropic-contextual-retrieval.md]]).
- Anthropic presents RAG as "the typical solution" once a knowledge base no longer fits in the context window, able to "cost-effectively scale to enormous knowledge bases" ([[raw/anthropic-contextual-retrieval.md]]).
- Below 200,000 tokens ("about 500 pages") Anthropic says to skip RAG and put the whole knowledge base in the prompt, with [[wiki/concepts/Prompt caching]] ([[raw/anthropic-contextual-retrieval.md]]).
- Its main weakness, per Anthropic: chunking "often destroy[s] context", so a chunk can't be matched or used without knowing its document ([[raw/anthropic-contextual-retrieval.md]]). [[wiki/concepts/Contextual Retrieval]] and [[wiki/concepts/Reranking]] are the proposed fixes.
- Karpathy describes RAG as the common way LLMs meet documents (NotebookLM, ChatGPT file uploads) and says it "works", but "the LLM is rediscovering knowledge from scratch on every question" ([[raw/karpathy-llm-wiki.md]]).
- Karpathy says an index-first [[wiki/concepts/Compiled wiki]] avoids "the need for embedding-based RAG infrastructure" at moderate scale (~100 sources, ~hundreds of pages) ([[raw/karpathy-llm-wiki.md]]).

## Where sources disagree
- **Does RAG accumulate anything?**
  - Karpathy: "There's no accumulation … Nothing is built up"; each question re-finds and re-assembles fragments ([[raw/karpathy-llm-wiki.md]]).
  - Anthropic: with [[wiki/concepts/Contextual Retrieval]], an LLM reads each chunk against its whole document once, at preprocessing, and the resulting context is prepended to the chunk before embedding and before building the BM25 index ([[raw/anthropic-contextual-retrieval.md]]). Retrieval then runs over this ingest-time LLM output.
  - Separately, the post prices that step as a "one-time cost" of $1.02 per million document tokens, under its stated assumptions ([[raw/anthropic-contextual-retrieval.md]]).
  - Scope: Anthropic's stored work is per-chunk, within one document; Karpathy's "accumulation" means cross-document synthesis, contradictions and cross-references, which Anthropic's method does not produce ([[raw/karpathy-llm-wiki.md]], [[raw/anthropic-contextual-retrieval.md]]). Neither source addresses the other.
- **Is RAG the thing to replace or the thing to improve?** Karpathy positions the compiled wiki as the alternative to RAG ([[raw/karpathy-llm-wiki.md]]). Anthropic treats RAG as the default at scale and rejects summary-based alternatives it tested: generic document summaries on chunks ("very limited gains") and summary-based indexing ("low performance") ([[raw/anthropic-contextual-retrieval.md]]). Those are not compiled wikis, so this is a difference in framing, not a head-to-head result.

## Mentioned in
- [[wiki/sources/Source - Contextual Retrieval]]
- [[wiki/sources/Source - LLM Wiki]]

## Related
- [[wiki/concepts/Compiled wiki]]
- [[wiki/concepts/Contextual Retrieval]]
- [[wiki/concepts/BM25]]
- [[wiki/concepts/Reranking]]
- [[wiki/concepts/Prompt caching]]
