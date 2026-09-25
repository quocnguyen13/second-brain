---
type: insight
status: draft
origin: claude
created: "2026-09-22"
checked: "2026-09-25"
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

## Check 2026-09-25
**Evidence:** 3 problems
- Memex forges permanent, replayable links between items → holds, uncited · raw/bush-as-we-may-think.pdf page 16
- Conventional indexing files each item on one fixed path → holds, uncited · raw/bush-as-we-may-think.pdf page 14
- Joining two items so viewing one recalls the other → holds, uncited · raw/bush-as-we-may-think.pdf page 16
- Trails replayed, branched, annotated, handed on → holds, uncited · raw/bush-as-we-may-think.pdf pages 16–17
- RAG rediscovers knowledge from scratch on every query → holds, uncited · raw/karpathy-llm-wiki.md line 20
- Entity and concept pages accumulate citations and cross-references → holds in part: raw/ says entity pages are updated and cross-references maintained; accumulating citations is this vault's ingest rule, not the gist's · raw/karpathy-llm-wiki.md lines 22, 42
- Bush's user taps a key for every join → holds, uncited · raw/bush-as-we-may-think.pdf page 16
- This vault's ingest has the LLM update and link the pages a source touches → holds · `.claude/skills/ingest/SKILL.md` step 4
- "Who builds the links changed" is "not a claim either source makes" → wrong: Karpathy says Bush couldn't solve "who does the maintenance. The LLM handles that." · raw/karpathy-llm-wiki.md line 81
- Wrong label: "(general knowledge)" is on a step of reasoning
**Reasoning, not in a source:** both problems are "found one associative link at a time"; the trail survives whoever builds it
**Leans on:** [[wiki/concepts/Associative indexing]] · contested: one home per item (Forte) vs association (Bush); [[wiki/concepts/Compiled wiki]] · contested: whether RAG builds nothing up, and RAG as the thing to replace or improve
**Links:** fine
**Overlaps:** [[This vault's raw-wiki split is Bush's record-consulted record split]] · builds on; [[Bush linked documents, evergreen notes link ideas]] · builds on
