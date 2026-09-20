---
type: project-doc
project: thinking-system
status: active
trust: working
origin: claude
created: 2026-09-19
reviewed: 2026-09-19
tags: [project/thinking-system, handover]
---

# 14 M0 Handover

Back to [[00 Project Home]] · Modules in [[06 Roadmap]] §2

**Module M0 – Foundation · closed 2026-09-19. Next: M1 – Vault and Obsidian Basics.**

## What was done
- Adopted Karpathy's LLM Wiki pattern as the foundation: three layers (`raw/`, `wiki/`, schema) and three operations (ingest, query, lint).
- Added four things on top: a thinking layer you own (`mine/`), provenance rules, an enforcement layer, and three separate input zones.
- Agreed the vault structure, page types, properties, and linking rules.
- Wrote the schema drafts: `CLAUDE.md`, permission settings, skills, and a 10-prompt test suite.
- Agreed ways of working: one chat per module, review by comment, changed files only, a stage marker on every reply.
- Produced documents 00–09, 13, and 14, plus an interactive structure diagram.

## Decisions carried into M1
- D-001 to D-025, all accepted. D-004 and D-005 are superseded by D-019 and D-020.
- Bank data governance is parked as doc 12 (D-018). Until it exists, one rule stands: **personal and public sources only.**
- Notes in English by default. No migration assumed. Phone capture deferred to M8.

## State of the vault
Nothing is built yet. Obsidian is not installed, and the vault does not exist. M1 starts from an empty machine.

## What M1 must produce
1. Obsidian installed; vault `Second-Brain` created at `C:\Users\<you>\Vaults\Second-Brain`, outside OneDrive.
2. The folder structure from [[04 Vault Blueprint]] §1, including the three zones in `inbox/`.
3. Git initialised in the vault, with `.gitignore` and a first commit.
4. This document set placed in `mine/projects/thinking-system/`.
5. Learning Path Stages 0–2 complete.

**M1 is done when** you can navigate the vault without the mouse, every project document opens through its links, and the local graph makes sense to you.

## Open questions
| ID | Question | Due |
|---|---|---|
| Q-013 | Your first five sources. The LLM Wiki gist is source 1; four more are yours. | Start of M3 |
| Q-008 | Which product-owner routines matter most | M7 |
| Q-004 | Your bank's AI-tools policy | M8, with doc 12 |

## Risks to watch in M1
- Building folders that don't match the blueprint, which would break the permission rules later. Check §1 of [[04 Vault Blueprint]] as you go.
- Installing community plugins early. Core plugins only until the MVP is done (D-006).
