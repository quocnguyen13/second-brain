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

# 18 M4 Handover

Back to [[00 Project Home]] · Modules in [[06 Roadmap]] §2 · Previous: [[17 M3 Handover]]

**Module M4 – Ask and File-back · closed 2026-09-24. Next: M5 – Lint and Review.**

## What was done
- Two skills written, placed in `.claude/skills/`, and mirrored in [[08 Claude Operating Instructions]] §4.2–4.3. Both follow the `ingest` pattern: they run only when you type the command, and carry no `allowed-tools` (D-041).
  - **`/ask`** answers the question typed after the command, or else the oldest open one in `inbox/questions.md`. It searches `wiki/` as well as reading `index.md` (D-049), and traces each claim to a wiki page and then to a file in `raw/`. When the wiki has nothing, it opens with "Nothing in the wiki on this." It writes nothing but the tick in the queue (D-048).
  - **`/file-answer`** files the last answer in the session as a page in `wiki/analyses/`. It re-reads every cited passage in `raw/` first (D-050), and links the new page from the pages it drew on, for context only (D-051). It also updates `index.md` and `log.md`.
- `CLAUDE.md`'s ask section is now a pointer, plus three rules for questions asked without the command.
- The 10 test prompts were made concrete for this wiki and run: **10 of 10 passed.** Results are in `system/test-results.md`. Test 7 used a throwaway injection file instead of the contextualizer prompt (D-052).
- The first analysis page is filed: `wiki/analyses/Compare the PARA method and evergreen notes as ways to organise what I read`, `contested`, with 7 claims confirmed in `raw/`.

## What the tests taught us, and what changed because of it
| What happened | What changed |
|---|---|
| Test 4: the Read tool couldn't open PDF pages because Poppler was missing. Claude reported it and installed nothing | You installed Poppler 25.07. The no-installing behaviour is now a rule in `CLAUDE.md` and both skills (D-054, proposed). `file-answer` marks a claim it can't re-check "not re-checked", and the page `unverified` |
| Test 8: `/file-answer`'s re-check found that "PARA ranks Resources below Projects and Areas" isn't in the Forte source | The claim was kept out of the analysis's evidence. The same claim sits on `Organizing by actionability` and `Compiled wiki`, and is queued in `inbox/checks.md` for `/lint`. This is the first real error the system has caught in itself |
| Tests 3, 5 and 10: recommendations added when nobody asked, and left out when one would have helped | One rule in `CLAUDE.md` and `ask`: recommend when asked, or when there's an obvious next step (D-053, proposed) |
| Tests 3 and 5: extra sections ("Known limits"); contested pages listed under "Not in the wiki" | `ask` now has a fixed set of answer sections, with **Caveats** for status and coverage limits and "Not in the wiki" for real gaps only |
| Test 8: the `/ask` text put a wiki page where a citation goes, and the filed page left out the page behind Bush's position | `ask` forbids wiki pages as citations. `file-answer`'s Related list includes the page behind each disputed position |
| Test 10: the deletion proposal said `Reranking` cites one source; it cites two | No change. A reminder to read Claude's summaries against the page |

## Decisions made in M4
- **Accepted 2026-09-24:**
  - **D-048:** `/ask` writes nothing but the tick; asks aren't logged; only `/file-answer` adds to the wiki.
  - **D-049:** `/ask` searches `wiki/` as well as reading the index.
  - **D-050:** analysis pages cite `raw/` directly, and every cited passage is re-read before filing.
  - **D-051:** an analysis's conclusion is its own reasoning from its evidence. The pages it drew on link to it under Related.
  - **D-052:** test 7 uses a throwaway injection file. Tests run through `/ask`, and results are recorded in `system/test-results.md`.
- **Proposed, waiting for your word:**
  - **D-053:** one recommendation rule.
  - **D-054:** never install, never ask to.

## State of the vault
- **`raw/`:** 5 sources, unchanged.
- **`wiki/`:** 27 pages — 15 concepts, 5 entities, 5 source pages, `overview.md`, and 1 analysis.
  - `contested`: 7 — the 6 from M3, plus the analysis.
  - `unverified`: 1 — `Karpathy`.
- **`inbox/checks.md`:** 1 open check, the unsupported Resources ranking claim. `inbox/questions.md` is empty.
- **`mine/drafts/`:** 11 insight drafts, unchanged. M4 wrote none.
- **Tools:** Poppler 25.07 is installed, so Claude can read PDF pages.
- **Branch `main`**, in step with `origin/main` once this batch is pushed.
- **Your file, `system/context.md`:** "Current focus" still says M3. Update it yourself when convenient.

## What M5 must produce
1. The `lint` skill at `.claude/skills/lint/SKILL.md`, following the same pattern: user-invoked only, no `allowed-tools`, mirrored in doc 08 §4. It runs the standing checks in `CLAUDE.md`, works through `inbox/checks.md`, and writes `system/lint/report-<YYYY-MM-DD>.md`. It changes nothing else without your approval.
2. The two Bases views from [[05 Obsidian Essentials]] §4: **Needs attention** (`unverified` or `contested`) and **Draft queue** (`mine/drafts`). Bases is a core plugin, so D-006 is kept.
3. The weekly routine: a `/lint` run, both views, and a pass through `mine/scratch`.

**M5 is done when** a lint pass catches a contradiction and an uncited claim.

**Real cases are already in the wiki**, so, as in M4, nothing needs planting:
- **Uncited claim:** "Resources ranked below Projects and Areas" on `Organizing by actionability` (line 18) and `Compiled wiki` (line 24). It cites `raw/forte-para-method.md`, which doesn't say it. That's harder to catch than a sentence with no citation. The queued check names both pages; a good lint should also find them unprompted.
- **Contradiction between pages:** those two pages say PARA ranks Resources lower, while the analysis page says the source states no ranking.
- **General knowledge on a page:** the `Karpathy` page's full name.

## Open questions
| ID | Question | Due |
|---|---|---|
| Q-015 | Hide the synced claude.ai skills (D-040): the `skillOverrides` entry still needs the names from `~/.claude/skills/synced` | When you're next at the terminal |
| Q-008 | Which product-owner routines matter most | M7 |
| Q-004 | Your bank's AI-tools policy | M8, with doc 12 |

## Parked in M4
- A naming rule for a source with no author.
- Long analysis titles: the title is the question word for word.
- Your work-domain sources, such as Basel texts and regulator rules. Test 6 showed the gap, and doc 16 puts them after the MVP.

## Risks to watch in M5
- **Lint that fixes instead of reporting.** `CLAUDE.md` says lint changes nothing without your approval, but `wiki/` is on the allow list, so an edit wouldn't prompt. The skill has to write the report and stop, like `ingest` step 1.
- **Checking citations, not just their presence.** Every page in the wiki has citations, so a lint that only counts them will pass the Resources claim. The skill needs to open the cited passage in `raw/`, at least for the pages a check names.
- **Report volume.** 27 pages and seven checks can produce a long report. Ask for findings grouped by page, most serious first, each with a proposed fix.
- **Staleness is untestable yet.** Every page is days old, so the six-month check has nothing to find. That's expected, not a failure.
