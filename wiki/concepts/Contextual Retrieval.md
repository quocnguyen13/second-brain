---
type: concept
status: verified
sources: ["[[raw/anthropic-contextual-retrieval.md]]"]
created: "2026-09-22"
updated: "2026-09-22"
tags: ["information-retrieval"]
---
# Contextual Retrieval

A RAG preprocessing step: an LLM writes a short context situating each chunk within its whole document, and that context is prepended to the chunk before embedding ("Contextual Embeddings") and before building the BM25 index ("Contextual BM25") ([[raw/anthropic-contextual-retrieval.md]]).

## What the sources say
- Problem it targets: a chunk such as "The company's revenue grew by 3% over the previous quarter" doesn't say which company or period; the contextualised version adds "This chunk is from an SEC filing on ACME corp's performance in Q2 2023; the previous quarter's revenue was $314 million" ([[raw/anthropic-contextual-retrieval.md]]).
- The LLM gets the whole document plus one chunk and returns only the context, "usually 50-100 tokens" ([[raw/anthropic-contextual-retrieval.md]]).
- Cost: $1.02 per million document tokens, one-time, assuming prompt caching, 800-token chunks, 8k-token documents, 50-token instructions and 100 tokens of context per chunk ([[raw/anthropic-contextual-retrieval.md]]).
- Accuracy, averaged over four domains (codebases, fiction, ArXiv papers, science papers) with Gemini Text 004 embeddings, top 20 chunks, metric 1 − recall@20 ([[raw/anthropic-contextual-retrieval.md]]):
  - contextual embeddings alone: failure rate 5.7% → 3.7% (−35%);
  - contextual embeddings + contextual BM25: 5.7% → 2.9% (−49%);
  - plus a Cohere reranker (top 150 → top 20): 5.7% → 1.9% (−67%).
- It improved results "in every embedding-source combination we evaluated" ([[raw/anthropic-contextual-retrieval.md]]).
- Tuning levers: chunk size, boundary and overlap; embedding model (Gemini and Voyage best of those tested); domain-specific contextualizer prompts, e.g. with a glossary of terms defined in other documents ([[raw/anthropic-contextual-retrieval.md]]).
- Distinct from earlier methods the authors tried: generic document summaries on chunks gave "very limited gains"; summary-based indexing showed "low performance" ([[raw/anthropic-contextual-retrieval.md]]).

## Where sources disagree
- None found. It bears on the contested question of whether RAG accumulates anything; see [[wiki/concepts/Retrieval-augmented generation]].

## Mentioned in
- [[wiki/sources/Source - Contextual Retrieval]]

## Related
- [[wiki/concepts/Retrieval-augmented generation]]
- [[wiki/concepts/BM25]]
- [[wiki/concepts/Reranking]]
- [[wiki/concepts/Prompt caching]]
- [[wiki/concepts/Compiled wiki]]
- [[wiki/entities/Anthropic]]
