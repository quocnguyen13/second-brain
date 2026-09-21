---
type: project-doc
project: thinking-system
status: active
trust: ai-draft
origin: claude
created: 2026-09-21
reviewed: 2026-09-21
tags: [project/thinking-system, handover]
---

# 15 M1 Handover

Back to [[00 Project Home]] · Modules in [[06 Roadmap]] §2 · Previous: [[14 M0 Handover]]

**Module M1 – Vault and Git · closed 2026-09-21. Next: M2 – Connect Claude Code.**

## What was done
- Obsidian installed (1.13.7). Vault `Second-Brain` at `C:\Users\Admin\Vaults\Second-Brain`, outside OneDrive. Documents on this PC is redirected into OneDrive, so nothing vault-related goes there.
- Obsidian set up per [[05 Obsidian Essentials]] §1: links update automatically, new notes go to `mine/scratch`, attachments to `raw/assets`, core plugins on with Sync, Publish and Canvas off, daily notes to `mine/journal`, templates folder `system/templates`.
- Folder structure per [[04 Vault Blueprint]] §1, including the three `inbox/` zones and `mine/scratch/`. Empty folders hold a `.gitkeep` so git keeps them.
- Git for Windows installed. The vault is a git repo with `.gitignore` and `.gitattributes`, committed, and pushed to the private GitHub repo `second-brain`.
- Web Clipper saves to `inbox/sources/`.
- Project documents live in `mine/projects/thinking-system/`; project knowledge syncs that folder only. The old documents repo is archived.

## Decisions made in M1
- D-026 (curriculum removed) and D-027 (G5 narrowed to verification) accepted.
- D-028 (separate documents repo) accepted, then superseded by D-030 the same day.
- **D-029:** your own new notes go to `mine/scratch/`; `mine/drafts/` holds only Claude's insight drafts.
- **D-030:** the vault repo is the single source of truth.

## State of the vault
- Branch `main`, in step with `origin/main` on GitHub.
- Not yet created, all due in M2: `CLAUDE.md`, `.claude/`, `index.md`, `log.md`, `system/context.md`, `system/conventions.md`.
- `raw/`, `wiki/` and the zone queues are empty.

## Document workflow from now on
Claude delivers changed files → you drop them into `mine/projects/thinking-system/` → read `git diff` → commit → `git push` → Sync in the Project.

## What M2 must produce
1. Claude Code installed, with no `ANTHROPIC_API_KEY` set.
2. `CLAUDE.md`, `.claude/settings.json`, `system/context.md`, `system/conventions.md`, and empty `index.md` and `log.md`, committed and pushed.
3. Doc 10 (Templates).

**M2 is done when** the setup checks in [[08 Claude Operating Instructions]] §6 pass.

## Open questions
| ID | Question | Due |
|---|---|---|
| Q-013 | Your first five sources. The LLM Wiki gist is source 1; four more are yours. | Start of M3 |
| Q-008 | Which product-owner routines matter most | M7 |
| Q-004 | Your bank's AI-tools policy | M8, with doc 12 |

## Risks to watch in M2
- **An elevated terminal.** Your Windows account is named Admin. Start Claude Code from a normal terminal, never one opened with "Run as administrator".
- **Permission paths that don't match the folders.** The rules in [[08 Claude Operating Instructions]] §3 use exact paths; compare them with [[04 Vault Blueprint]] §1 before the first session.
- **The repo's visibility.** `second-brain` holds the whole vault. Keep it private, and give the Claude GitHub app access to that repo only.
- **Slashes.** `\` in PowerShell, `/` inside Obsidian, Markdown and Claude Code's permission rules.
