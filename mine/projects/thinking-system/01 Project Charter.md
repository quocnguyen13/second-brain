---
type: project-doc
project: thinking-system
status: active
trust: working
origin: claude
created: 2026-09-16
reviewed: 2026-09-19
tags: [project/thinking-system]
---

# 01 Project Charter

Back to [[00 Project Home]]

## 1. Vision
A knowledge base that compounds. I collect sources and ask good questions; Claude compiles what I read into a linked, maintained wiki; and my own conclusions live in a layer I own. Nothing useful disappears into chat history, and Claude always has my context.

## 2. Problem
- Chat conversations are short-lived, so insights get lost or have to be worked out again.
- Uploading files to an assistant re-derives the same understanding on every question. Nothing accumulates.
- Claude's general knowledge doesn't include my products, my domain, or my past decisions.
- Notes kept by hand fall out of date, because the bookkeeping is the tedious part and it never gets done.

## 3. The bet
The LLM does the bookkeeping: summarizing, cross-referencing, filing, flagging contradictions. I do the sourcing, the questions, and the judgment. See [[02 System Architecture]].

## 4. MVP
**The MVP is the working loop:** ingest a source → the wiki updates itself → ask a question → get an answer with citations → file the good answers back → lint keeps it healthy.

**In scope**
- One vault on the Windows PC, in git, holding `raw/`, `wiki/`, and `mine/`
- Claude Code running inside it, with the schema file, conventions, and permission settings
- The three operations: ingest, query, lint
- `index.md` and `log.md`, maintained by Claude
- A thinking layer I own, for insights and decisions
- Enough Obsidian skill to read, navigate, and write in the vault

**Out of scope for the MVP**
- **Bank data governance (parked as doc 12).** The MVP takes personal and public sources only, so the rules aren't needed yet. They get written before any work material enters the vault.
- Running any of this on a bank device or against bank systems
- Product-owner workflows (module M7, after the MVP)
- Sync, phone capture, semantic search, custom tooling

## 5. Goals
| ID | Goal | Measure |
|---|---|---|
| G1 | **Compounding:** each new source makes the wiki better, not just bigger | A single ingest updates several existing pages, not only one new one |
| G2 | **Grounded:** answers come from my wiki with citations back to sources | Test prompts pass; every wiki claim traces to a source in `raw/` |
| G3 | **Honest:** the wiki shows contradictions and gaps instead of hiding them | Lint finds planted contradictions and uncited claims |
| G4 | **Mine:** my conclusions are recorded in a layer Claude cannot rewrite | Insight and decision pages accumulate in `mine/` |
| G5 | **Fluent:** I can navigate and extend the vault without Claude | Learning Path Stages 0–4 complete |

## 6. Success criteria for the MVP
- 5 sources ingested; `index.md` and `log.md` current.
- An ingest of source 5 updates at least 3 existing pages.
- 10 test prompts: at least 9 answered from the wiki with correct citations ([[08 Claude Operating Instructions]] §5).
- One query answer filed back as an analysis page.
- One lint pass that finds a planted contradiction and a planted uncited claim.
- At least 5 insight pages written or accepted by me in `mine/`.

## 7. Owner profile
- Product Owner at a commercial bank
- Setup: personal Windows PC, Claude Pro, comfortable with the terminal, more than 6 hours a week
- Still to confirm: note language(s), notes to migrate, phone capture (Q-005 to Q-007 in [[07 Decision Log]])

## 8. Principles
1. **I own the sources and the conclusions; Claude owns the compilation.**
2. **Everything cites something.** A claim with no source is marked unverified.
3. **Plain Markdown in git.** No lock-in, and every change can be undone.
4. **Start manual, then automate.** Learn the vault by using it before handing over the bookkeeping.
5. **Minimal tooling.** Core Obsidian features first.
6. **Personal and public sources only, until doc 12 exists.**

## 9. Constraints
- Claude Pro covers Claude Code, but usage limits are shared with claude.ai, so a large batch ingest can eat the day's allowance.
- Claude Code changes weekly; check its documentation before each build step.
- The wiki is only as good as the sources I feed it.

## 10. Risks
| Risk | Mitigation |
|---|---|
| The wiki becomes confidently wrong | Citation rule, unverified status, lint, git diffs ([[03 Trust and Provenance]]) |
| Claude's own summaries get treated as evidence | Wiki pages cite `raw/`, never other wiki pages, as their source of fact |
| I stop reading what Claude writes | Ingest one source at a time and stay involved; weekly lint |
| Bank material drifts into the vault before the rules exist | One standing rule in [[03 Trust and Provenance]] §4 until doc 12 is written |
| Claude edits or deletes the wrong thing | Permission rules, manual approval outside the allowed paths, git history |
| Usage limits run out mid-task | Ingest sources singly; check `/usage` |
