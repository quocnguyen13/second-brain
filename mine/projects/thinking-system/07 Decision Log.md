---
type: project-doc
project: thinking-system
status: active
trust: working
origin: claude
created: 2026-09-16
reviewed: 2026-09-22
tags: [project/thinking-system, decisions]
---

# 07 Decision Log

Back to [[00 Project Home]]

## Decisions
Accepted on 2026-09-19 unless marked otherwise. New proposals wait for your word.

| ID | Decision | Status | Reasoning |
|---|---|---|---|
| D-001 | The vault is a local folder of plain Markdown, edited in Obsidian and tracked in git | **Accepted 2026-09-19** | No lock-in; every change reviewable and reversible |
| D-002 | The MVP runs on a personal Windows PC with personal and public sources only | **Accepted 2026-09-19** | Makes parking governance safe ([[03 Trust and Provenance]] §4) |
| D-003 | Claude Code, started inside the vault, is the main tool. Cowork is optional; community MCP servers are not used. | **Accepted 2026-09-19** | Terminal comfort; enforced permission rules; skills and git |
| D-006 | Core Obsidian plugins only through the MVP; any community plugin needs a recorded reason | **Accepted 2026-09-19** | Less risk and less to learn |
| D-008 | Commit after every Claude session | **Accepted 2026-09-19** | Git diff is the review tool and the undo button |
| D-010 | Claude Code's auto memory is off; the vault is the only memory | **Accepted 2026-09-19** | One reviewable store |
| D-011 | Manual permission mode; auto and bypass modes disabled | **Accepted 2026-09-19** | You approve everything outside the allowed paths. Checked 2026-09-21: on Pro, sessions now start in auto mode unless a settings file disables it, so `disableAutoMode` is what keeps you in Manual |
| D-012 | Always-on rules in `CLAUDE.md` (under 200 lines); procedures in skills | **Accepted 2026-09-19** | Claude Code's own guidance; keeps context small |
| D-013 | Install Git for Windows before Claude Code | **Accepted 2026-09-19** | Needed for D-008; gives Claude Code its Bash tool |
| D-014 | Collaboration follows [[09 Working Agreement]] | **Accepted 2026-09-19** | Comment in chat; Claude sends only changed files |
| D-015 | One chat per module, with a handover between modules | **Accepted 2026-09-19** | Keeps chats focused |
| **D-017** | **Adopt the LLM Wiki pattern as the foundation:** three layers (`raw/`, `wiki/`, schema) and three operations (ingest, query, lint) | **Accepted 2026-09-19** | Proven pattern, well matched to this goal; we build on it rather than inventing one ([[02 System Architecture]]) |
| **D-018** | **Bank data governance is parked** as doc 12, to be written in M8 or before any work material enters the vault, whichever comes first | **Accepted 2026-09-19** | Nothing confidential in the MVP means nothing to govern yet |
| **D-019** | Replace the PARA folder scheme with `raw/`, `wiki/`, `mine/`, `system/` | **Accepted 2026-09-19** | Matches the adopted pattern; fewer concepts to learn |
| **D-020** | Claude owns `wiki/` and may create and update pages there, plus `index.md` and `log.md`, without asking each time. `mine/` stays yours, with drafts only in `mine/drafts/`. `raw/` is read-only to Claude. | **Accepted 2026-09-19**, supersedes D-004 and D-005 | Compiling is the whole point; your conclusions stay yours ([[08 Claude Operating Instructions]] §3) |
| **D-021** | Every wiki page cites sources in `raw/`; a wiki page never cites another wiki page as evidence | **Accepted 2026-09-19** | Stops Claude's summaries becoming their own evidence |
| **D-023** | Each operation has its own input zone: `inbox/sources/` for `/ingest`, `inbox/questions.md` for `/ask`, `inbox/checks.md` for `/lint`. A command reads only its own zone and never re-routes misfiled material. | **Accepted 2026-09-19** | Keeps the three operations from mixing ([[13 Input Zones]]) |
| **D-024** | The draft queue is renamed `mine/drafts/`, so "inbox" means the input zones and nothing else | **Accepted 2026-09-19** | Two folders called inbox would be confusing from day one |
| **D-025** | All three operations run as Claude Code commands in a vault session. No plugins, scripts, or separate apps. | **Accepted 2026-09-19** | Your preference for Claude as the platform; one place to learn |
| **D-026** | **The Obsidian curriculum is removed.** Doc 05 becomes a one-page reference; no stages, lessons, or exercises. Skills are picked up inside the modules. | **Accepted 2026-09-21** | Speed. Under the adopted pattern Claude writes the wiki, so hand-authoring practice isn't on the critical path |
| **D-027** | Goal G5 changes from "fluent in Obsidian" to "able to verify any wiki claim against its source" | **Accepted 2026-09-21** | The review loop is what keeps the wiki honest; general tool fluency isn't |
| **D-028** | The project documents live in a private GitHub repo, synced into this Project's knowledge. The repo is the master copy: Claude sends changed files, you commit, push, and click Sync. | **Accepted 2026-09-21** (you set it up), superseded by D-030 the same day | No re-uploading between modules; history and rollback for free |
| **D-022** | Sources are ingested one at a time, with you reading the result, at least through M3 | **Accepted 2026-09-19** | Karpathy's own preference, and how you learn what good output looks like |
| **D-029** | Your own new notes go to `mine/scratch/`. `mine/drafts/` holds only Claude's insight drafts. | **Accepted 2026-09-20** | `mine/drafts/` is on Claude's allow list, so your rough notes stay outside it and G4 is enforced by the permission rules; the draft queue stays unmixed ([[04 Vault Blueprint]] §1) |
| **D-030** | **The vault repo is the single source of truth.** It is pushed to the private GitHub repo `second-brain`; project knowledge syncs only `mine/projects/thinking-system/` from it. The separate documents repo is archived. | **Accepted 2026-09-21**, supersedes D-028 | One master copy, so documents can't drift between two repos; the push also gives the vault an off-site backup ([[09 Working Agreement]] §2) |
| **D-031** | Every shell deny rule has a PowerShell twin: `PowerShell(git clean *)` and `PowerShell(git reset *)` join `PowerShell(Remove-Item *)` | **Accepted 2026-09-22** | With Git for Windows installed, Claude Code has a Bash tool and a PowerShell tool, and PowerShell is on by default for claude.ai accounts. A `Bash(...)` rule doesn't catch the same command run through PowerShell ([[08 Claude Operating Instructions]] §3) |
| **D-032** | Claude's edit rights in `inbox/` narrow from the whole folder to the two queue files, `inbox/questions.md` and `inbox/checks.md` | **Accepted 2026-09-22** | A captured source can't be changed before it reaches `raw/`, so immutability starts at capture rather than at ingest. Cost: when Claude fetches a link into `inbox/sources/`, you approve that one file ([[13 Input Zones]] §2) |
| **D-033** | M2 closes when the setup checks and a three-part permission smoke test pass. Ingesting the LLM Wiki gist moves to M3, where it is already source 1. | **Accepted 2026-09-22** | Doc 08 §6 listed the ingest as an M2 step, while the roadmap puts it in M3 with the `ingest` skill. The smoke test proves the rules hold before any real content goes in ([[08 Claude Operating Instructions]] §6) |
| **D-034** | One template per page type, in `system/templates/`, named `<Type> template`. Claude reads the wiki templates before creating a page; the `mine/` templates are yours. The files are the source of truth; doc 10 describes them. | **Accepted 2026-09-22** | Delivers D-016. The names can't collide with a wiki page called "Concept" or "Decision", and the templates hold no wikilinks, so no ghost links ([[10 Templates]]) |
| **D-035** | Install Claude Code with the native PowerShell installer, not WinGet | **Accepted 2026-09-22** | The native install updates itself in the background; a WinGet install doesn't, so it would drift behind on fixes. Behaviour can change with updates, which is why tool facts get rechecked ([[09 Working Agreement]] §5) |
| **D-036** | Claude.ai connectors are switched off for vault sessions (`disableClaudeAiConnectors: true` in `.claude/settings.json`) | **Accepted 2026-09-22** | Signed in with your claude.ai account, Claude Code loads your claude.ai connectors automatically. Connected, they would let a vault session read mail and cloud files that sit outside the vault and outside the personal-and-public boundary ([[03 Trust and Provenance]] §4). The vault stays the only thing Claude reads, in line with D-003 |
| **D-037** | The `data` plugin synced from your claude.ai account is switched off for vault sessions (`"enabledPlugins": {"data@synced": false}` in `.claude/settings.json`) | **Accepted 2026-09-22** | It brings 8 MCP servers for analytics tools (Amplitude, Atlassian, BigQuery, Hex and others) and 10 skills into every vault session. None has a job in the vault; the servers are ways out of it, and D-025 keeps the operations free of plugins. The setting applies to this project only; the plugin stays on everywhere else |
| **D-038** | New standing rule in `CLAUDE.md`: if a permission rule blocks an action, Claude stops and tells you, and never looks for another way to do it | **Accepted 2026-09-22** | In the M2 smoke test the `raw/` block held, but Claude then offered to try again. Offering a workaround invites approving one by habit. Test 7 in M4 checks the same instinct ([[08 Claude Operating Instructions]] §2, §5) |

