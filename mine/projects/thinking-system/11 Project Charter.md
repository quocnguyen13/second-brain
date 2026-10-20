---
type: project-doc
project: thinking-system
status: active
trust: working
origin: claude
created: 2026-09-16
reviewed: 2026-10-20
tags: [project/thinking-system]
---

# 11 Project Charter

Back to [[00 Project Home]]

## 1. Vision
> [!note] Superseded as the product vision by [[10 Product Vision]] (D-076). Kept as MVP 1's starting point.

A knowledge base that compounds. I collect sources and ask good questions; Claude compiles what I read into a linked, maintained wiki; and my own conclusions live in a layer I own. Nothing useful disappears into chat history, and Claude always has my context.

## 2. Problem
- Chat conversations are short-lived, so insights get lost or have to be worked out again.
- Uploading files to an assistant re-derives the same understanding on every question. Nothing accumulates.
- Claude's general knowledge doesn't include my products, my domain, or my past decisions.
- Notes kept by hand fall out of date, because the bookkeeping is the tedious part and it never gets done.

## 3. The bet
The LLM does the bookkeeping: summarizing, cross-referencing, filing, flagging contradictions. I do the sourcing, the questions, and the judgment. See [[30 System Architecture]].

## 4. MVP
**The MVP is the working loop:** ingest a source → the wiki updates itself → ask a question → get an answer with citations → file the good answers back → lint keeps it healthy.

**In scope**
- One vault on the Windows PC, in git, holding `raw/`, `wiki/`, and `mine/`
- Claude Code running inside it, with the schema file, conventions, and permission settings
- The three operations: ingest, query, lint
- `index.md` and `log.md`, maintained by Claude
- A thinking layer I own, for insights and decisions
- Enough Obsidian to read, review, and search the vault ([[70 Obsidian Essentials]])

**Out of scope for the MVP**
- **Bank data governance (parked as doc 36).** The MVP takes personal and public sources only, so the rules aren't needed yet. They get written before any work material enters the vault.
- Running any of this on a bank device or against bank systems
- Product-owner workflows (now jobs and standards, MVP 3: [[10 Product Vision]] §4.1)
- Sync, phone capture, semantic search, custom tooling

## 5. Goals
| ID | Goal | Measure |
|---|---|---|
| G1 | **Compounding:** each new source makes the wiki better, not just bigger | A single ingest updates several existing pages, not only one new one |
| G2 | **Grounded:** answers come from my wiki with citations back to sources | Test prompts pass; every wiki claim traces to a source in `raw/` |
| G3 | **Honest:** the wiki shows contradictions and gaps instead of hiding them | Lint finds planted contradictions and uncited claims |
| G4 | **Mine:** my conclusions are recorded in a layer Claude cannot rewrite | Insight and decision pages accumulate in `mine/` |
| G5 | **Checkable:** I can verify any claim in the wiki in under a minute | I trace a claim from a wiki page to its file in `raw/` |

## 6. Success criteria for the MVP
- 5 sources ingested; `index.md` and `log.md` current.
- An ingest of source 5 updates at least 3 existing pages.
- 10 test prompts: at least 9 answered from the wiki with correct citations ([[40 Claude Operating Instructions]] §5).
- One query answer filed back as an analysis page.
- One lint pass that finds a planted contradiction and a planted uncited claim.
- At least 5 insight pages written or accepted by me in `mine/`.

## 7. Owner profile
- Product Owner at a commercial bank
- Setup: personal Windows PC, Claude Pro, comfortable with the terminal, more than 6 hours a week
- Still to confirm: note language(s), notes to migrate, phone capture (Q-005 to Q-007 in [[03 Decision Log]])

## 8. Principles
1. **I own the sources and the conclusions; Claude owns the compilation.**
2. **Everything cites something.** A claim with no source is marked unverified.
3. **Plain Markdown in git.** No lock-in, and every change can be undone.
4. **Start manual, then automate.** Learn the vault by using it before handing over the bookkeeping.
5. **Minimal tooling.** Core Obsidian features first.
6. **Personal and public sources only, until doc 36 exists.**

## 9. Constraints
- Claude Pro covers Claude Code, but usage limits are shared with claude.ai, so a large batch ingest can eat the day's allowance.
- Claude Code changes weekly; check its documentation before each build step.
- The wiki is only as good as the sources I feed it.

## 10. Risks
| Risk | Mitigation |
|---|---|
| The wiki becomes confidently wrong | Citation rule, unverified status, lint, git diffs ([[31 Trust and Provenance]]) |
| Claude's own summaries get treated as evidence | Wiki pages cite `raw/`, never other wiki pages, as their source of fact |
| I stop reading what Claude writes | One review per set, with conflicts and the weakest facts first, and nothing compiled before I answer the brief (D-085, D-086); weekly lint |
| Bank material drifts into the vault before the rules exist | One standing rule in [[31 Trust and Provenance]] §4 until doc 36 is written |
| Claude edits or deletes the wrong thing | Permission rules, manual approval outside the allowed paths, git history |
| Usage limits run out mid-task | Sets of up to 8 files; a stopped set resumes from its set review (D-086); check `/usage` |

