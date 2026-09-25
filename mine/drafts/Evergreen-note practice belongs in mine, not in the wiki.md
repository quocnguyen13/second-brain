---
type: insight
status: draft
origin: claude
created: "2026-09-22"
checked: "2026-09-25"
related: ["[[wiki/concepts/Evergreen notes]]", "[[wiki/concepts/Compiled wiki]]", "[[wiki/sources/Source - Evergreen notes]]"]
---
# Evergreen-note practice belongs in mine, not in the wiki

Matuschak's value comes from you writing the notes, because the point is better thinking. Karpathy's wiki is written by the LLM and read by you. The two don't conflict if the vault keeps them apart: `wiki/` is the compiled record, and `mine/insights/` is where evergreen-style writing happens. An LLM-written insight draft only becomes evergreen once you rewrite it in your own words.

## Why I think this
- Evergreen notes: "better thinking," not "better note-taking"; write for yourself by default ([[raw/matuschak-evergreen-notes.md]]).
- Compiled wiki: "you read it; the LLM writes it" ([[raw/karpathy-llm-wiki.md]]).
- This vault already splits `wiki/` (Claude's) from `mine/` (yours).

## Relations
- supports:: [[wiki/concepts/Evergreen notes]]
- contradicts:: 
- extends:: [[wiki/concepts/Compiled wiki]]
- source:: [[wiki/sources/Source - Evergreen notes]]

## Check 2026-09-25
**Evidence:** 1 problem
- Matuschak: "better thinking," not "better note-taking" → holds · raw/matuschak-evergreen-notes.md line 11
- Write for yourself by default → holds · raw/matuschak-evergreen-notes.md line 19 (title only)
- Matuschak's value comes from you writing the notes → holds in part: the page says write for yourself "disregarding audience", which is about audience, not who writes · raw/matuschak-evergreen-notes.md line 19
- "you read it; the LLM writes it" → holds · raw/karpathy-llm-wiki.md line 42
- The vault splits `wiki/` (Claude's) from `mine/` (yours) → holds · `CLAUDE.md`, Vault schema
- A draft becomes yours only when you write your own page → holds · `system/conventions.md`, Page types (insight)
**Reasoning, not in a source:** the two practices don't conflict if kept in separate layers; a rewritten draft counts as "evergreen"
**Leans on:** [[wiki/concepts/Evergreen notes]] · contested: concepts and associations (Matuschak) vs projects in a hierarchy (Forte); [[wiki/concepts/Compiled wiki]] · contested: whether RAG builds nothing up, and RAG as the thing to replace or improve
**Links:** fine
**Overlaps:** [[Organise work by project and knowledge by concept]] · builds on (same move: settle a dispute by giving each side its own layer)
