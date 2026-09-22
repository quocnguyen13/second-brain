---
type: concept
status: verified
sources: ["[[raw/karpathy-llm-wiki.md]]"]
created: "2026-09-22"
updated: "2026-09-22"
tags: ["compiled-wiki"]
---
# Wiki ingest

The operation of processing one new raw source into the wiki: summarizing it, updating the pages it touches, and logging the change ([[raw/karpathy-llm-wiki.md]]).

## What the sources say
- Flow: the LLM reads the source, discusses key takeaways with the person, writes a summary page, updates the index, updates relevant entity and concept pages across the wiki, and appends a log entry ([[raw/karpathy-llm-wiki.md]]).
- A single source might touch 10-15 wiki pages ([[raw/karpathy-llm-wiki.md]]).
- The source's author prefers ingesting one source at a time and staying involved — reading summaries, checking updates, guiding what to emphasize — though batch ingest with less supervision is also possible; the workflow is meant to be developed and documented in the schema ([[raw/karpathy-llm-wiki.md]]).

## Where sources disagree
- None found.

## Mentioned in
- [[wiki/sources/Source - LLM Wiki]]

## Related
- [[wiki/concepts/Compiled wiki]]
- [[wiki/concepts/Wiki query]]
- [[wiki/concepts/Wiki lint]]
- [[wiki/concepts/Wiki index and log]]
