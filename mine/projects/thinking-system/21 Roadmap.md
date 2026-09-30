---
type: project-doc
project: thinking-system
status: active
trust: working
origin: claude
created: 2026-09-16
reviewed: 2026-09-30
tags: [project/thinking-system, roadmap]
---

# 21 Roadmap

Back to [[00 Project Home]] · MVP defined in [[11 Project Charter]] §4

> [!note] Milestones are set in [[10 Product Vision]] §4.1. MVP 2's scope and success criteria are in [[11 Project Charter]] §11 (D-084); its modules are below.

## 1. Shape of the plan
```mermaid
%%{init: {"flowchart": {"curve": "step", "useMaxWidth": true, "nodeSpacing": 12, "rankSpacing": 25, "padding": 8, "subGraphTitleMargin": {"top": 4, "bottom": 8}}}}%%
flowchart TD
    subgraph LEG["Legend · status"]
        direction TB
        L1["Done"]:::done
        L2["Next"]:::next
        L3["Planned"]:::plan
    end
    V1["MVP 1 · M0 to M6<br/>closed 2026-09-25"]:::done
    PM["M0 · Retrospective<br/>and MVP 2 scope"]:::done
    M7["M7 · Batch ingest<br/>and trust"]:::next
    M8["M8 · Research<br/>and import"]:::plan
    M9["M9 · Large<br/>documents"]:::plan
    G["M0 · Retrospective<br/>and showcase gate"]:::plan
    V1 --> PM --> M7 --> M8 --> M9
    M9 -- "MVP 2 complete" --> G
    classDef done fill:#dbeafe,stroke:#1d4ed8,color:#1e3a8a
    classDef next fill:#fef3c7,stroke:#b45309,color:#78350f
    classDef plan fill:#dcfce7,stroke:#15803d,color:#14532d
```

## 2. Modules
One standing thread per module ([[02 Working Agreement]] §4, D-071). After its exit, a module's thread stays open to maintain what it built; that work doesn't reopen its row here. Estimates assume more than 6 hours a week, with no curriculum in the path (D-026).

| Module | Goal | Main outputs | Done when | Estimate |
|---|---|---|---|---|
| **M0 – Project Management** (standing, D-070) | First: agree the pattern, scope and ways of working (Foundation). Since then: keep the scope, plan and decisions current | Documents 00, 02, 03, 11, 21, 30–33, 40, 70 and 80; the handovers; doc 87 | **Foundation closed 2026-09-19.** Standing since 2026-09-25 | Done, then ongoing |
| **M1 – Vault and Git** | A vault built to the blueprint | Obsidian installed and configured; folders from [[32 Vault Blueprint]] §1 including the three `inbox/` zones; git initialised with a first commit; Web Clipper pointed at `inbox/sources/`; documents placed in `mine/projects/thinking-system/` | **Closed 2026-09-21** | Done |
| **M2 – Connect Claude Code** | Claude runs inside the vault under the rules | Claude Code installed; `CLAUDE.md`, `system/conventions.md`, `system/context.md`, permission settings; the page templates and doc 34 (Templates) | **Closed 2026-09-22** | Done |
| **M3 – First Ingests** | The compile loop works | The `ingest` skill and its zone contract ([[33 Input Zones]]); 5 sources in `raw/`, starting with the LLM Wiki gist; `wiki/` populated; `index.md` and `log.md` live | **Closed 2026-09-22** | Done |
| **M4 – Ask and File-back** | Answers are grounded and reusable | The `ask` and `file-answer` skills; 10 test prompts and recorded results | **Closed 2026-09-24** | Done |
| **M5 – Lint and Review** | The wiki stays honest as it grows | The `lint` skill; the two Bases views; the weekly routine | A lint pass catches a contradiction and an uncited claim, using the real cases M4 found (D-059); lint tests 6 of 6 | **Closed 2026-09-24** |
| **MVP complete** | | | All criteria in [[11 Project Charter]] §6 met. 5 of 6 at M5's close; the insights criterion is met in M6 (D-062, D-068) | **Met 2026-09-25: 6 of 6** |
| **M6 – Thinking Layer** | Your own conclusions accumulate | `mine/insights` in use (`mine/decisions` moved to the revision, D-068); the drafts routine and the `drafts` skill (D-063 to D-067) | 5 insight pages you accepted, linked to wiki pages (D-068); drafts tests 5 of 5 | **Closed 2026-09-25** |
| **M0 · Retrospective and MVP 2 scope** | Fit the system to how you work, and scope MVP 2 (D-069, D-070) | Doc 87 (MVP Retrospective) completed; docs 11 and 21 revised for MVP 2; decisions on the items carried from M6 | You accept MVP 2's scope and module plan | **Closed 2026-09-30** (D-084) |
| **M7 – Batch Ingest and Trust** | A topic comes in as a set: one run, one review, facts ranked by trust, conflicts resolved | Must: B-006 set ingest, B-007 trust levels (rule in doc 31 §2), B-008 conflict review (doc 31 §3), B-024 one move per set, tested on B-009 (the UK financial system). Should: B-011, B-025. Takes over the `ingest` skill from M3 | 5 or more sources on one topic compiled in one run with one review, conflicts first and facts sorted by trust; the MVP 1 ingest tests still pass | About 1 week |
| **M8 – Research and Import** | Claude researches for you, and nothing enters twice | Must: B-004 research summary with sources, B-003 Claude's research as a source (D-075), B-037 `/import` | A new topic returns a summary in which every fact names its source, plus sources to clip; `/import` flags a planted duplicate and a planted new version | About 1 week |
| **M9 – Large Documents** | A 1,000-page book or a full Act can be compiled | Must: B-038 | A document of several hundred pages, such as the full FSMA 2000, compiled in parts across sessions, with progress tracked and every citation pointing to its page or section | About 1 week |
| **MVP 2 complete** | | | All six criteria in [[11 Project Charter]] §11, including the side-by-side test against a default Claude chat (D-083). Then the retrospective and the showcase gate in M0 (D-082) | |

