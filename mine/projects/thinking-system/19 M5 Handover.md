---
type: project-doc
project: thinking-system
status: active
trust: ai-draft
origin: claude
created: 2026-09-24
reviewed: 2026-09-24
tags: [project/thinking-system, handover]
---

# 19 M5 Handover

Back to [[00 Project Home]] · Modules in [[06 Roadmap]] §2 · Previous: [[18 M4 Handover]]

**Module M5 – Lint and Review · closed 2026-09-24. Next: M6 – Thinking Layer.**

## What was done
- **The `lint` skill**, at `.claude/skills/lint/SKILL.md` and mirrored in [[08 Claude Operating Instructions]] §4.4. It follows the same pattern as the other skills: it runs only when you type the command and carries no `allowed-tools` (D-041). It has two modes:
  - **`/lint`** scans every page, deep-checks cited passages in `raw/`, reads `inbox/checks.md` last, and writes a numbered report to `system/lint/`. It changes nothing in `wiki/` (D-055).
  - **`/lint apply <numbers>`** makes the fixes you name, from the report file, and records them in the report and `log.md`.
- **`CLAUDE.md`:** the lint section is now a pointer to the skill. Two citation rules were added: a mis-cited claim counts as uncited, and `unverified` wins over `contested` (D-057).
- **Review views:** `system/views/Review.base` holds **Needs attention** and **Draft queue** (D-058). It is bookmarked and mirrored in [[05 Obsidian Essentials]] §6.
- **The weekly review:** seven steps in [[05 Obsidian Essentials]] §4.
- **Lint tests L1–L6 passed, 6 of 6**, on the real cases M4 found, with nothing planted (D-059). Results are in `system/test-results.md`. M5's exit criterion, and the lint criterion in [[01 Project Charter]] §6, are met.
- **Two lint passes cleaned the wiki:**
  - 13 fixes from the first report and 3 from the second, all approved by number.
  - The unsupported Resources ranking claim is gone from both pages.
  - Two misquotes of Bush are corrected, and "forerunner" is now "related in spirit to".
  - Cross-references and a missing `sources` entry are added, and every Bush PDF citation now names its pages.
  - No page changed status.

## What the tests taught us, and what changed because of it
| What happened | What changed |
|---|---|
| First run, finding 5: lint asked for citations in an analysis page's Answer. D-051 says the Answer needs none as long as it adds nothing beyond Evidence. The skill's own wording caused it | `lint` A1 and `file-answer` step 4 were reworded to match D-051. Finding 5 was not applied, and the second run cleared it |
| First run: the Resources contradiction was resolved inside finding 1, but the report named the analysis page only in the fix | A contradiction finding now names both pages, with their lines, and says which one `raw/` supports |
| Second run: two real errors on pages the first run had deep-checked and passed (how the PARA clip ends, and an uncited Scope line) | D-060: the first run of each month deep-checks every page. Otherwise a page that doesn't change would never be deep-checked again |
| Second run: lint asked whether a citation to the wrong PDF page is High, which would make the page `unverified` | D-061: it's a Low location fix when the claim is in the cited file |
| Obsidian rewrote `Review.base` in its own style when the view was first used | No change. The doc 05 mirror now copies the vault's version |
| The apply run pointed out a gap its fix didn't cover instead of fixing beyond the report | No change. This is the behaviour D-055 wants |

## Decisions made in M5
All accepted on 2026-09-24 except D-062.
- **D-053:** one recommendation rule. **D-054:** never install anything, never ask to. Both were proposed in M4.
- **D-055:** `/lint` reports, then stops. Fixes are made only by number.
- **D-056:** deep checks follow what changed. **D-060** adds a full deep check on the first run of each month.
- **D-057:** a mis-cited claim is uncited, and `unverified` wins over `contested`.
- **D-058:** both review views live in one Bases file in `system/views/`.
- **D-059:** the M5 exit test uses the real cases, with nothing planted.
- **D-061:** a wrong PDF page is a Low location fix.
- **Proposed, waiting for your word:** **D-062**, the last MVP criterion moves to M6 (see below).

