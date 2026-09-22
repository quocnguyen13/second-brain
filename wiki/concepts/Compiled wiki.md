---
type: concept
status: contested
sources: ["[[raw/karpathy-llm-wiki.md]]", "[[raw/anthropic-contextual-retrieval.md]]", "[[raw/forte-para-method.md]]"]
created: "2026-09-22"
updated: "2026-09-22"
tags: ["compiled-wiki", "knowledge-management"]
---
# Compiled wiki

A knowledge base an LLM incrementally builds and maintains, structured in three layers, so that knowledge compounds across sources instead of being re-derived at every query ([[raw/karpathy-llm-wiki.md]]).

## What the sources say
- Contrasts with [[wiki/concepts/Retrieval-augmented generation]]: in plain RAG the LLM retrieves chunks and rediscovers knowledge from scratch on every question; in a compiled wiki, the LLM reads each new source once, integrates it, and the synthesis persists ([[raw/karpathy-llm-wiki.md]]).
- Three layers: **raw sources** (immutable, curated, the source of truth), **the wiki** (LLM-owned markdown — summaries, entity pages, concept pages, an overview/synthesis), and **the schema** (a doc such as `CLAUDE.md` defining structure, conventions, and workflows) ([[raw/karpathy-llm-wiki.md]]).
- The person's role is sourcing, exploration, and asking questions; the LLM's role is the summarizing, cross-referencing, filing, and bookkeeping ([[raw/karpathy-llm-wiki.md]]).
- Works well at moderate scale (~100 sources, ~hundreds of pages) using just an index file, without embedding-based search infrastructure ([[raw/karpathy-llm-wiki.md]]).
- The source frames the idea as related in spirit to [[wiki/entities/Vannevar Bush]]'s [[wiki/concepts/Memex]] (1945) — a personal, curated store with associative trails between documents — noting Bush's unsolved problem was who does the maintenance, which the LLM now handles ([[raw/karpathy-llm-wiki.md]]).

- Anthropic's retrieval post does not mention compiled wikis. The nearest approaches it tested, generic document summaries on chunks and summary-based indexing, gave "very limited gains" and "low performance" for retrieval ([[raw/anthropic-contextual-retrieval.md]]). They are retrieval aids, not compiled wikis.
- For small corpora both sources skip RAG, by different routes: the compiled wiki reads an index at ~100 sources ([[raw/karpathy-llm-wiki.md]]); Anthropic puts the whole knowledge base in the prompt under 200,000 tokens ([[raw/anthropic-contextual-retrieval.md]]).
- **Organised by topic, not by project.**
  - The wiki's pages are "summaries, entity pages, concept pages, comparisons, an overview, a synthesis" ([[raw/karpathy-llm-wiki.md]]).
  - The [[wiki/concepts/PARA method]] puts projects first and keeps topics in a lower-priority "resources" category ([[raw/forte-para-method.md]]).
  - Neither source addresses the other, so this is an open point, not a disagreement. See [[wiki/concepts/Organizing by actionability]].

## Where sources disagree
- **The premise that RAG builds nothing up.**
  - Karpathy: in RAG "the LLM is rediscovering knowledge from scratch on every question. There's no accumulation"; the compiled wiki exists to fix that ([[raw/karpathy-llm-wiki.md]]).
  - Anthropic: in [[wiki/concepts/Contextual Retrieval]], an LLM generates context for each chunk once, at preprocessing, and that context is prepended to the chunk before embedding and before building the BM25 index ([[raw/anthropic-contextual-retrieval.md]]). What gets searched at query time is therefore LLM output produced at ingest: work that persists, which is what Karpathy says RAG lacks.
  - Separately, the post prices that step as a "one-time cost" of $1.02 per million document tokens, under its stated assumptions ([[raw/anthropic-contextual-retrieval.md]]).
  - Scope: what Anthropic stores is per-chunk context within one document; the compiled wiki's accumulation is cross-document synthesis, cross-references and flagged contradictions, which Contextual Retrieval does not produce ([[raw/karpathy-llm-wiki.md]], [[raw/anthropic-contextual-retrieval.md]]). The sources don't address each other.
- **Retrieval as the thing to replace or to improve.** Karpathy offers the compiled wiki as the alternative to RAG ([[raw/karpathy-llm-wiki.md]]); Anthropic calls RAG "the typical solution" at scale and fixes it from within ([[raw/anthropic-contextual-retrieval.md]]). No source in the wiki compares the two on the same corpus.

## Mentioned in
- [[wiki/sources/Source - LLM Wiki]]
- [[wiki/sources/Source - Contextual Retrieval]]
- [[wiki/sources/Source - The PARA Method]]

## Related
- [[wiki/concepts/Wiki ingest]]
- [[wiki/concepts/Wiki query]]
- [[wiki/concepts/Wiki lint]]
- [[wiki/concepts/Wiki index and log]]
- [[wiki/entities/Karpathy]]
- [[wiki/concepts/Memex]]
- [[wiki/concepts/Evergreen notes]]
- [[wiki/concepts/Retrieval-augmented generation]]
- [[wiki/concepts/Contextual Retrieval]]
- [[wiki/concepts/PARA method]]
- [[wiki/concepts/Organizing by actionability]]
