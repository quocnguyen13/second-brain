---
type: project-doc
project: thinking-system
status: active
trust: ai-draft
origin: claude
created: 2026-09-25
reviewed: 2026-09-25
tags: [project/thinking-system, retrospective]
---

# 21 MVP Retrospective

Back to [[00 Project Home]] · Plan in [[06 Roadmap]] · Owned by M0 – Project Management ([[07 Decision Log]] D-070)

> [!abstract] What this is
> This is the retrospective that [[09 Working Agreement]] §4 calls for at the end of a phase, covering the MVP (M0–M6). §1–§3 are the record, compiled from handovers 14–20 and `system/test-results.md`. §4–§6 are yours to fill in. §7 lists the decisions MVP 2 needs, and §8 is where the M0 thread records the outcome.

## 1. What was built
| Module | Dates | Delivered | Exit evidence |
|---|---|---|---|
| M0 – Foundation | 2026-09-16 → 19 | Documents 00–09, 13 and 14; the LLM Wiki pattern adopted | Documents accepted; D-001 to D-025 |
| M1 – Vault and Git | → 2026-09-21 | Obsidian vault, folder structure, git pushed to `second-brain`, Web Clipper | Structure matches the blueprint; first commit |
| M2 – Connect Claude Code | 2026-09-21 → 22 | Claude Code, `CLAUDE.md`, permission settings, eight templates | Setup checks and the permission smoke test pass |
| M3 – First Ingests | 2026-09-22 | The `ingest` skill; 5 sources; the wiki compiled | Source 5 updated 6 existing pages, against a bar of 3 |
| M4 – Ask and File-back | 2026-09-24 | The `ask` and `file-answer` skills; the first analysis page | Test prompts 10 of 10 |
| M5 – Lint and Review | 2026-09-24 | The `lint` skill; two review views; the weekly review | Lint tests 6 of 6; 16 fixes applied |
| M6 – Thinking Layer | 2026-09-24 → 25 | The `drafts` skill; the drafts routine; 5 insights (`origin: claude`) | Drafts tests 5 of 5 |

**Outcome:** the MVP was complete on 2026-09-25, meeting all 6 criteria in [[01 Project Charter]] §6, nine days after the first document (2026-09-16).

**The vault today:**
- 5 sources in `raw/`.
- 27 wiki pages: 19 `verified`, 7 `contested`, 1 `unverified`. One of them is an analysis page.
- 2 lint reports.
- 5 skills: `ingest`, `ask`, `file-answer`, `lint` and `drafts`.
- 5 insights, all written by Claude.
- Nothing yet in `mine/decisions/`, `mine/journal/` or `mine/scratch/`.

**The project record:** 21 of 21 tests passed. 66 decisions logged (D-001 to D-071). 42 commits.

## 2. What the system caught in itself
- **M4, test 8.** `/file-answer`'s re-check found that "Resources rank below Projects and Areas" isn't in the Forte source, although two wiki pages said it. This was the first error the system caught in itself.
- **M5, lint.** The first run reported 14 findings, and 13 were real: two misquotes of Bush, unsupported claims, and missing links. The fourteenth came from the skill's own wording and was fixed in the skill. The second run found 3 more real problems on pages the first run had passed. That led to D-060, a full deep check once a month.
- **M6, drafts.** 9 of the 11 insight drafts had problems, and every finding held against `raw/`. One draft presented Karpathy's point as its own reasoning.
- **Pattern:** the checks that open `raw/` catch what summaries miss. Every error found so far sat in Claude-written synthesis, such as drafts and claims that span pages, rather than in the sources.

## 3. Where the plan changed
| Decision | Change | Why |
|---|---|---|
| D-026 | The Obsidian curriculum was removed | Speed: steps, not lessons |
| D-030 | The documents repo was folded into the vault repo | One master copy |
| D-045 | You move each source into `raw/` | The permission rule held against Claude's shell too |
| D-062, D-068 | The insights criterion moved to M6, then was met with insights Claude wrote and you accepted | MVP first; revise before MVP 2 |
| D-069 to D-071 | The revision runs in M0, and every module thread is standing | Planning is project management; threads keep their module's context |

**What Claude observed while building.** These are for you to confirm or reject:
- **File placement.** Every change reaches the vault as files you copy, diff, commit, push and sync. M6 alone took four rounds, including this one.
- **Mirrors.** Each skill and `CLAUDE.md` is mirrored in doc 08, so every skill change is two edits in one commit.
- **The thinking layer.** `mine/` holds no page you have written yet. The five insights are Claude's, and `decisions`, `journal` and `scratch` are empty.
- **Stale files.** `system/context.md` said "M3" until M6, and Q-015 has been open since 2026-09-22.
- **The wiki.** It is about knowledge systems, not your domains. D-039 left your domains (lending, cards, payments, onboarding) to the next iteration.

## 4. What worked for you
Yours. What would you keep exactly as it is?
- 

## 5. What didn't fit how you work
Yours. Three to five things that felt slow, heavy, unnecessary or awkward, in your words.
- 

## 6. What you want the system to do for your real work
Yours. Three things, at a public level: no employer, product, team or internal detail (D-018).
- 

## 7. Decisions MVP 2 needs
Carried from [[20 M6 Handover]]:
1. The five `origin: claude` insights: rewrite them, keep them as they are, or archive them (D-068).
2. Whether D-063 stays: a kept insight means you write the page.
3. The first page in `mine/decisions/`.
4. Whether the product-owner workflows (doc 11) come into MVP 2, and which routines matter most (Q-008).
5. When doc 12 (Data Governance) is written, and your bank's AI-tools policy (Q-004). Either way, doc 12 comes before any work material (D-018).
6. The first domain sources: which of your domains the wiki should cover next (D-039).
7. The parked items: page names in `log.md`, a re-read check for decisions, the M5 leftovers, and Q-015.
8. The module references still to update: [[01 Project Charter]] §4, [[02 System Architecture]] §3, and the due dates on D-018, Q-004, Q-007 and Q-008.

## 8. Outcome
Filled in by the M0 thread: MVP 2's goal, scope and module plan, the decision IDs, and the revised docs 01 and 06.