## 11. MVP 2 · Research assistant
Scope accepted 2026-09-30 ([[03 Decision Log]] D-084). Where it sits among the milestones: [[10 Product Vision]] §4.1. Modules: [[21 Roadmap]] §2.

**Status, 2026-10-20:** M7 – Batch Ingest and Trust closed 2026-10-06 ([[88 M7 Handover]]), M8 – Research and Import on 2026-10-14 ([[89 M8 Handover]]) and M9 – Large Documents on 2026-10-20 ([[90 M9 Handover]]). Done: B-003, B-004, B-006, B-007, B-008, B-011, B-024, B-025, B-037, B-038; B-009 holds 18 raw files, the whole FSMA 2000 among them. Criteria 1 to 4 are met.

**Exit, run in M0** (D-117): criterion 6, the regression, on 21–22 October; criterion 5, the side-by-side, on 23 October; then the retrospective and the showcase gate on 26 October ([[21 Roadmap]] §13).

**Goal:** research a topic in one pass, with trust-ranked, verified facts, so an answer from the vault beats a default Claude answer (D-083).

**In scope** ([[22 Product Backlog]])
- **Must:** B-003 Claude's research as a source · B-004 research summary with sources · B-006 ingest a set · B-007 trust levels · B-008 conflict review · B-009 the UK financial system as the test set · B-024 one move per set · B-037 `/import` · B-038 large documents
- **Should:** B-011 page names in `log.md` · B-025 Claude commits after your review
- **Could:** B-015 the five Claude-written insights · B-023 Q-015 · B-026 docs straight into the vault · B-027 no skill mirrors in doc 40

**Out of scope:** jobs and standards (MVP 3); Office files and work material (MVP 4); the showcase, decided at the gate (D-082); everything else in the backlog.

**Success criteria**
1. **Research:** a new topic returns a summary in which every fact names its source, plus a list of primary sources to clip. **Met 2026-10-14** (tests RS1–RS4): a report on the Financial Ombudsman Service, every fact with its source and a quote; three quotes traced; seven sources clipped and compiled; `/ask` made no web call.
2. **Import:** `/import` flags a planted duplicate and a planted new version. **Met 2026-10-12** (tests IM1–IM4); IM5–IM6 also loaded the capture list and two typed links, one approval each.
3. **Batch ingest:** 5 or more sources on one topic compiled in one run with one review. The review lists conflicts first, then facts sorted by trust. **Met 2026-10-06** (tests I3–I5): 5 sources, 18 pages new, 10 updated, 58 facts, 3 conflicts decided.
4. **Large documents:** a document of several hundred pages compiled in parts, with progress tracked and every citation pointing to its page or section. **Met 2026-10-20** (tests LD3–LD6): the whole FSMA 2000, 1,263 pages, mapped into 49 Parts and 36 Schedules; Parts II, 4A and XVI compiled and Part 1A compared, across four sessions; all 522 citations into the Act carry a page.
5. **Side-by-side:** 5 questions on the UK set, asked through `/ask` and in a default Claude chat. Every fact in the `/ask` answers traces to `raw/`, with its trust level. The questions sit on compiled parts and `verified` pages, chosen with the FSMA map open: a question in a part not compiled tests LD8's behaviour, not the fact guarantee. On 23 October.
6. **Regression:** the 21 MVP 1 tests still pass, so `/ingest`, `/ask`, `/file-answer` and `/lint` keep working. The ingest tests passed again in M7 (I1, I2); all 21 are rerun at MVP 2's exit, since M7, M8 and M9 changed `ingest`, `import`, `ask`, `file-answer`, `lint`, `drafts` and `CLAUDE.md`. On 21–22 October.

**Risks**
| Risk | Mitigation |
|---|---|
| A set or a large document uses up the day's Pro allowance mid-run | The set review records progress, so the next `/ingest` resumes a stopped set (D-086). A large document runs one part of about 60 pages per session, with `/clear` between runs (D-108). Tested in M9 (LD5): a run stopped after a chunk was written and before it was ticked; the next `/ingest` resumed it and added nothing twice. Since then a chunk is marked `started` before it is written (D-116). `/usage` wasn't recorded per run, so the 60-page cap is still an estimate |
| A faster review means you read less of what Claude writes | Conflicts and low-trust facts come first, and the checks that open `raw/` stay ([[10 Product Vision]] §6, principle 7). The set of five listed 58 facts, 41 of them primary and folded. Lint then found errors the set reviews had passed, 6 after M7 and 5 after M8, so `/ingest` now recommends `/lint` after a large set (D-103) |
| Trust levels become Claude's opinion of a source | Levels set by type of source in doc 31, not by judgement, and you can override one |
| Claude's research is treated as evidence | D-075: a claim marked `· AI` stays uncited, and its page `unverified`, until a primary source backs it (D-087). Tested in M8: asked to mark a page resting on AI claims `verified`, Claude declined and listed the claims (AI3). An unbacked claim goes on an existing page only when it is about that page's subject (D-102) |
