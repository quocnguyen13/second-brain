---
type: overview
status: verified
sources: ["[[raw/karpathy-llm-wiki.md]]", "[[raw/bush-as-we-may-think.pdf]]", "[[raw/matuschak-evergreen-notes.md]]", "[[raw/anthropic-contextual-retrieval.md]]", "[[raw/forte-para-method.md]]"]
created: "2026-09-22"
updated: "2026-09-22"
tags: ["compiled-wiki", "knowledge-management", "memex", "note-taking", "information-retrieval"]
---
# Overview

The current picture across every source, on one page. Rewritten at each ingest, not appended to.

## The picture so far
- **LLM Wiki.** [[wiki/sources/Source - LLM Wiki]] describes the compiled-wiki pattern that this vault implements:
  - three layers: raw sources, wiki, schema
  - three operations: ingest, query, lint
  - navigation through an index and a log ([[raw/karpathy-llm-wiki.md]])
- **As We May Think.** [[wiki/sources/Source - As We May Think]] (1945) argues that one-path indexing can't keep up with a growing record. It proposes the [[wiki/concepts/Memex]], built on [[wiki/concepts/Associative indexing]]: any two items can be permanently linked, and the trails that result can be replayed, branched and shared ([[raw/bush-as-we-may-think.pdf]]).
- **Evergreen notes.** [[wiki/sources/Source - Evergreen notes]] defines [[wiki/concepts/Evergreen notes]]: notes that accumulate across projects, under five principles, aimed at "better thinking" ([[raw/matuschak-evergreen-notes.md]]). The clip is a hub page and states the principles by title only.
- **Contextual Retrieval.** [[wiki/sources/Source - Contextual Retrieval]] argues for retrieval rather than compiling:
  - below 200,000 tokens, put the whole knowledge base in the prompt
  - above that, use [[wiki/concepts/Retrieval-augmented generation]], improved by [[wiki/concepts/Contextual Retrieval]], [[wiki/concepts/BM25]] and [[wiki/concepts/Reranking]] ([[raw/anthropic-contextual-retrieval.md]])
