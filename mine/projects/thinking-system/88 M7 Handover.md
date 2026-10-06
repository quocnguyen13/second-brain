---
type: project-doc
project: thinking-system
status: active
trust: ai-draft
origin: claude
created: 2026-10-06
reviewed: 2026-10-06
tags: [project/thinking-system, handover]
---

# 88 M7 Handover

Back to [[00 Project Home]] · Modules in [[21 Roadmap]] §2 · Previous: [[86 M6 Handover]] and [[87 MVP Retrospective]]

**Module M7 – Batch Ingest and Trust · closed 2026-10-06. Tests I1–I7: 7 of 7. Next: M8 – Research and Import.** This thread stays open to maintain the `ingest` skill, trust levels and the conflict review (D-071).

## What was done
- **`/ingest` takes a set** (D-085). Every file in `inbox/sources/`, or the ones you name, up to 8: one brief, one move block, one run, one review. A set of one runs as MVP 1's ingest did. D-022's one source per run ended with this module.
- **The set review** (D-086). One file per set in `system/ingest/`: conflicts first, then facts sorted by trust with the weakest first and primary facts folded, then one claim per level to trace. It also records progress so a stopped run can resume.
- **Trust levels** (D-087). Primary, secondary, commentary and AI, set by source type; `trust` on every source page; a marker on every citation below primary. Rule in [[31 Trust and Provenance]] §2.1, live copy in `system/conventions.md`.
- **Conflicts: Claude proposes, you decide** (D-088, D-094). Four kinds: fact, newer, scope, view. For facts the proposal goes by level, then a body's own statement about itself, then date. `/ingest resolve 1a 2d` applies your letters; the claim set aside stays on the page, marked.
- **Fewer steps.** One move block per set (D-089). Claude commits after your review, with `git commit` always asking and `git push` denied to Claude (D-090). Log entries name the pages they change (D-091).
- **Other skills brought into line.** `/ask` gives each fact's level; `/lint` checks markers and treats a resolved dispute as settled; `/file-answer` and `/drafts` keep markers and commit the same way.
- **The UK set** (B-009). Seven sources on how the FCA and the PRA regulate firms are compiled: FSMA Part 1A, the FCA's own page, the PRA's approach to banking supervision, the FCA–Bank of England MoU, the Bank's prudential regulation page, a Commons Library briefing and Wikipedia's article on the FCA.

**For five sources, your steps fell from 15 to 4:** clip the set, paste the move block and say what to emphasise, read one review and decide the conflicts, push.

## What the tests taught us, and what changed because of it
| What happened | What changed |
|---|---|
| I1: a source page cited another source's raw file in a conflict note without listing it in `sources` | The skill: a page that cites another raw file lists it, and its index count follows |
| I1: the run moved the disputed claim out of the page's opening line and under "Where sources disagree", against the skill, and said so | The skill now says the same: an open dispute sits only there, with a pointer where it stood |
| I1: after the resolve, notes on source pages and the overview still said "waiting for your decision" | `resolve` updates them |
| I1: ingest and resolve were committed together, since nothing was committed in between | The skill says so |
| I3: the run stopped a set of five public sources because Wikipedia names a person in a prosecution the FCA announced | D-093: no personal-data flag. The stop for confidential work material, customer data included, stays |
| I3: the last pasted line of the move block waited for Enter, so one file moved late. The run held until it arrived | The skill tells you to press Enter |
| I4: the run used a script to rewrite lines in `index.md`, which left Windows line endings, and reported it | Ground rule: vault files change through Edit or Write only |
| I1, I5: the FCA's page gives the PRA about 1,500 firms, the PRA's own page about 1,292. Date picked the right one only because the PRA's page was newer | D-094: at the same level, a body's own statement about itself comes before date |
| I3: the brief noticed Wikipedia's 58,000 firms rests on a 2010 article that predates the FCA | No change. Reading a source's own citations made the conflict easy to decide |
| I1: the brief found a conflict nobody predicted, the FCA "established" in 2013 against the FSA renamed | No change. The search of `wiki/` and `raw/` before writing is what finds these |
| I4: 82 PDF pages and two clips compiled in one Pro session without stopping | No change. The resume path stayed untested; see Parked |

## Decisions made in M7
All accepted.
- **D-085:** `/ingest` takes a set. **D-086:** the set review. **D-087:** trust levels. **D-088:** conflicts: Claude proposes, you decide.
- **D-089:** one move for the set. **D-090:** Claude commits after your review. **D-091:** page names in `log.md`. **D-092:** the test set and tests I1–I7.
- **D-093:** no personal-data flag; the confidentiality stop stays.
- **D-094:** at the same level, a body's own statement about itself is proposed before the newer source.
- **D-022** (one source per run) is replaced by D-085. **D-008** (commit after every session) is revised by D-090.