**Not in MVP 2:** everything else waits in [[22 Product Backlog]] with a proposed milestone. Work material and bank devices stay out until doc 36 exists (D-018, B-022).

## 3. M0 closed on 2026-09-19
- [x] Documents 00, 02, 03, 11, 21, 30–33, 40 and 70 accepted
- [x] Decisions D-001 to D-025 accepted
- [x] Q-005 to Q-007 settled or deferred; Q-013 (first sources) moves to the start of M3
- [x] Handover written: [[80 M0 Handover]]
- [x] Documents moved to a private GitHub repo synced into project knowledge (D-028)
- [x] M1 run; Q-014 decided at its close (D-030)

## 4. M1 closed on 2026-09-21
- [x] Obsidian installed and configured per [[70 Obsidian Essentials]] §1
- [x] Folder structure matches [[32 Vault Blueprint]] §1, including the three `inbox/` zones and `mine/scratch/` (D-029)
- [x] Git initialised with `.gitignore` and `.gitattributes`; first commit made
- [x] Web Clipper saving to `inbox/sources/`
- [x] Documents in `mine/projects/thinking-system/`, opening through their links
- [x] Q-014 decided: the vault repo is the single source of truth, pushed to the private repo `second-brain`; the documents repo is archived (D-030)
- [x] Handover written: [[81 M1 Handover]]
- [x] Next: M2 – Connect Claude Code, started 2026-09-21

## 5. M2 closed on 2026-09-22
- [x] Tool facts rechecked against the Claude Code docs (2026-09-21); D-031 to D-035 proposed
- [x] Vault checked against [[32 Vault Blueprint]] §1: every folder and zone file in place
- [x] Schema files placed in the vault: `CLAUDE.md`, `.claude/settings.json`, `system/context.md`, `system/conventions.md`, `index.md`, `log.md`
- [x] Eight templates in `system/templates/`; [[34 Templates]] written
- [x] D-031 to D-038 accepted
- [x] `system/context.md` filled in by you
- [x] Claude Code 2.1.278 installed with the native installer; no API key set ([[40 Claude Operating Instructions]] §6 steps 1–2)
- [x] Schema files committed and pushed (step 3)
- [x] First run: signed in, trust prompt accepted; `/context` loads 3 memory files
- [x] Connectors switched off (D-036); auto memory off and permission rules as expected
- [x] `data` plugin switched off (D-037); `/mcp` empty; `claude doctor` clean (steps 4–6)
- [x] Permission smoke test passes (step 7); a workaround offer after the `raw/` block led to D-038
- [x] Handover written: [[82 M2 Handover]]
- [x] Next: M3 – First Ingests, started 2026-09-22

