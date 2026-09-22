---
type: insight
status: draft
origin: claude
created: "2026-09-22"
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
