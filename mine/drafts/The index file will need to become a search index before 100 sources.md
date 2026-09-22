---
type: insight
status: draft
origin: claude
created: "2026-09-22"
related: ["[[wiki/concepts/Wiki index and log]]", "[[wiki/concepts/Compiled wiki]]", "[[wiki/sources/Source - LLM Wiki]]"]
---
# The index file will need to become a search index before 100 sources

`index.md` as a flat, hand-read catalog is fine at this vault's current size, but it's worth deciding now what the upgrade trigger is, rather than discovering it once the file is unwieldy.

## Why I think this
- The source's own confidence bound for the index-only approach is "moderate scale (~100 sources, ~hundreds of pages)" — it names a ceiling rather than claiming the approach scales indefinitely.
- Your domain (digital lending, cards, payments, onboarding) is broad enough that 100 sources could arrive faster than expected once ingest becomes routine.
- The source names a concrete fallback (a local tool like `qmd`, or a simple vibe-coded search script) rather than assuming embeddings are the only next step — worth noting as the option to reach for, not embedding-based RAG, if `index.md` starts to strain.

## Relations
- supports:: [[wiki/concepts/Wiki index and log]]
- contradicts::
- extends:: [[wiki/concepts/Compiled wiki]]
- source:: [[wiki/sources/Source - LLM Wiki]]