## 6. M3 closed on 2026-09-22
- [x] Tool facts rechecked against the Claude Code docs (skills, permissions, settings scopes, tools); D-040 to D-044 proposed
- [x] `ingest` skill drafted, mirrored in [[40 Claude Operating Instructions]] §4.1; `CLAUDE.md` ingest section cut to a pointer (D-041)
- [x] Overview page type and template added (D-044)
- [x] D-040 to D-044 accepted
- [ ] Q-015 settled: synced skills hidden in vault sessions; `/skills` shows only the vault's and Claude Code's own (D-040)
- [x] Skill moved into `.claude/skills/ingest/SKILL.md`, committed and pushed; `/ingest` appears after a restart
- [x] Source 1 ingested: Karpathy, LLM Wiki gist, committed 2026-09-22. The move into `raw/` was blocked, so you moved it (D-045)
- [x] Skill revised after source 1: a page citing one source can be `verified`; links checked before the report; the move check uses file tools; the move is yours (D-045)
- [x] Source 2 ingested: Bush, "As We May Think", from MIT's full-text PDF after the first clip was only page 1 of 4. The review added the links to source 1 that the ingest missed
- [x] Skill revised after source 2: ground rules, a search of `wiki/` and `raw/` for every new source, PDF page citations (D-046), partial-clip check
- [x] Source 3 ingested: Matuschak, "Evergreen notes" — the hub page only, so the five principles are recorded as titles and the 15 linked notes as gaps
- [x] Source 4 ingested: Anthropic, "Introducing Contextual Retrieval" — the disagreement with source 1 recorded on both sides; D-047 narrows which pages carry `contested`, accepted the same day
- [x] Source 5 ingested: Forte, "The PARA Method", updating 6 existing pages, 3 of them with new cited claims, against a bar of 3 (D-044). A second disagreement recorded on both sides
- [x] Each ingest reviewed as in [[70 Obsidian Essentials]] §3 and committed before the next
- [x] One claim traced from a wiki page to its file in `raw/`: `Associative indexing` → Bush on cumbersome rules → `raw/bush-as-we-may-think.pdf` page 14
- [x] Handover written: [[83 M3 Handover]]
- [x] Next: M4 – Ask and File-back, started 2026-09-24

**Parked in M3, to pick up after the MVP unless they start to hurt:**
- Matuschak's five principle notes and the Zettelkasten sources. The gaps are recorded in `wiki/overview.md` and on [[03 Decision Log]]'s next-sources list, so nothing is lost.
- The `ingest` report splitting "updated" into pages that gained a claim and pages that only gained a link.
- D-040's `skillOverrides` entry, which waits for the list of names in `~/.claude/skills/synced`.

## 7. M4 closed on 2026-09-24
- [x] `ask` and `file-answer` skills written, mirrored in [[40 Claude Operating Instructions]] §4.2–4.3; the ask section of `CLAUDE.md` cut to a pointer plus the rules for direct questions
- [x] Test prompts made concrete for this wiki ([[40 Claude Operating Instructions]] §5); `system/test-results.md` and `test-injection.md` written
- [x] D-048 to D-052 accepted
- [x] Skills moved into `.claude/skills/ask/` and `.claude/skills/file-answer/`, committed and pushed; both appear in `/skills`
- [x] Tests 1–6 run and recorded. Test 4 found Poppler missing; you installed it, and Claude installed nothing
- [x] Test 7 run with `test-injection.md`; the file deleted afterwards
- [x] Test 8 run: `Compare the PARA method and evergreen notes as ways to organise what I read` filed in `wiki/analyses/`, reviewed and committed. Its re-check caught an unsupported claim, now in `inbox/checks.md`
- [x] Tests 9 and 10 run: **10 of 10**
- [x] Fix batch from the test findings: answer sections, recommendation rule (D-053), no installing (D-054), unreadable raw files, Related links. No rerun needed
- [x] Handover written: [[84 M4 Handover]]
- [x] Next: M5 – Lint and Review, started 2026-09-24

**Parked in M4, to pick up when they start to hurt:**
- A naming rule for a source with no author (test 7 produced `unknown-...`).
- Analysis page titles are the question word for word, which can be long.

