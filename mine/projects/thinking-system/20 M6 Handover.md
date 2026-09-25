---
type: project-doc
project: thinking-system
status: active
trust: ai-draft
origin: claude
created: 2026-09-25
reviewed: 2026-09-25
tags: [project/thinking-system, handover]
---

# 20 M6 Handover

Back to [[00 Project Home]] · Modules in [[06 Roadmap]] §2 · Previous: [[19 M5 Handover]]

**Module M6 – Thinking Layer · closed 2026-09-25. The MVP is complete, 6 of 6. Next: the retrospective and MVP 2 scope, in the M0 – Project Management thread.** This thread stays open to maintain the thinking layer (D-071).

## What was done
- **The drafts routine** (D-063), in [[05 Obsidian Essentials]] §4 step 5. Every draft is kept or deleted at the review where you meet it. Keeping one means writing a new page in `mine/insights/`; a draft never moves there.
- **The `drafts` skill** (D-064), at `.claude/skills/drafts/SKILL.md` and mirrored in [[08 Claude Operating Instructions]] §4.5. `/drafts` checks each draft against `raw/` and writes a Check section and a `checked` date into it. It also lists your insights whose linked wiki pages changed after their `reviewed` date. It writes only in `mine/drafts/` and `log.md`.
- **Rules for insight pages** (D-065): what `origin`, `status` and `reviewed` mean, and how a Relations line reads. **`mine/decisions/` and doc 07 separated** (D-066). **Drafts from `ingest` cite `raw/`** (D-067).
- **Drafts tests R1–R5 passed, 5 of 5**, on the 11 real drafts with nothing planted. Results are in `system/test-results.md`.
- **Five insights placed in `mine/insights/`** (D-068). Claude wrote them from the checked drafts, merging 9 of the 11 and fixing what the Checks found, and you accepted them. They carry `origin: claude`. All 11 drafts are deleted; git keeps them at `45526e4`.
- **Q-016 answered** (D-069, D-070): the revision you want before MVP 2 comes next, in the M0 thread, which is now M0 – Project Management. Every module thread is standing (D-071).

## What the tests taught us, and what changed because of it
| What happened | What changed |
|---|---|
| 7 of the 11 drafts cited nothing in `raw/`, and two labelled their own reasoning "(general knowledge)" | D-067: `ingest` drafts now cite `raw/` inline and mark reasoning "(reasoning)" |
| The first `/drafts` found problems in 9 of 11 drafts. Claude checked every finding against `raw/` and all of them held, including five beyond the expected ones | No change. Checking drafts before keeping them is worth the run |
| The Memex draft called its main point "not a claim either source makes", but Karpathy makes it (`raw/karpathy-llm-wiki.md` line 81) | No change. The Check's "Reasoning, not in a source" list is what exposed it; the insight now credits Karpathy |
| Two drafts presented one side of a dispute as settled: "exact match first" where Anthropic says combine, and a layer split that Forte doesn't accept | Both insights say so plainly |
| R5 listed the right insight but couldn't say which operation changed each page, because `lint apply` logs page counts, not page names | Parked: have `lint apply` and `ingest` name the pages they change in `log.md` |
| R5 noticed a `reviewed` date earlier than `created`, and an uncommitted edit, and changed nothing | No change. This is the behaviour D-064 wants |
| Obsidian rewrote the Epics insight's properties in its own style (unquoted dates, `related` as a list) when you edited them | No change. Harmless, as with `Review.base` in M5 |
| You chose to finish the MVP first and write the insights later, if at all | D-068: the five MVP insights are Claude's, marked `origin: claude`. The revision in M0 decides what happens to them |

## Decisions made in M6
All accepted.
- **D-062:** the MVP's last criterion is met in M6.
- **D-063:** the drafts routine: keep means write a new page; unsure means delete.
- **D-064:** the `drafts` skill checks, and you decide.
- **D-065:** insight pages: `origin`, `status`, `reviewed`, and how Relations read.
- **D-066:** decisions about the system go in doc 07; your own go in `mine/decisions/`.
- **D-067:** `ingest` drafts cite `raw/`.
- **D-068:** the five MVP insights are Claude's, accepted by you.
- **D-069:** the revision comes next. **D-070:** it runs in the M0 thread, now M0 – Project Management. **D-071:** every module thread is standing.

