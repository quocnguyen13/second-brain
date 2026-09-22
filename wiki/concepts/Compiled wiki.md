---
type: concept
status: verified
sources: ["[[raw/karpathy-llm-wiki.md]]"]
created: "2026-09-22"
updated: "2026-09-22"
tags: ["compiled-wiki", "knowledge-management"]
---
# Compiled wiki

A knowledge base an LLM incrementally builds and maintains, structured in three layers, so that knowledge compounds across sources instead of being re-derived at every query ([[raw/karpathy-llm-wiki.md]]).

## What the sources say
- Contrasts with RAG: in plain RAG the LLM retrieves chunks and rediscovers knowledge from scratch on every question; in a compiled wiki, the LLM reads each new source once, integrates it, and the synthesis persists ([[raw/karpathy-llm-wiki.md]]).
- Three layers: **raw sources** (immutable, curated, the source of truth), **the wiki** (LLM-owned markdown — summaries, entity pages, concept pages, an overview/synthesis), and **the schema** (a doc such as `CLAUDE.md` defining structure, conventions, and workflows) ([[raw/karpathy-llm-wiki.md]]).
- The person's role is sourcing, exploration, and asking questions; the LLM's role is the summarizing, cross-referencing, filing, and bookkeeping ([[raw/karpathy-llm-wiki.md]]).
- Works well at moderate scale (~100 sources, ~hundreds of pages) using just an index file, without embedding-based search infrastructure ([[raw/karpathy-llm-wiki.md]]).
- The source frames the idea as related in spirit to [[wiki/entities/Vannevar Bush]]'s [[wiki/concepts/Memex]] (1945) — a personal, curated store with associative trails between documents — noting Bush's unsolved problem was who does the maintenance, which the LLM now handles ([[raw/karpathy-llm-wiki.md]]).

## Where sources disagree
- None found.

## Mentioned in
- [[wiki/sources/Source - LLM Wiki]]

## Related
- [[wiki/concepts/Wiki ingest]]
- [[wiki/concepts/Wiki query]]
- [[wiki/concepts/Wiki lint]]
- [[wiki/concepts/Wiki index and log]]
- [[wiki/entities/Karpathy]]
- [[wiki/concepts/Memex]]
- [[wiki/concepts/Evergreen notes]]