## State of the vault
- **`raw/`:** 12 sources: 5 on knowledge systems, 7 on UK regulation.
- **`wiki/`:** 57 pages: 12 source pages, 13 entities, 30 concepts, 1 analysis and the overview. 48 `verified`, 7 `contested` (all from MVP 1's two disagreements of view) and 2 `unverified` (`Karpathy`, `Solo and dual regulation`).
- **`system/ingest/`:** 2 set reviews, both `done`: `set-2026-10-06` (1 source, 1 conflict, resolved c) and `set-2026-10-06-2` (5 sources, 3 conflicts, resolved 1a 2a 3a).
- **`mine/drafts/`:** 6 drafts, none checked yet. **`mine/insights/`:** 5, unchanged.
- **Skills:** `ingest` (reworked), `ask`, `file-answer`, `lint`, `drafts`. **Settings:** 8 allow, 2 ask and 10 deny rules.
- **`log.md`:** the last entry is the resolve of `set-2026-10-06-2`.
- **Branch `main`:** e8f4340 (opening files), 473c5e1 (set of one), d15b457 (D-093), 3e474a7 (set of five). The last two weren't pushed when this was written.
- **Named person.** `Source - Wikipedia on the FCA` names the person charged in the WealthTek case, as Wikipedia does. D-093 allows it; the `Financial Conduct Authority` page mentions the case without the name.
- **Your file, `system/context.md`:** "Current focus" says M7. Change it when M8 opens.

## MVP 2 status ([[11 Project Charter]] §11)
| Criterion | Status |
|---|---|
| 1. Research: a summary in which every fact names its source, plus sources to clip | M8 |
| 2. Import: `/import` flags a planted duplicate and a planted new version | M8 |
| 3. Batch ingest: 5 or more sources in one run with one review, conflicts first, facts by trust | **Met** (I3–I5, 2026-10-06) |
| 4. Large documents compiled in parts, with progress tracked | M9 |
| 5. Side-by-side: 5 questions through `/ask` and a default Claude chat | At MVP 2's exit. I7 is a first sign: `/ask` gave the FCA's own figure with its level |
| 6. Regression: the 21 MVP 1 tests still pass | Ingest part met (I1, I2). `ask`, `file-answer`, `lint` and `drafts` changed in M7, so the other 19 are rerun at MVP 2's exit |

## What M8 must produce
From [[21 Roadmap]] §2 and D-084:
1. **B-004, a research summary with sources:** a new topic returns a summary in which every fact names its source, plus the primary sources for you to clip.
2. **B-003, Claude's research as a source** (D-075): a Claude output goes through `/ingest`, verified claim by claim, with unbacked claims marked `· AI` and counted as uncited.
3. **B-037, `/import`:** new files are checked against `raw/` for duplicates and newer versions before ingest.

**M8 is done when** a new topic returns such a summary plus sources to clip, and `/import` flags a planted duplicate and a planted new version.

**What M7 leaves ready for it**
- The `ai` level and the `· AI` marker exist (D-087), and `/ingest` leaves Claude outputs out of a set until M8 builds their path.
- Raw names carry a year for dated documents (D-089), which `/import` can use to spot versions.
- A real test file is waiting: `mine/projects/uk-financial-system/claude-2026-09-27-foundations-1-1-who-regulates-what.md`, a Claude research output on the topic the wiki now covers from primary sources.

**To settle in M8:** where the capture list lives between sessions; whether web search gets an allow rule or asks each time, since it is the first operation that reaches outside the vault; a size limit for research reports; how "similar" is measured for `/import`, and whether it is its own command or step 0 of `/ingest`.

**Opening brief for the M8 thread**
```
Module: M8 – Research and Import
Goal: Claude researches for you, and nothing enters twice (21 Roadmap §2)
Handover: 88 M7 Handover
Read first: 11 §11; 21 §2; 22 items B-004, B-003, B-037; 31 §2.1 and §3; 33 §2; 40 §4.1; 03 D-075, D-083, D-087, D-093
Time available this week:
```

## Request for M0
```
M0 · Project Management · request from M7
What: bring the as-built descriptions up to date with set ingest and trust levels:
  10 §2.2 (N1) and §4.2 (E-02), 11 §10 and §11 (criterion 3 met), 20 §3.1 (US-02), §5.0, §5.1 and §8, 30 §5.
  In 02 §4, move 33, 32 §5–6 and 70 §3 from M3's row to M7's. D-076 is still Proposed.
Why: D-084, D-085 to D-094; M7 closed 2026-10-06
Read first: 88 M7 Handover; 40 §4.1
Done when: no project document says one source per run, and 02 §4 matches who maintains what
```

## Parked in M7
- **Resuming a stopped set** (D-086) is built but untested, because the set compiled in one session. M9's large documents will exercise it.
- **The first `/lint` since M7** hasn't run. It will deep-check about 30 changed pages, and it is the first use of the trust-level check. Run it before M8 adds more.
- **Six drafts wait for `/drafts`:** three from the FSMA ingest, one from I1, two from the set of five.
- **`Claude outputs/` at the vault root** isn't in the blueprint. It holds a copy of doc 10 and `test-injection.md`, a file written to mislead Claude; better deleted now the test is done.
- **"Co-Authored-By" in commit messages.** Claude Code adds it to the commits it makes. The `attribution.commit` setting changes or hides it (Claude Code settings reference, checked 2026-10-06).
- **Still parked from earlier modules:** Q-015 (synced skills), a weekly reminder, the sources lint suggested in M5.

## Risks to watch in M8
- **Claude's research treated as evidence.** D-075 holds only if a `· AI` claim stays uncited until a primary source backs it. Test that an AI-only page can't become `verified`.
- **A long review read too fast.** The set of five listed 58 facts; the 41 primary ones sit folded. Errors would hide there, and `/lint` is the backstop, so it should run after every large set.
- **Reaching outside the vault.** Research needs web search. Decide its permission on purpose (D-036, D-043), and keep fetched pages out of `raw/`.
- **The skill is getting long.** `ingest` is 230 lines. The AI path may be better as its own skill, or a supporting file, than as more of this one.
