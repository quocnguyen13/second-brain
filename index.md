# Index

Catalog of every wiki page, one line each. Claude maintains it; format in `system/conventions.md`.

## Overview

- [[wiki/overview.md]] — five sources: the compiled-wiki pattern, Bush's memex, Matuschak's evergreen notes, Anthropic's case for improved retrieval, Forte's PARA; records the disagreements on whether RAG accumulates anything and on project hierarchy vs associative ontology (5 sources)

## Sources

- [[wiki/sources/Source - LLM Wiki]] — Karpathy's gist proposing the compiled-wiki pattern: three layers, three operations, index/log; records the Contextual Retrieval disagreement and an open point with PARA (3 sources)
- [[wiki/sources/Source - As We May Think]] — Bush's 1945 essay proposing the memex and associative indexing as a fix for one-path indexing; records the PARA disagreement (3 sources)
- [[wiki/sources/Source - Evergreen notes]] — Matuschak's hub page defining evergreen notes and five principles; linked notes not captured; records the PARA disagreement (4 sources)
- [[wiki/sources/Source - Contextual Retrieval]] — Anthropic's post: long prompt under 200k tokens, else RAG improved by contextualised chunks, BM25 and reranking (1 source)
- [[wiki/sources/Source - The PARA Method]] — Forte's four-category system (Projects, Areas, Resources, Archives) organised by actionability; set against Matuschak, Bush and the compiled wiki (4 sources)

## Entities

- [[wiki/entities/Karpathy]] — author of the LLM Wiki gist (1 source)
- [[wiki/entities/Vannevar Bush]] — author of "As We May Think," proposed the memex (2 sources)
- [[wiki/entities/Andy Matuschak]] — author of the "Evergreen notes" page (1 source)
- [[wiki/entities/Anthropic]] — publisher of the Contextual Retrieval post; maker of Claude and prompt caching (1 source)
- [[wiki/entities/Tiago Forte]] — author of the PARA method post; former productivity coach (1 source)

## Concepts

- [[wiki/concepts/Compiled wiki]] — an LLM-maintained, three-layer wiki that compounds knowledge instead of re-deriving it; contested on its RAG premise; topic-organised, open point with PARA (3 sources)
- [[wiki/concepts/Wiki ingest]] — the operation that files one new source into the wiki (1 source)
- [[wiki/concepts/Wiki query]] — the operation that answers a question from the wiki and can file the answer back (1 source)
- [[wiki/concepts/Wiki lint]] — the operation that health-checks the wiki for contradictions, staleness, and gaps (1 source)
- [[wiki/concepts/Wiki index and log]] — the content catalog and the chronological record that keep the wiki navigable; small-scale alternatives to RAG (2 sources)
- [[wiki/concepts/Memex]] — Bush's proposed personal device for storing and associatively linking a lifetime's records (2 sources)
- [[wiki/concepts/Associative indexing]] — finding records by association instead of fixed classification; contested by PARA's one-home-per-item filing (3 sources)
- [[wiki/concepts/Evergreen notes]] — notes written to accumulate across projects: atomic, concept-oriented, densely linked; contested by PARA's project-first hierarchy (4 sources)
- [[wiki/concepts/Retrieval-augmented generation]] — retrieving chunks at query time and adding them to the prompt; contested on whether it accumulates anything (2 sources)
- [[wiki/concepts/Contextual Retrieval]] — LLM-written per-chunk context prepended before embedding and BM25 indexing (1 source)
- [[wiki/concepts/BM25]] — lexical ranking function for exact-term matches, paired with embeddings in hybrid search (2 sources)
- [[wiki/concepts/Reranking]] — scoring retrieved chunks and keeping only the top ones; accuracy vs latency trade-off (2 sources)
- [[wiki/concepts/Prompt caching]] — caching prompt content between API calls; makes long prompts and Contextual Retrieval cheaper (1 source)
- [[wiki/concepts/PARA method]] — Projects, Areas, Resources, Archives; projects end, areas don't; contested on hierarchy vs association (3 sources)
- [[wiki/concepts/Organizing by actionability]] — organise by current projects and goals, not subjects; contested against concept-oriented, associative notes (4 sources)

## Analyses

- [[wiki/analyses/Compare the PARA method and evergreen notes as ways to organise what I read]] — PARA files items by project for action; evergreen notes link concepts for thinking and suit reading better; contested on hierarchy vs association (3 sources)