## State of the vault
- **`raw/`:** 5 sources, unchanged.
- **`wiki/`:** 27 pages. `contested`: 7, the same pages as before; `unverified`: 1, `Karpathy`.
- **`system/lint/`:** two reports, `report-2026-09-24` and `report-2026-09-24-2`, with every finding applied except the first report's finding 5, which the second run cleared.
- **`inbox/`:** `checks.md` has no open checks, and `questions.md` is empty.
- **`mine/`:** 11 drafts in `mine/drafts/`, none reviewed yet. `mine/insights/`, `mine/decisions/`, `mine/journal/` and `mine/scratch/` are empty in the pushed repo.
- **Skills:** `ingest`, `ask`, `file-answer` and `lint`.
- **Branch `main`**, in step with `origin/main` at `c38e95b`.
- **Your file, `system/context.md`:** "Current focus" still says M3.

## MVP status ([[01 Project Charter]] §6)
| Criterion | Status |
|---|---|
| 5 sources ingested; `index.md` and `log.md` current | Met (M3) |
| Source 5 updates at least 3 existing pages | Met (M3) |
| 10 test prompts, at least 9 answered from the wiki with correct citations | Met: 10 of 10 (M4) |
| One answer filed back as an analysis page | Met (M4) |
| One lint pass finds a contradiction and an uncited claim | Met: L1–L2 (M5) |
| At least 5 insight pages written or accepted by you in `mine/` | **Not met:** 0 in `mine/insights/`, 11 drafts waiting |

**5 of 6.** D-062 proposes closing M5 on its own exit criterion and meeting the last one in M6. M6's own exit, 5 insight pages you wrote, linked to wiki pages, meets it anyway. If you kept drafts locally and haven't pushed yet, push and this line changes.

## What M6 must produce
From [[06 Roadmap]] §2:
1. `mine/insights/` and `mine/decisions/` in use.
2. The drafts routine: how a Claude draft becomes an insight of yours, or is deleted. [[05 Obsidian Essentials]] §4 step 5 is the current one-line version.
3. The weekly review running, with its first full cycle through steps 4–7.

**M6 is done when** 5 insight pages you wrote are in `mine/insights/`, each linked to wiki pages through its Relations block. That also closes the MVP (D-062).

**Material already waiting:** the 11 drafts. None repeats a claim the lint removed from the wiki; I checked for the ranking, "forerunner" and the misquotes. Lint doesn't read `mine/`, though, so the drafts have never been checked against `raw/`.

## Open questions
| ID | Question | Due |
|---|---|---|
| Q-015 | Hide the synced claude.ai skills (D-040): the `skillOverrides` entry still needs the names from `~/.claude/skills/synced` | When you're next at the terminal |
| Q-008 | Which product-owner routines matter most | M7 |
| Q-004 | Your bank's AI-tools policy | M8, with doc 12 |

## Parked in M5
- **Uncited restating lines.** Lint reads an uncited line that restates claims cited in the same section as synthesis, not as a claim. It made that call on its own. Write it down as a rule if it starts to matter.
- **Checking drafts.** Lint doesn't check `mine/drafts/` against `raw/`. M6 decides whether a draft's claims get checked before you keep it.
- **Sources lint suggested:** a primary source on the Zettelkasten (Luhmann, "Communicating with Slip Boxes"), Matuschak's "Prefer associative ontologies to hierarchical taxonomies" note, and Forte's book chapter on PARA.
- **A weekly reminder or digest.** Still a candidate for later ([[06 Roadmap]] §2).

## Risks to watch in M6
- **Keeping drafts by clicking.** Moving a draft to `mine/insights/` without rewriting it makes Claude's words look like yours, which undoes goal G4. Rewrite before you keep.
- **Claude writing in `mine/`.** Claude may draft only in `mine/drafts/` and never changes the `status` of a page in `mine/`. The drafts routine must keep both rules.
- **Insights that drift from the wiki.** An insight links to wiki pages that lint can still change. Obsidian updates links when a page is renamed, but not when a claim is corrected.