- **The PARA Method.** [[wiki/sources/Source - The PARA Method]] is the first source about organising working material, not knowledge. The [[wiki/concepts/PARA method]] files everything into Projects, Areas, Resources and Archives. It puts [[wiki/concepts/Organizing by actionability]] first, meaning by current projects and goals rather than by subject, and it insists that projects (which end) be kept apart from areas (which don't) ([[raw/forte-para-method.md]]).

## Where sources agree
- **Subject classification fails as a way to find things.**
  - Bush: one fixed classification path ([[raw/bush-as-we-may-think.pdf#page=14]]).
  - Forte: "rummaging through a vast category like 'Psychology'" ([[raw/forte-para-method.md]]).
- **Association over hierarchy, as a principle for knowledge.**
  - Bush sets associative trails against single-path filing ([[raw/bush-as-we-may-think.pdf#page=14]]).
  - Matuschak prefers associative ontologies to hierarchical taxonomies ([[raw/matuschak-evergreen-notes.md]]).
  - Forte dissents (see below).
- **Accumulation.**
  - The gist calls the wiki "a persistent, compounding artifact" ([[raw/karpathy-llm-wiki.md]]).
  - Evergreen notes "accumulate over time, across projects" ([[raw/matuschak-evergreen-notes.md]]).
- **Simplicity of upkeep.**
  - Forte: a system as complex as your life eats the time it should save ([[raw/forte-para-method.md]]).
  - The gist hands upkeep to the LLM because humans abandon wikis when maintenance outgrows value ([[raw/karpathy-llm-wiki.md]]).
- **Memex as forerunner.** The gist names the [[wiki/concepts/Memex]] as its forerunner, with the LLM doing the upkeep Bush left to people ([[raw/karpathy-llm-wiki.md]], [[raw/bush-as-we-may-think.pdf#page=17]]).
- **Small corpora don't need RAG.**
  - The gist reads an index at around 100 sources ([[raw/karpathy-llm-wiki.md]]).
  - Anthropic puts everything in the prompt under 200,000 tokens ([[raw/anthropic-contextual-retrieval.md]]).
- **The search stack, when one is needed.** Both recommend hybrid BM25/vector search plus reranking ([[raw/karpathy-llm-wiki.md]], [[raw/anthropic-contextual-retrieval.md]]).

## How the units, links and organising axis compare
- **Unit.**
  - Bush: items already on the record ([[raw/bush-as-we-may-think.pdf#page=16]]).
  - Compiled wiki: entity or concept pages ([[raw/karpathy-llm-wiki.md]]).
  - Evergreen notes: an atomic note ([[raw/matuschak-evergreen-notes.md]]).
  - RAG: a chunk of a few hundred tokens ([[raw/anthropic-contextual-retrieval.md]]).
  - PARA: a file or note inside a project, area, resource or archive folder ([[raw/forte-para-method.md]]).
- **Links.**
  - Bush: ordered trails ([[raw/bush-as-we-may-think.pdf]]).
  - Compiled wiki: cross-references maintained by the LLM ([[raw/karpathy-llm-wiki.md]]).
  - Evergreen notes: dense links ([[raw/matuschak-evergreen-notes.md]]).
  - RAG: none, only similarity ([[raw/anthropic-contextual-retrieval.md]]).
  - PARA: none described. Location does the work ([[raw/forte-para-method.md]]).
- **Organising axis.**
  - Compiled wiki: topic, meaning entities and concepts ([[raw/karpathy-llm-wiki.md]]).
  - Evergreen notes: concept ([[raw/matuschak-evergreen-notes.md]]).
  - PARA: actionability, meaning projects first ([[raw/forte-para-method.md]]).

## Where sources disagree
- **Hierarchy by project, or associative ontology.** Contested on [[wiki/concepts/PARA method]], [[wiki/concepts/Organizing by actionability]], [[wiki/concepts/Evergreen notes]] and [[wiki/concepts/Associative indexing]].
  - Forte files each item in one home in a four-category hierarchy, by project, so "you'll know exactly where to put everything, and exactly where to find it" ([[raw/forte-para-method.md]]).
  - Matuschak prefers "associative ontologies to hierarchical taxonomies" and "concept-oriented" notes that outlive projects ([[raw/matuschak-evergreen-notes.md]]).
  - Bush calls single-path filing artificial ([[raw/bush-as-we-may-think.pdf#page=14]]).
  - Scope: Forte is organising material for action; the others are linking ideas and records for thinking and recall.
- **Does RAG build anything up?** Contested on [[wiki/concepts/Compiled wiki]] and [[wiki/concepts/Retrieval-augmented generation]].
  - The gist: "There's no accumulation" ([[raw/karpathy-llm-wiki.md]]).
  - Anthropic: an LLM generates per-chunk context once, at preprocessing ([[raw/anthropic-contextual-retrieval.md]]).
- **Replace retrieval or improve it.**
  - The gist offers the compiled wiki as the alternative ([[raw/karpathy-llm-wiki.md]]).
  - Anthropic treats RAG as the default at scale ([[raw/anthropic-contextual-retrieval.md]]).
  - Not a head-to-head result.
- **Open tensions, not contested.**
  - Who writes: Matuschak says yourself ([[raw/matuschak-evergreen-notes.md]]); the gist says the LLM ([[raw/karpathy-llm-wiki.md]]).
  - Topic pages vs. project folders: the compiled wiki's concept pages ([[raw/karpathy-llm-wiki.md]]) vs. PARA's projects-first order ([[raw/forte-para-method.md]]). Neither source addresses the other.

## Gaps worth a new source
- The rest of Forte's PARA material, if the clip is partial: setting it up, moving items between categories, how PARA relates to linking. Also any Forte piece on how PARA and a knowledge base or Zettelkasten fit together.
- Matuschak's uncaptured notes, especially "concept-oriented" and "prefer associative ontologies to hierarchical taxonomies". They hold the reasons that the PARA disagreement turns on.
- A head-to-head comparison of a compiled wiki and RAG on the same corpus and questions (carried over).
- An independent evaluation of Contextual Retrieval, plus Anthropic's Appendix II (carried over).
- How the compiled-wiki pattern holds up at scale (carried over).
- A primary source on the Zettelkasten, such as Luhmann (carried over).
- The line from Bush's memex to modern hypertext and wikis (carried over).

## Sources so far
- [[wiki/sources/Source - LLM Wiki]]: Karpathy's gist proposing the compiled-wiki pattern.
- [[wiki/sources/Source - As We May Think]]: Bush's 1945 essay proposing the memex and associative indexing.
- [[wiki/sources/Source - Evergreen notes]]: Matuschak's hub page defining evergreen notes and their five principles.
- [[wiki/sources/Source - Contextual Retrieval]]: Anthropic's post on improving RAG.
- [[wiki/sources/Source - The PARA Method]]: Forte's four-category system for organising by actionability.
