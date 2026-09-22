---
type: overview
status: verified
sources: ["[[raw/karpathy-llm-wiki.md]]"]
created: "2026-09-22"
updated: "2026-09-22"
tags: ["compiled-wiki"]
---
# Overview

The current picture across every source, on one page. Rewritten at each ingest, not appended to.

## The picture so far
- One source so far, [[wiki/sources/Source - LLM Wiki]], which describes the compiled-wiki pattern this vault itself implements: three layers (raw sources, wiki, schema) and three operations (ingest, query, lint), navigated with an index and a log ([[raw/karpathy-llm-wiki.md]]).
- See [[wiki/concepts/Compiled wiki]], [[wiki/concepts/Wiki ingest]], [[wiki/concepts/Wiki query]], [[wiki/concepts/Wiki lint]], and [[wiki/concepts/Wiki index and log]] for the details.

## Where sources agree
- N/A — only one source so far.

## Where sources disagree
- None found.

## Gaps worth a new source
- The pattern is described abstractly by its own proposer; no independent source yet on how well it holds up in practice at scale (the source itself caps its own confidence at "~100 sources, ~hundreds of pages").
- No source yet on alternative or competing approaches (e.g. embedding-based RAG, tools like `qmd`) to compare against.

## Sources so far
- [[wiki/sources/Source - LLM Wiki]] — Karpathy's gist proposing the compiled-wiki pattern.