**Superseded:** D-004 (Claude writes only to an AI-drafts folder) and D-005 (PARA structure) are replaced by D-019 and D-020. D-028 (a separate documents repo) is replaced by D-030. D-007 (no automatic saving) still holds: operations run when you ask. D-009 (hyphenated folder names) is folded into [[04 Vault Blueprint]]; D-016 (templates early) is delivered in M2 by [[10 Templates]] (D-034).

## Open questions
| ID | Question | Why it matters | Answer |
|---|---|---|---|
| Q-001 | Operating system | Tool availability | **Windows, personal PC** |
| Q-002 | Claude plan | Claude Code access; shared usage limits | **Pro** |
| Q-003 | Terminal comfort | Tool choice | **Comfortable** |
| Q-004 | Bank AI-tools policy | Needed for doc 12 in M8 | Deferred with D-018 |
| Q-005 | Note language(s)? | Page titles, search, how Claude writes | **English by default**, set 2026-09-19; say the word to change it |
| Q-006 | Existing notes to migrate? | They'd become sources in `raw/` | None assumed; anything you find later just goes in `inbox/sources/` |
| Q-007 | Phone capture needed? | A later sync decision | Deferred to M8 |
| Q-010 | Time per week | Estimates | **More than 6 hours** |
| Q-011 | Review method | Document loop | **Comments in chat** |
| Q-012 | Session style | Chat structure | **One chat per module** |
| **Q-013** | **What are the first 5 sources?** The LLM Wiki gist is source 1; four more are yours | Module M3 needs them, and they set the wiki's first shape | Open, due at the start of M3 |
| **Q-014** | Once M1 creates the vault repo, does it replace the separate documents repo? | Two repos holding the same documents will drift apart | **Yes**, decided 2026-09-21 (D-030). Project knowledge syncs `mine/projects/thinking-system/` from the private repo `second-brain`; the documents repo is archived |
| **Q-015** | Keep the skills synced from your claude.ai account in vault sessions? 38 loaded at first run; the 10 from the `data` plugin go with D-037, the rest (such as `pdf` and `xlsx`) remain | They cost little context, but they're procedures the vault didn't define; `pdf` may help ingest PDF sources | Open, due at the start of M3, when the `ingest` skill is written |

## Plugin and MCP register
| Name | Type | Why it's needed | Source | Date added |
|---|---|---|---|---|
| claude.ai connectors | MCP | None; switched off for vault sessions (D-036) | Your claude.ai account | Not added |
| `data` plugin (8 MCP servers, 10 skills) | Plugin | None; switched off for vault sessions (D-037) | Synced from your claude.ai account | Not added |
