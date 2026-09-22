---
type: project-doc
project: thinking-system
status: active
trust: ai-draft
origin: claude
created: 2026-09-22
reviewed: 2026-09-22
tags: [project/thinking-system, handover]
---

# 16 M2 Handover

Back to [[00 Project Home]] · Modules in [[06 Roadmap]] §2 · Previous: [[15 M1 Handover]]

**Module M2 – Connect Claude Code · closed 2026-09-22. Next: M3 – First Ingests.**

## What was done
- Claude Code facts were rechecked against the current docs before anything was built. Four findings shaped the settings:
  - Pro sessions now start in auto mode unless a settings file turns it off.
  - With Git for Windows installed, Claude Code has both a Bash tool and a PowerShell tool.
  - Rule paths starting with `/` anchor at the folder Claude Code is started in.
  - Writes to `.claude/` and `.git/` always ask, whatever the allow rules say.
- Claude Code 2.1.278 installed with the native installer at `C:\Users\Admin\.local\bin\claude.exe`. It updates itself. No `ANTHROPIC_API_KEY` at session, user or machine level. Signed in with your claude.ai account on Pro.
- Schema files live in the vault, mirrored in [[08 Claude Operating Instructions]]:
  - `CLAUDE.md` (54 lines), importing `system/context.md` and `system/conventions.md`
  - `.claude/settings.json`: Manual mode, auto and bypass modes off, auto memory off, 7 allow rules, 8 deny rules, claude.ai connectors off, the synced `data` plugin off
  - `index.md` and `log.md`, empty apart from headings
  - Eight page templates in `system/templates/`, described in [[10 Templates]]
- `system/context.md` filled in by you: your domains, and reading interests for the first sources.
- First session checks passed: 3 memory files loaded, `⏸ manual mode on`, auto memory off, rules as expected, `/mcp` empty, `claude doctor` clean.
- The permission smoke test passed:
  - an edit to `inbox/checks.md` went through without a prompt
  - an edit to `system/context.md` asked first
  - a write to `raw/` was blocked

## Decisions made in M2
All accepted on 2026-09-22.
- **D-031:** PowerShell versions of the `git clean` and `git reset` deny rules.
- **D-032:** Claude's edit rights in `inbox/` cover only `questions.md` and `checks.md`.
- **D-033:** M2 closes on the setup checks and the smoke test; the gist ingest moves to M3.
- **D-034:** One template per page type in `system/templates/`; Claude reads a template before creating a page.
- **D-035:** Native installer, not WinGet.
- **D-036:** claude.ai connectors are off for vault sessions.
- **D-037:** The synced `data` plugin is off for vault sessions.
- **D-038:** When a permission rule blocks an action, Claude stops and tells you, and doesn't look for another way.

## State of the vault
- Branch `main`. After you commit and push this batch, it's in step with `origin/main`.
- `raw/`, `wiki/` and the zone queues are empty. No skills exist yet; `.claude/skills/` is created in M3.
- Your "don't ask again" approvals, if any, sit in `.claude/settings.local.json`, which git ignores.
- The other skills synced from your claude.ai account, such as `pdf` and `xlsx`, still load in vault sessions (Q-015).
- [[10 Templates]] is still `ai-draft`, waiting for your review.

## What M3 must produce
1. **Q-013 answered first:** the first five sources. Source 1 is the LLM Wiki gist; the reading interests in `system/context.md` point to the other four.
2. **The `ingest` skill** at `.claude/skills/ingest/SKILL.md`, following [[13 Input Zones]] §2 and the ingest steps in `CLAUDE.md`. Once it exists, the ingest section of `CLAUDE.md` shrinks to a pointer (D-012). Settle Q-015 at the same time.
3. **Five sources ingested one at a time** (D-022), starting with the gist. That means `wiki/` populated, `wiki/overview.md` written, and `index.md` and `log.md` live.

**M3 is done when** ingesting source 5 updates at least 3 existing pages, and you've traced one claim back to its file in `raw/`.

## Open questions
| ID | Question | Due |
|---|---|---|
| Q-013 | Your first five sources. The LLM Wiki gist is source 1; four more are yours. | Start of M3 |
| Q-015 | Keep the remaining synced skills in vault sessions, or switch some off? | Start of M3 |
| Q-008 | Which product-owner routines matter most | M7 |
| Q-004 | Your bank's AI-tools policy | M8, with doc 12 |

## Risks to watch in M3
- **Moving a source into `raw/`.** The deny rule on `raw/` might also block Claude's `mv` command. If it does, move the file yourself with `Move-Item`, or drag it in Obsidian, and tell Claude the final path. That keeps `raw/` just as safe. Test it on the first ingest.
- **Skill files sit in `.claude/`.** That folder always asks before a write, and Claude in these Project chats can't write there at all. The skill file gets created inside a vault session, with your approval, or moved in by you the way the settings file was.
- **Skipping the review.** One ingest can touch ten pages. Check each ingest as in [[05 Obsidian Essentials]] §3 before the next one.
- **Synced items coming back.** A plugin or connector you turn on at claude.ai later syncs into vault sessions. Run `/mcp` and `claude plugin list` at the start of each module.
