---
type: source
status: verified
sources: ["[[raw/karpathy-llm-wiki.md]]", "[[raw/anthropic-contextual-retrieval.md]]", "[[raw/forte-para-method.md]]"]
created: "2026-09-22"
updated: "2026-09-22"
tags: ["compiled-wiki", "knowledge-management"]
---
# LLM Wiki

**Raw file:** [[raw/karpathy-llm-wiki.md]] · **Author or publisher:** Karpathy (per the gist URL, `github.com/karpathy`) · **Published:** not dated in the clip · **Ingested:** 2026-09-22

## Summary
A GitHub Gist proposing a pattern for personal knowledge bases: instead of [[wiki/concepts/Retrieval-augmented generation|RAG]]-style retrieval that rediscovers knowledge from scratch on every query, an LLM incrementally builds and maintains a persistent, interlinked wiki from a curated collection of raw sources. The wiki compounds over time — cross-references, contradictions, and synthesis accumulate rather than being re-derived ([[raw/karpathy-llm-wiki.md]]).

## Key claims
- Three-layer architecture: **raw sources** (immutable, source of truth), **the wiki** (LLM-owned markdown pages — summaries, entities, concepts, overview), and **the schema** (a doc like `CLAUDE.md` that defines conventions and workflows) ([[raw/karpathy-llm-wiki.md]]).
- Three operations: **Ingest** — process one new source, discuss takeaways, write a summary page, update relevant entity/concept pages and the index, log the change; a single source may touch 10-15 pages. **Query** — search the wiki, synthesize an answer with citations, and file substantial answers back into the wiki as new pages so explorations compound too. **Lint** — periodic health check for contradictions, claims superseded by newer sources, orphan pages, missing cross-references, and concepts mentioned but lacking a page ([[raw/karpathy-llm-wiki.md]]).
- `index.md` is content-oriented: a catalog of every page with a one-line summary, organized by category, read first when answering a query, updated on every ingest ([[raw/karpathy-llm-wiki.md]]).
- `log.md` is chronological and append-only: one entry per ingest/query/lint, with a consistent line prefix (e.g. `## [YYYY-MM-DD] ingest | Title`) so it stays parseable with simple tools ([[raw/karpathy-llm-wiki.md]]).
- The wiki being a git repo gives version history, branching, and collaboration for free ([[raw/karpathy-llm-wiki.md]]).
- The source is explicitly abstract: it describes the pattern, not a fixed implementation — the reader's LLM and the reader are meant to co-develop the actual schema and conventions ([[raw/karpathy-llm-wiki.md]]).

## Entities and concepts
- [[wiki/entities/Karpathy]]
- [[wiki/concepts/Compiled wiki]]
- [[wiki/concepts/Wiki ingest]]
- [[wiki/concepts/Wiki query]]
- [[wiki/concepts/Wiki lint]]
- [[wiki/concepts/Wiki index and log]]
- [[wiki/concepts/Memex]]
- [[wiki/entities/Vannevar Bush]]
- [[wiki/concepts/Retrieval-augmented generation]]
- [[wiki/concepts/BM25]]
- [[wiki/concepts/Reranking]]

## Conflicts and open points
- This is the first source in the wiki, and it is also the design document this vault's own `CLAUDE.md` implements.
- **Disagreement with the Contextual Retrieval post: does RAG build anything up?** This source says in RAG "the LLM is rediscovering knowledge from scratch on every question. There's no accumulation" ([[raw/karpathy-llm-wiki.md]]). [[wiki/sources/Source - Contextual Retrieval]] describes RAG preprocessing where an LLM generates context for each chunk once and prepends it before embedding and before building the BM25 index ([[raw/anthropic-contextual-retrieval.md]]). What persists there is per-chunk context, not cross-document synthesis. Contested; both positions are shown on [[wiki/concepts/Compiled wiki]] and [[wiki/concepts/Retrieval-augmented generation]].
- **Open point with the PARA post: topic pages vs. project folders.**
  - This source organises the wiki into entity and concept pages ([[raw/karpathy-llm-wiki.md]]).
  - [[wiki/sources/Source - The PARA Method]] puts projects first and topics in "resources" ([[raw/forte-para-method.md]]).
  - Neither addresses the other, so this is not contested. See [[wiki/concepts/Organizing by actionability]].
