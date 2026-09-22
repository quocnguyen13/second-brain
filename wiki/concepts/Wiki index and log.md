---
type: concept
status: verified
sources: ["[[raw/karpathy-llm-wiki.md]]", "[[raw/anthropic-contextual-retrieval.md]]"]
created: "2026-09-22"
updated: "2026-09-22"
tags: ["compiled-wiki"]
---
# Wiki index and log

The two navigation files that keep a compiled wiki usable as it grows: `index.md`, a content catalog, and `log.md`, a chronological record ([[raw/karpathy-llm-wiki.md]]).

## What the sources say
- `index.md` is content-oriented: a catalog of everything in the wiki, each page listed with a link, a one-line summary, and optionally metadata like date or source count, organized by category (entities, concepts, sources, etc.); updated on every ingest ([[raw/karpathy-llm-wiki.md]]).
- When answering a query, the LLM is meant to read the index first to find relevant pages, then drill into them ([[raw/karpathy-llm-wiki.md]]).
- This index-first approach works well at moderate scale (~100 sources, ~hundreds of pages) and avoids needing embedding-based [[wiki/concepts/Retrieval-augmented generation]] infrastructure ([[raw/karpathy-llm-wiki.md]]).
- A different small-scale alternative to RAG: Anthropic says a knowledge base under 200,000 tokens ("about 500 pages") can go into the prompt whole, made cheaper by [[wiki/concepts/Prompt caching]] ([[raw/anthropic-contextual-retrieval.md]]). The two thresholds are in different units; neither source compares them.
- When the index is no longer enough, the gist suggests a search tool such as qmd, with "hybrid BM25/vector search and LLM re-ranking" ([[raw/karpathy-llm-wiki.md]]). Anthropic's tests found that same combination ([[wiki/concepts/BM25]] + embeddings + [[wiki/concepts/Reranking]]) the most accurate of the setups it tried ([[raw/anthropic-contextual-retrieval.md]]).
- `log.md` is chronological: an append-only record of ingests, queries, and lint passes, giving a timeline of the wiki's evolution ([[raw/karpathy-llm-wiki.md]]).
- Keeping a consistent entry prefix (e.g. `## [2026-04-02] ingest | Article Title`) makes the log parseable with simple unix tools, e.g. `grep "^## \[" log.md | tail -5` for the last 5 entries ([[raw/karpathy-llm-wiki.md]]).

## Where sources disagree
- None found.

## Mentioned in
- [[wiki/sources/Source - LLM Wiki]]
- [[wiki/sources/Source - Contextual Retrieval]]

## Related
- [[wiki/concepts/Compiled wiki]]
- [[wiki/concepts/Wiki ingest]]
- [[wiki/concepts/Retrieval-augmented generation]]
