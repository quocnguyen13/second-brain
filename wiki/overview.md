---
type: overview
status: verified
sources: ["[[raw/karpathy-llm-wiki.md]]", "[[raw/bush-as-we-may-think.pdf]]"]
created: "2026-09-22"
updated: "2026-09-22"
tags: ["compiled-wiki", "knowledge-management", "memex"]
---
# Overview

The current picture across every source, on one page. Rewritten at each ingest, not appended to.

## The picture so far
- [[wiki/sources/Source - LLM Wiki]] describes the compiled-wiki pattern this vault implements: three layers (raw sources, wiki, schema) and three operations (ingest, query, lint), navigated with an index and a log ([[raw/karpathy-llm-wiki.md]]).
- [[wiki/sources/Source - As We May Think]], writing in 1945, argues that conventional one-path indexing can't keep up with a growing record, and proposes the [[wiki/concepts/Memex]]: a personal device built on [[wiki/concepts/Associative indexing]], where any two items can be permanently linked and the resulting trails replayed, branched, annotated, and shared ([[raw/bush-as-we-may-think.pdf]]).

## Where sources agree
- [[wiki/sources/Source - LLM Wiki]] names [[wiki/sources/Source - As We May Think]]'s [[wiki/concepts/Memex]] as the compiled-wiki pattern's forerunner: both describe a personal, curated store where the connections between documents matter as much as the documents themselves, and the gist casts the LLM as solving the one problem Bush's 1945 proposal left unsolved — who does the upkeep ([[raw/karpathy-llm-wiki.md]]). Bush's own proposal instead has people build the trails, even anticipating a profession of "trail blazers" ([[raw/bush-as-we-may-think.pdf#page=17]]). See the drafts in `mine/drafts/` for this connection worked out in more detail.

## Where sources disagree
- None found.

## Gaps worth a new source
- No source yet tracing the line between Bush's memex and modern hypertext/wiki systems directly (e.g. Engelbart, Nelson's Xanadu, or the history of the wiki format) — would let a claim about that lineage carry a citation instead of resting on general knowledge.
- No source yet on how well the compiled-wiki pattern holds up in practice at scale (carried over from the first ingest).
- No independent source on alternatives to compiled-wiki (embedding-based RAG, etc.) (carried over).

## Sources so far
- [[wiki/sources/Source - LLM Wiki]] — Karpathy's gist proposing the compiled-wiki pattern.
- [[wiki/sources/Source - As We May Think]] — Bush's 1945 essay proposing the memex and associative indexing.
