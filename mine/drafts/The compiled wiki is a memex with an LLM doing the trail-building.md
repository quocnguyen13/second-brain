---
type: insight
status: draft
origin: claude
created: "2026-09-22"
related: ["[[wiki/concepts/Memex]]", "[[wiki/concepts/Associative indexing]]", "[[wiki/concepts/Compiled wiki]]", "[[wiki/sources/Source - As We May Think]]", "[[wiki/sources/Source - LLM Wiki]]"]
---
# The compiled wiki is a memex with an LLM doing the trail-building

Bush's memex let a human forge permanent, replayable links between any two items in a personal record, because conventional indexing files each item on one fixed path. The compiled-wiki pattern this vault runs solves the same problem — knowledge that has to be found one associative link at a time, not re-derived from scratch — except the linking is now done by an LLM working through an ingest procedure instead of a human tapping a key at a desk.

## Why I think this
- Bush's fix for indexing's "one item, one path" limitation was associative indexing: joining two items so that viewing one recalls the other, then chaining joins into a trail that can be replayed, branched, annotated, and handed to someone else.
- The LLM Wiki source frames its own problem the same way: RAG-style retrieval rediscovers knowledge from scratch on every query, losing the structure a persistent, cross-referenced wiki would keep; its fix is also link-based — entity and concept pages that accumulate citations and cross-references over time.
- What changed in eighty years is who builds the links. Bush's user tapped a key by hand for every join; this vault's ingest procedure has the LLM decide what a new source touches and write the connecting pages itself. The trail survives either way — my own reading, not a claim either source makes. (general knowledge)

## Relations
- supports:: [[wiki/concepts/Memex]]
- supports:: [[wiki/concepts/Associative indexing]]
- extends:: [[wiki/concepts/Compiled wiki]]
- contradicts::
- source:: [[wiki/sources/Source - As We May Think]]
- source:: [[wiki/sources/Source - LLM Wiki]]
