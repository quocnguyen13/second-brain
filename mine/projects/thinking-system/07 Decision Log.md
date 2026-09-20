---
type: project-doc
project: thinking-system
status: active
trust: working
origin: claude
created: 2026-09-16
reviewed: 2026-09-19
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
| D-011 | Manual permission mode; auto and bypass modes disabled | **Accepted 2026-09-19** | You approve everything outside the allowed paths |
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
| **D-022** | Sources are ingested one at a time, with you reading the result, at least through M3 | **Accepted 2026-09-19** | Karpathy's own preference, and how you learn what good output looks like |

**Superseded:** D-004 (Claude writes only to an AI-drafts folder) and D-005 (PARA structure) are replaced by D-019 and D-020. D-007 (no automatic saving) still holds: operations run when you ask. D-009 (hyphenated folder names) and D-016 (templates early) are folded into [[04 Vault Blueprint]] and module M2.

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

## Plugin and MCP register
| Name | Type | Why it's needed | Source | Date added |
|---|---|---|---|---|
| (none yet) | | | | |
