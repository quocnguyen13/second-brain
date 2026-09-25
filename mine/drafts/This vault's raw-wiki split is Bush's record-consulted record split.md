---
type: insight
status: draft
origin: claude
created: "2026-09-22"
checked: "2026-09-25"
related: ["[[wiki/concepts/Memex]]", "[[wiki/concepts/Compiled wiki]]", "[[wiki/sources/Source - As We May Think]]"]
---
# This vault's raw-wiki split is Bush's record-consulted record split

Bush treats making and storing the record as one problem and consulting it as a separate, harder one — bulk microfilm storage solves the first, associative trails solve the second. This vault draws the same line: `raw/` is the immutable store nobody browses directly, `wiki/` is the associatively-linked layer built to be consulted.

## Why I think this
- Bush says storage isn't the hard part: even a great library "is not generally consulted; it is nibbled by a few," and compression alone "is not enough; one needs not only to make and store a record but also to be able to consult it."
- This vault's own rule that `raw/` is read-only, and that every wiki claim must trace back to a raw file, keeps the two problems institutionally separate the same way — that structural parallel is my own reading of this vault's design against Bush's essay, not a claim either source states. (general knowledge)

## Relations
- supports:: [[wiki/concepts/Memex]]
- extends:: [[wiki/concepts/Compiled wiki]]
- contradicts::
- source:: [[wiki/sources/Source - As We May Think]]

## Check 2026-09-25
**Evidence:** 3 problems
- Bush separates making and storing the record from consulting it, the harder part → holds, uncited · raw/bush-as-we-may-think.pdf pages 4, 7, 12
- Microfilm solves storage → holds, uncited · raw/bush-as-we-may-think.pdf pages 7, 15
- Associative trails solve consultation → holds, uncited · raw/bush-as-we-may-think.pdf pages 14, 16
- Quote "is not generally consulted; it is nibbled by a few" → holds, uncited · raw/bush-as-we-may-think.pdf page 7
- Quote "is not enough; one needs not only to make and store a record but also to be able to consult it" → holds, uncited · raw/bush-as-we-may-think.pdf page 7
- `raw/` is read-only and every wiki claim traces to a raw file → holds · `CLAUDE.md`, Citation discipline and Standing rules
- `raw/` is a store "nobody browses directly" → holds in part: every wiki claim cites a raw file and ingest, lint and drafts all read `raw/` · `CLAUDE.md`, Citation discipline and Operations
- Left out: Bush's stored record isn't immutable; the user adds marginal notes and comments to it and enters longhand notes directly · raw/bush-as-we-may-think.pdf pages 15–16
- Wrong label: "(general knowledge)" is on a step of reasoning
**Reasoning, not in a source:** the vault's raw/wiki rules keep the two problems institutionally separate, as Bush does
**Leans on:** [[wiki/concepts/Compiled wiki]] · contested: whether RAG builds nothing up, and RAG as the thing to replace or improve
**Links:** fine
**Overlaps:** [[The compiled wiki is a memex with an LLM doing the trail-building]] · builds on
