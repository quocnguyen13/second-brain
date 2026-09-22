---
type: concept
status: verified
sources: ["[[raw/anthropic-contextual-retrieval.md]]", "[[raw/karpathy-llm-wiki.md]]"]
created: "2026-09-22"
updated: "2026-09-22"
tags: ["information-retrieval"]
---
# Reranking

A filtering step after initial retrieval: a reranking model scores each retrieved chunk for relevance to the query, and only the top-scoring chunks go to the generating model ([[raw/anthropic-contextual-retrieval.md]]).

## What the sources say
- Steps as tested by Anthropic: retrieve the top 150 chunks, pass them with the query through a reranker, keep the top 20, send those to the model ([[raw/anthropic-contextual-retrieval.md]]).
- Adding a Cohere reranker to contextual embeddings + contextual BM25 took the retrieval failure rate from 2.9% to 1.9% (baseline 5.7%, overall −67%), averaged over four domains with Gemini Text 004 embeddings and metric 1 − recall@20 ([[raw/anthropic-contextual-retrieval.md]]).
- Trade-off: reranking adds runtime latency and cost even though chunks are scored in parallel; reranking more chunks buys accuracy at more latency and cost ([[raw/anthropic-contextual-retrieval.md]]).
- Voyage also offers a reranker; Anthropic did not test it ([[raw/anthropic-contextual-retrieval.md]]).
- Karpathy's suggested wiki search tool, qmd, includes "LLM re-ranking" ([[raw/karpathy-llm-wiki.md]]).

## Where sources disagree
- None found.

## Mentioned in
- [[wiki/sources/Source - Contextual Retrieval]]
- [[wiki/sources/Source - LLM Wiki]]

## Related
- [[wiki/concepts/Retrieval-augmented generation]]
- [[wiki/concepts/Contextual Retrieval]]
- [[wiki/concepts/BM25]]