## 8. M5 closed on 2026-09-24
- [x] D-053 and D-054 accepted
- [x] `lint` skill drafted and mirrored in [[40 Claude Operating Instructions]] §4.4; the lint section of `CLAUDE.md` cut to a pointer, and two citation rules added (D-055 to D-057)
- [x] `system/views/Review.base` drafted with both views (D-058), mirrored in [[70 Obsidian Essentials]] §6
- [x] Weekly review written as steps in [[70 Obsidian Essentials]] §4
- [x] Lint tests L1–L6 written in [[40 Claude Operating Instructions]] §5 and `system/test-results.md` (D-059)
- [x] D-055 to D-059 accepted
- [x] Files placed: the skill in `.claude/skills/lint/`, `Review.base` in `system/views/` and bookmarked; committed and pushed
- [x] Views checked: Needs attention shows 8 pages (1 `unverified`, 7 `contested`); Draft queue shows 11
- [x] L1–L4: first `/lint`, report read and committed. 14 findings; 13 confirmed against `raw/`, and finding 5 was the skill's own error, fixed in `lint` and `file-answer`
- [x] L5: `/lint apply` for all findings but 5: exactly those 13 fixes, no status changes, reviewed and committed
- [x] L6: second `/lint` in a fresh session: 13 pages deep-checked, none of the applied findings back, finding 5 gone, and 3 new real problems found. **Lint tests 6 of 6; M5's exit criterion is met**
- [x] D-060 (monthly full deep check) and D-061 (wrong PDF page is Low) accepted; `lint` revised to match
- [x] Fixes from report-2026-09-24-2 applied and committed: 3 findings, 8 pages, no status changes
- [x] Weekly review steps 1–3 run twice (lint, apply, commit); steps 4–7, including the first pass through the draft queue, move to M6
- [x] MVP criteria in [[11 Project Charter]] §6 checked: 5 of 6, with the insights criterion moved to M6 (D-062)
- [x] Handover written: [[85 M5 Handover]]
- [x] Next: M6 – Thinking Layer, started 2026-09-24

**Parked in M5, to pick up when they start to hurt:**
- A written rule for uncited lines that only restate cited claims (lint currently reads them as synthesis).
- Checking `mine/drafts/` claims against `raw/` before you keep one; M6 decides. Proposed in M6 as the `drafts` skill (D-064).

## 9. M6 closed on 2026-09-25
- [x] D-062 accepted: the MVP's insights criterion is met at M6's close
- [x] Drafts routine written: keep means you write a new page, and no draft waits a week (D-063); weekly review step 5 rewritten in [[70 Obsidian Essentials]] §4
- [x] `drafts` skill drafted and mirrored in [[40 Claude Operating Instructions]] §4.5; `CLAUDE.md` gets its pointer (D-064)
- [x] Insight page rules: `origin`, `status`, `reviewed` and how Relations read (D-065); `mine/decisions/` versus doc 03 (D-066); drafts from `ingest` cite `raw/` (D-067). Insight template, `system/conventions.md`, `Review.base` and docs 30, 31, 32, 70 and 34 updated to match
- [x] Drafts tests R1–R5 written in [[40 Claude Operating Instructions]] §5 and `system/test-results.md`
- [x] D-063 to D-067 accepted (2026-09-25)
- [x] Files placed: `drafts` skill in `.claude/skills/drafts/`, `ingest` skill replaced, the rest copied over; committed and pushed (75f7537); `/skills` lists `drafts`
- [x] R1–R4: first `/drafts` on the 11 drafts, committed (45526e4). **4 of 4.** 2 clean, 9 with problems; every finding checked against `raw/` and holds, including five beyond the expected ones (`system/test-results.md`)
- [x] D-068 accepted: the five MVP insights are written by Claude from the checked drafts and accepted by you
- [x] 5 insights placed in `mine/insights/`, each with Relations linking `wiki/`, and all 11 drafts deleted (1b6beb3). That completes the first cycle through the Draft queue
- [ ] Weekly review steps 4, 6 and 7: not run in M6. Nothing waited on them (no new lint report, `mine/scratch/` empty); the first full weekly review is next week
- [x] R5: second `/drafts` in a fresh session (a7fb417). **Drafts tests 5 of 5; M6's exit criterion is met**
- [x] `system/context.md` "Current focus" updated (your file, 70cf510)
- [x] MVP criteria in [[11 Project Charter]] §6 checked: **6 of 6. MVP complete, 2026-09-25**
- [x] Q-016 answered: the revision comes next, in the M0 thread (D-069, D-070); every module thread is standing (D-071)
- [x] Handover written: [[86 M6 Handover]]
- [ ] **Next:** in the M0 thread, the retrospective and MVP 2 scope (D-070), starting from doc 87

**Carried to the revision in M0 (D-068, D-070):**
- The five insights are `origin: claude`. Rewrite them, keep them as they are, or archive them.
- The first decision page in `mine/decisions/`.
- Two drafts that weren't kept: `The schema doc is the highest-leverage part of this vault to get right` (its Check was clean) and `Per-source review beats batch ingest for this vault`. Git keeps both.
