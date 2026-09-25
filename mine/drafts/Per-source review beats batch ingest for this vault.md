---
type: insight
status: draft
origin: claude
created: "2026-09-22"
checked: "2026-09-25"
related: ["[[wiki/concepts/Wiki ingest]]", "[[wiki/sources/Source - LLM Wiki]]"]
---
# Per-source review beats batch ingest for this vault

Ingesting sources one at a time with your review in the loop, rather than batching many with less supervision, should be the default here — at least while the schema and conventions are still being shaped in M3.

## Why I think this
- The source itself frames per-source review as the author's own preference, precisely because it lets you catch what to emphasize and guide the LLM before pages compound on a wrong assumption.
- This vault's `CLAUDE.md` already enforces "one source per run" and a stop-after-report step, which only pays off if you actually review each report rather than rubber-stamping it.
- Batch ingest becomes more attractive later, once the schema conventions are stable and you've built trust in how the LLM applies them — but adopting it now would risk baking early mistakes into many pages at once.

## Relations
- supports:: [[wiki/concepts/Wiki ingest]]
- contradicts::
- extends::
- source:: [[wiki/sources/Source - LLM Wiki]]

## Check 2026-09-25
**Evidence:** 3 problems
- Per-source review is the author's own preference → holds, uncited · raw/karpathy-llm-wiki.md line 48
- It lets you guide emphasis before pages compound on a wrong assumption → holds in part: raw/ says he reads summaries, checks updates and guides "what to emphasize"; it gives no reason about compounding errors · raw/karpathy-llm-wiki.md line 48
- `CLAUDE.md` enforces one source per run and stop-after-report → holds · `CLAUDE.md`, Operation: ingest
- Schema and conventions still being shaped "in M3" → holds in part: the vault's current focus is M6 · `system/context.md`, Current focus
- Left out: the source treats batch ingest as an equal option: "It's up to you to develop the workflow that fits your style" · raw/karpathy-llm-wiki.md line 48
**Reasoning, not in a source:** review pays only if reports are actually read; batch becomes attractive once conventions are stable; batching now would bake early mistakes into many pages
**Leans on:** no open pages
**Links:** fine
**Overlaps:** [[The schema doc is the highest-leverage part of this vault to get right]] · builds on
