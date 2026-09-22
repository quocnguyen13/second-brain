---
type: project-doc
project: thinking-system
status: active
trust: ai-draft
origin: claude
created: 2026-09-22
reviewed: 2026-09-22
tags: [project/thinking-system, handover]
---

# 17 M3 Handover

Back to [[00 Project Home]] · Modules in [[06 Roadmap]] §2 · Previous: [[16 M2 Handover]]

**Module M3 – First Ingests · closed 2026-09-22. Next: M4 – Ask and File-back.**

## What was done
- The `ingest` skill was written, placed at `.claude/skills/ingest/SKILL.md`, and revised three times as the first ingests exposed gaps. It is mirrored in [[08 Claude Operating Instructions]] §4.1. `CLAUDE.md`'s ingest section is now a three-line pointer (D-012, D-041).
- Five sources were ingested one at a time, each reviewed before the next (D-022):
  1. Karpathy, LLM Wiki gist
  2. Bush, "As We May Think" (MIT's full-text PDF, after the first clip turned out to be page 1 of 4)
  3. Matuschak, "Evergreen notes" (the hub page only)
  4. Anthropic, "Introducing Contextual Retrieval"
  5. Forte, "The PARA Method"
- The compile loop works. Source 5 updated six existing pages, three of them with new cited claims, against an exit bar of three.
- Two real disagreements are recorded on both sides, with the sources named:
  - Karpathy's "RAG builds nothing up" against Anthropic's per-chunk context generated once at preprocessing.
  - Forte's single home chosen by actionability against Bush's and Matuschak's association over hierarchy.
- `wiki/overview.md`, `index.md` and `log.md` are live and rewritten or appended at every ingest.

## What the ingests taught us, and what changed because of it
| What happened | What changed |
|---|---|
| The `raw/` deny rule blocked Claude's shell move, not just its file tools | The move is yours, with the command handed to you in the skill's first message (D-045) |
| Ingest 1 marked every page `unverified` because each cited only one source | The status rule was spelled out: one source is enough; status records whether claims are cited |
| Ingest 2 missed that source 1 already discussed Bush's memex | The skill now searches `wiki/` and `raw/` for every new source before writing, and the review added the missing links |
| Tracing a claim in a 20-page PDF was slow | PDF citations carry the page: `([[raw/<name>.pdf#page=N]])` (D-046) |
| Ingest 4 left five pages `contested`, most of the wiki's spine | `contested` now goes only on pages carrying the disputed claim (D-047) |
| Claude saved a PDF text extraction into `inbox/sources/`, then offered to delete it and tried straight away | Ground rules: file tools not shell browsing, no working files in the vault, no deletions |
| A clip from a four-page reprint looked complete but wasn't | "Pages: 1 \| 2 \| 3" and "next" links now count as a partial-clip flag |

## Decisions made in M3
All accepted on 2026-09-22.
- **D-040:** the skills synced from claude.ai are hidden in vault sessions (`skillOverrides`). Parked until the list of names is to hand.
- **D-041:** vault skills run only when you type their command, and carry no `allowed-tools`.
- **D-042:** a source is renamed as it moves into `raw/`: `<author>-<short-title>.<ext>`.
- **D-043:** sources reach `inbox/sources/` as files you save. Claude doesn't fetch links into the zone.
- **D-044:** `wiki/overview.md` is its own page type with its own template, rewritten at each ingest.
- **D-045:** you run the move into `raw/` yourself, with the command the skill gives you.
- **D-046:** citations to a PDF carry the page number.
- **D-047:** `contested` marks only the pages that carry the disputed claim.

## State of the vault
- **`raw/`:** 5 sources, immutable, each moved in by you.
- **`wiki/`:** 26 pages — 15 concepts, 5 entities, 5 source pages and `overview.md`.
  - `contested` (4): `PARA method`, `Organizing by actionability`, `Evergreen notes`, `Associative indexing`. `Compiled wiki` and `Retrieval-augmented generation` carry the RAG disagreement.
  - `unverified` (1): `Karpathy`, whose full name comes from general knowledge and is labelled as such. It makes a ready-made case for lint in M5.
  - Everything else is `verified`.
- **`mine/drafts/`:** 11 insight drafts waiting for your decision. None has been promoted to `mine/insights/`; that routine is M6.
- **Gaps recorded in the overview:** Matuschak's 15 uncaptured notes, a primary Zettelkasten source, the memex-to-hypertext lineage, how the compiled wiki holds up at scale, and an independent comparison of compiled wiki against RAG.
- **Branch `main`**, in step with `origin/main` once the last batch is pushed.

## What M4 must produce
1. The `ask` skill at `.claude/skills/ask/SKILL.md`, and `file-answer`, following the same pattern as `ingest`: user-invoked only, no `allowed-tools`, mirrored in doc 08 §4.
2. The 10 test prompts in [[08 Claude Operating Instructions]] §5 run and recorded in `system/test-results.md`.
3. One answer filed back as a page in `wiki/analyses/`, which is still empty.

**M4 is done when** at least 9 of the 10 prompts pass and one answer is filed as an analysis page.

**The test conditions are already in place**, so nothing needs planting:
- Test 4 (do any sources disagree?) has two real disagreements to find.
- Test 5 (what's unverified?) has the `Karpathy` page.
- Test 7 (a source containing instructions) can use the contextualizer prompt inside the Contextual Retrieval clip, which the ingest already treated as data.

## Open questions
| ID | Question | Due |
|---|---|---|
| Q-015 | Hide the synced claude.ai skills (D-040): the `skillOverrides` entry still needs the names from `~/.claude/skills/synced` | When you're next at the terminal |
| Q-008 | Which product-owner routines matter most | M7 |
| Q-004 | Your bank's AI-tools policy | M8, with doc 12 |

## Parked in M3
- Matuschak's five principle notes and a primary Zettelkasten source.
- The ingest report splitting "updated" into pages that gained a claim and pages that only gained a link.
- D-040's settings entry (Q-015 above).

## Risks to watch in M4
- **Answers that read well and cite nothing.** The `ask` skill has to refuse to answer from the wiki when the wiki has nothing, and say so before falling back to general knowledge. Test 6 checks exactly that.
- **Filed answers becoming evidence.** An analysis page cites `raw/` like any other page, never another wiki page (D-021). Watch for it in the first `file-answer` run.
- **The index doing the finding.** `index.md` is now 26 lines of summaries. If `ask` starts missing relevant pages, that's the signal for the search tool the drafts already flag, not a reason to loosen the citation rules.
- **Obsidian overwriting Claude's edits.** A change-log entry vanished in M3 because a project document was open in Obsidian while it was being written. Keep the documents closed while files are being delivered, and check `git diff` before committing.
