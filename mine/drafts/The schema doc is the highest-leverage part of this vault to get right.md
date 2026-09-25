---
type: insight
status: draft
origin: claude
created: "2026-09-22"
checked: "2026-09-25"
related: ["[[wiki/concepts/Compiled wiki]]", "[[wiki/sources/Source - LLM Wiki]]"]
---
# The schema doc is the highest-leverage part of this vault to get right

Time spent tightening `CLAUDE.md` and `system/conventions.md` pays off more than time spent on any single ingest, because every page this vault will ever hold gets filtered through those rules.

## Why I think this
- The source calls the schema "the key configuration file — it's what makes the LLM a disciplined wiki maintainer rather than a generic chatbot," distinct from the raw and wiki layers.
- It also says the schema is meant to be co-evolved as you learn what works for your domain — implying it's expected to need revision, not a one-time setup cost.
- A citation or naming mistake baked into the schema would replicate across every future ingest silently, whereas a mistake in one wiki page stays contained to that page.

## Relations
- supports:: [[wiki/concepts/Compiled wiki]]
- contradicts::
- extends::
- source:: [[wiki/sources/Source - LLM Wiki]]

## Check 2026-09-25
**Evidence:** clean
- Quote "the key configuration file — it's what makes the LLM a disciplined wiki maintainer rather than a generic chatbot" → holds, uncited · raw/karpathy-llm-wiki.md line 44
- Schema is distinct from the raw and wiki layers → holds, uncited · raw/karpathy-llm-wiki.md lines 38–44
- Schema is co-evolved as you learn your domain → holds, uncited · raw/karpathy-llm-wiki.md line 44
**Reasoning, not in a source:** every page is filtered through `CLAUDE.md` and `system/conventions.md`; a schema mistake replicates silently, a page mistake stays contained; tightening the schema pays more than any single ingest
**Leans on:** [[wiki/concepts/Compiled wiki]] · contested: whether RAG builds nothing up (Karpathy vs Anthropic), and RAG as the thing to replace or improve
**Links:** fine
**Overlaps:** [[Per-source review beats batch ingest for this vault]] · builds on
