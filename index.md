# Index

Catalog of every wiki page, one line each. Claude maintains it; format in `system/conventions.md`.

## Overview

- [[wiki/overview.md]] — four sources: the compiled-wiki pattern, Bush's memex, Matuschak's evergreen notes, Anthropic's case for improved retrieval; records the disagreement on whether RAG accumulates anything (4 sources)

## Sources

- [[wiki/sources/Source - LLM Wiki]] — Karpathy's gist proposing the compiled-wiki pattern: three layers, three operations, index/log; records the Contextual Retrieval disagreement over its "RAG builds nothing up" claim (2 sources)
- [[wiki/sources/Source - As We May Think]] — Bush's 1945 essay proposing the memex and associative indexing as a fix for one-path indexing (2 sources)
- [[wiki/sources/Source - Evergreen notes]] — Matuschak's hub page defining evergreen notes and five principles; linked notes not captured (3 sources)
- [[wiki/sources/Source - Contextual Retrieval]] — Anthropic's post: long prompt under 200k tokens, else RAG improved by contextualised chunks, BM25 and reranking (1 source)

## Entities

- [[wiki/entities/Karpathy]] — author of the LLM Wiki gist (1 source)
- [[wiki/entities/Vannevar Bush]] — author of "As We May Think," proposed the memex (2 sources)
- [[wiki/entities/Andy Matuschak]] — author of the "Evergreen notes" page (1 source)
- [[wiki/entities/Anthropic]] — publisher of the Contextual Retrieval post; maker of Claude and prompt caching (1 source)

## Concepts

- [[wiki/concepts/Compiled wiki]] — an LLM-maintained, three-layer wiki that compounds knowledge instead of re-deriving it; contested on its RAG premise (2 sources)
- [[wiki/concepts/Wiki ingest]] — the operation that files one new source into the wiki (1 source)
- [[wiki/concepts/Wiki query]] — the operation that answers a question from the wiki and can file the answer back (1 source)
- [[wiki/concepts/Wiki lint]] — the operation that health-checks the wiki for contradictions, staleness, and gaps (1 source)
- [[wiki/concepts/Wiki index and log]] — the content catalog and the chronological record that keep the wiki navigable; small-scale alternatives to RAG (2 sources)
- [[wiki/concepts/Memex]] — Bush's proposed personal device for storing and associatively linking a lifetime's records (2 sources)
- [[wiki/concepts/Associative indexing]] — finding records by association instead of fixed classification (1 source)
- [[wiki/concepts/Evergreen notes]] — notes written to accumulate across projects: atomic, concept-oriented, densely linked (3 sources)
- [[wiki/concepts/Retrieval-augmented generation]] — retrieving chunks at query time and adding them to the prompt; contested on whether it accumulates anything (2 sources)
- [[wiki/concepts/Contextual Retrieval]] — LLM-written per-chunk context prepended before embedding and BM25 indexing (1 source)
- [[wiki/concepts/BM25]] — lexical ranking function for exact-term matches, paired with embeddings in hybrid search (2 sources)
- [[wiki/concepts/Reranking]] — scoring retrieved chunks and keeping only the top ones; accuracy vs latency trade-off (2 sources)
- [[wiki/concepts/Prompt caching]] — caching prompt content between API calls; makes long prompts and Contextual Retrieval cheaper (1 source)

## Analyses
