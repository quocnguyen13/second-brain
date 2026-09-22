---
type: concept
status: verified
sources: ["[[raw/karpathy-llm-wiki.md]]"]
created: "2026-09-22"
updated: "2026-09-22"
tags: ["compiled-wiki"]
---
# Wiki index and log

The two navigation files that keep a compiled wiki usable as it grows: `index.md`, a content catalog, and `log.md`, a chronological record ([[raw/karpathy-llm-wiki.md]]).

## What the sources say
- `index.md` is content-oriented: a catalog of everything in the wiki, each page listed with a link, a one-line summary, and optionally metadata like date or source count, organized by category (entities, concepts, sources, etc.); updated on every ingest ([[raw/karpathy-llm-wiki.md]]).
- When answering a query, the LLM is meant to read the index first to find relevant pages, then drill into them ([[raw/karpathy-llm-wiki.md]]).
- This index-first approach works well at moderate scale (~100 sources, ~hundreds of pages) and avoids needing embedding-based RAG infrastructure ([[raw/karpathy-llm-wiki.md]]).
- `log.md` is chronological: an append-only record of ingests, queries, and lint passes, giving a timeline of the wiki's evolution ([[raw/karpathy-llm-wiki.md]]).
- Keeping a consistent entry prefix (e.g. `## [2026-04-02] ingest | Article Title`) makes the log parseable with simple unix tools, e.g. `grep "^## \[" log.md | tail -5` for the last 5 entries ([[raw/karpathy-llm-wiki.md]]).

## Where sources disagree
- None found.

## Mentioned in
- [[wiki/sources/Source - LLM Wiki]]

## Related
- [[wiki/concepts/Compiled wiki]]
- [[wiki/concepts/Wiki ingest]]
