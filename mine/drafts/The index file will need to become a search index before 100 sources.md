---
type: insight
status: draft
origin: claude
created: "2026-09-22"
checked: "2026-09-25"
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

## Check 2026-09-25
**Evidence:** 1 problem
- Quote "moderate scale (~100 sources, ~hundreds of pages)" → holds, uncited · raw/karpathy-llm-wiki.md line 58
- The source names a ceiling, not indefinite scaling → holds, uncited · raw/karpathy-llm-wiki.md lines 58, 64 ("as the wiki grows you want proper search")
- Fallback is qmd or a vibe-coded search script → holds, uncited · raw/karpathy-llm-wiki.md line 64
- qmd is the option to reach for "not embedding-based RAG" → holds in part: qmd is "hybrid BM25/vector search and LLM re-ranking", so it uses embeddings; only the naive script avoids them · raw/karpathy-llm-wiki.md line 64
**Reasoning, not in a source:** decide the upgrade trigger now; your domains could bring 100 sources fast; the title's "before 100" goes past the source, which says the index works well at ~100
**Leans on:** [[wiki/concepts/Compiled wiki]] · contested: whether RAG builds nothing up (Karpathy vs Anthropic), and RAG as the thing to replace or improve
**Links:** fine
**Overlaps:** [[Exact-match search matters more than embeddings for banking documents]] · builds on (both pick qmd as the step after `index.md`)