## State of the vault
- **`raw/`:** 5 sources, unchanged since M3.
- **`wiki/`:** 27 pages, unchanged in M6: 19 `verified`, 7 `contested`, and 1 `unverified` (`Karpathy`).
- **`mine/insights/`:** 5 pages, `origin: claude`, `status: active`, each with Relations linking `wiki/`.
- **`mine/drafts/`:** empty. **`mine/decisions/`, `mine/journal/`, `mine/scratch/`:** empty.
- **Skills:** `ingest`, `ask`, `file-answer`, `lint` and `drafts`.
- **`log.md`:** the last entry is the R5 run of `/drafts`.
- **Branch `main`:** at `a7fb417` before this closing commit.
- **Your file, `system/context.md`:** "Current focus" says M6. Change it when the M0 work starts.

## MVP status ([[01 Project Charter]] §6)
| Criterion | Status |
|---|---|
| 5 sources ingested; `index.md` and `log.md` current | Met (M3) |
| Source 5 updates at least 3 existing pages | Met (M3) |
| 10 test prompts, at least 9 answered from the wiki with correct citations | Met: 10 of 10 (M4) |
| One answer filed back as an analysis page | Met (M4) |
| One lint pass finds a contradiction and an uncited claim | Met: L1–L2 (M5) |
| At least 5 insight pages written or accepted by you in `mine/` | Met: 5 accepted (M6, D-068) |

**6 of 6. The MVP is complete as of 2026-09-25.**

## What the M0 work must produce
From [[06 Roadmap]] §2, D-069 and D-070. It starts from [[21 MVP Retrospective]], whose record sections are already filled:
1. **A retrospective of M0–M6:** what worked, what didn't fit how you work, and what to drop, completed in doc 21. [[09 Working Agreement]] §4 asks for one at the end of each phase.
2. **A revised scope for MVP 2:** docs 01 (Charter) and 06 (Roadmap) rewritten, with a module plan from M7 onward. The candidates are product-owner workflows, doc 12, and whatever the retrospective finds.
3. **Decisions on the items carried from M6:**
   - the five `origin: claude` insights: rewrite them, keep them as they are, or archive them;
   - whether D-063 (you write every kept insight) stays;
   - the first page in `mine/decisions/`;
   - the parked items below.
4. **Old module references updated** once the plan is set: [[01 Project Charter]] §4, [[02 System Architecture]] §3, and the M7 and M8 due dates on D-018, Q-004, Q-007 and Q-008 in [[07 Decision Log]].

**The work is done when** you accept MVP 2's scope and module plan, and doc 21 is complete.

**Bring to the M0 thread:** three to five things that felt slow, heavy or unnecessary while building, and three things you want the system to do for your real work. Keep them at a public level: no employer, product or internal detail (D-018).

## Open questions
| ID | Question | Due |
|---|---|---|
| Q-015 | Hide the synced claude.ai skills (D-040): the `skillOverrides` entry still needs the names from `~/.claude/skills/synced` | When you're next at the terminal |
| Q-008 | Which product-owner routines matter most | M0, with the MVP 2 scope |
| Q-004 | Your bank's AI-tools policy | Before doc 12; M0 sets when |

## Parked in M6
- **Page names in `log.md`.** `lint apply` and `ingest` log page counts, so `/drafts` can't say which operation changed a page an insight links to.
- **A re-read check for decision pages.** `reviewed` and the re-read list cover insights only.
- **Two drafts not kept:** `The schema doc is the highest-leverage part of this vault to get right` (its Check was clean) and `Per-source review beats batch ingest for this vault`. Both are in git at `45526e4`.
- **Still parked from M5:**
  - A rule for uncited lines that restate cited claims.
  - The sources lint suggested: Luhmann on the Zettelkasten, Matuschak's associative-ontologies note, and Forte's book chapter on PARA.
  - A weekly reminder.

## Risks to watch in the M0 work
- **Revising without evidence.** The system has run for a week. Tie each change to something the retrospective found, not to a new idea of what it could do.
- **Work material creeping in.** Tailoring the system to product-owner work pulls toward real work material. Doc 12 comes first (D-018).
- **Claude's words becoming yours by default.** The five insights read as yours over time. The `origin: claude` label only helps if someone checks it, which is why the revision decides their fate.
