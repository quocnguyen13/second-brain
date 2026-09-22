---
type: overview
status: verified
sources: ["[[raw/karpathy-llm-wiki.md]]", "[[raw/bush-as-we-may-think.pdf]]", "[[raw/matuschak-evergreen-notes.md]]"]
created: "2026-09-22"
updated: "2026-09-22"
tags: ["compiled-wiki", "knowledge-management", "memex", "note-taking"]
---
# Overview

The current picture across every source, on one page. Rewritten at each ingest, not appended to.

## The picture so far
- [[wiki/sources/Source - LLM Wiki]] describes the compiled-wiki pattern this vault implements. It has three layers (raw sources, wiki, schema) and three operations (ingest, query, lint), and it is navigated with an index and a log ([[raw/karpathy-llm-wiki.md]]).
- [[wiki/sources/Source - As We May Think]], writing in 1945, argues that conventional one-path indexing can't keep up with a growing record. It proposes the [[wiki/concepts/Memex]], a personal device built on [[wiki/concepts/Associative indexing]], where any two items can be permanently linked and the resulting trails replayed, branched, annotated and shared ([[raw/bush-as-we-may-think.pdf]]).
- [[wiki/sources/Source - Evergreen notes]] defines [[wiki/concepts/Evergreen notes]]: notes written to accumulate across projects, governed by five principles (atomic, concept-oriented, densely linked, associative over hierarchical, written for yourself) and aimed at "better thinking" rather than better note-taking ([[raw/matuschak-evergreen-notes.md]]). The clip is a hub page: it states the principles by title only.

## Where sources agree
- **Association over hierarchy.** Bush sets associative trails against filing under one classification path ([[raw/bush-as-we-may-think.pdf#page=14]]). Matuschak prefers associative ontologies to hierarchical taxonomies ([[raw/matuschak-evergreen-notes.md]]).
- **Accumulation.** The gist calls the wiki "a persistent, compounding artifact" ([[raw/karpathy-llm-wiki.md]]). Evergreen notes "accumulate over time, across projects" ([[raw/matuschak-evergreen-notes.md]]).
- **Memex as forerunner.** The gist names the [[wiki/concepts/Memex]] as the compiled wiki's forerunner and casts the LLM as solving the upkeep problem Bush left open ([[raw/karpathy-llm-wiki.md]]). Bush himself has people build the trails, even anticipating "trail blazers" ([[raw/bush-as-we-may-think.pdf#page=17]]).

## How the units and links compare
- **Unit.** Bush links items already on the record, such as pages of books ([[raw/bush-as-we-may-think.pdf#page=16]]). The compiled wiki's unit is an entity or concept page ([[raw/karpathy-llm-wiki.md]]). An evergreen note is written to be atomic ([[raw/matuschak-evergreen-notes.md]]).
- **Links.** Bush's links are ordered trails ([[raw/bush-as-we-may-think.pdf]]). The compiled wiki's are cross-references the LLM maintains and lint checks ([[raw/karpathy-llm-wiki.md]]). Evergreen notes should be densely linked ([[raw/matuschak-evergreen-notes.md]]), but the captured page doesn't say how.
- **Who links.** Bush: the user or a trail blazer. The compiled wiki: the LLM. Evergreen notes: you, writing for yourself.

## Where sources disagree
- None found. There is one open tension. Matuschak says write for yourself, because the value is better thinking ([[raw/matuschak-evergreen-notes.md]]). The gist says "you read it; the LLM writes it" ([[raw/karpathy-llm-wiki.md]]). They aim at different goals, so this isn't marked contested.

## Gaps worth a new source
- The 15 Matuschak notes the hub links to but which were not captured. The priorities are "atomic", "concept-oriented", "densely linked", "prefer associative ontologies to hierarchical taxonomies" and "similarities and differences … Zettelkasten". The full list is on [[wiki/sources/Source - Evergreen notes]].
- A primary source on the Zettelkasten, such as Luhmann's "Communicating with Slip Boxes", cited in the Matuschak page.
- No source yet tracing the line from Bush's memex to modern hypertext and wiki systems (carried over).
- No source yet on how well the compiled-wiki pattern holds up at scale (carried over).
- No independent source on alternatives to the compiled wiki, such as embedding-based RAG (carried over).

## Sources so far
- [[wiki/sources/Source - LLM Wiki]]: Karpathy's gist proposing the compiled-wiki pattern.
- [[wiki/sources/Source - As We May Think]]: Bush's 1945 essay proposing the memex and associative indexing.
- [[wiki/sources/Source - Evergreen notes]]: Matuschak's hub page defining evergreen notes and their five principles.
