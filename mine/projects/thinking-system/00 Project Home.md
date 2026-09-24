---
type: moc
project: thinking-system
status: active
trust: working
origin: claude
created: 2026-09-16
reviewed: 2026-09-24
tags: [project/thinking-system, moc]
---

# Thinking System: Project Home

> [!abstract] What this is
> A personal knowledge base built on the **LLM Wiki** pattern: you collect sources, Claude compiles and maintains a linked wiki from them, and you read it in Obsidian. On top of that foundation we add a thinking layer you own, provenance rules, and product-owner workflows.

**Setup:** personal Windows PC · Claude Pro · Claude Code running inside the vault
**Current module:** M4 – Ask and File-back, started 2026-09-24 (see [[06 Roadmap]] §7)

## Document set

| # | Document | Purpose | Status |
|---|---|---|---|
| 00 | [[00 Project Home]] | Map of the project (you are here) | Draft |
| 01 | [[01 Project Charter]] | Why, what, MVP scope, success criteria | **Accepted** |
| 02 | [[02 System Architecture]] | The three layers, the three operations, and what we add on top | **Accepted** |
| 03 | [[03 Trust and Provenance]] | Citation rules, verified and unverified claims, what is parked | **Accepted** |
| 04 | [[04 Vault Blueprint]] | Folders, page types, properties, index and log formats | **Accepted** |
| 05 | [[05 Obsidian Essentials]] | The one page of Obsidian this system needs | **Accepted** |
| 06 | [[06 Roadmap]] | MVP definition, phases, modules M0–M8 | **Accepted** |
| 07 | [[07 Decision Log]] | Decisions made and questions still open | Living document |
| 08 | [[08 Claude Operating Instructions]] | The schema file, permission settings, skills, and tests | **Accepted** |
| 09 | [[09 Working Agreement]] | How you and Claude work together on this project | **Accepted** |
| 10 | [[10 Templates]] | One template per page type, in `system/templates/` | Draft |
| 13 | [[13 Input Zones]] | One input door per operation, all triggered inside Claude | **Accepted** |
| 14 | [[14 M0 Handover]] | Closing state of M0, used to open the M1 chat | Closed |
| 15 | [[15 M1 Handover]] | Closing state of M1, used to open the M2 chat | Closed |
| 16 | [[16 M2 Handover]] | Closing state of M2, used to open the M3 chat | Closed |
| 17 | [[17 M3 Handover]] | Closing state of M3, to open the M4 chat with | Current |

**Planned (not written yet)**
- 11 Workflow Playbook (module M7): product-owner routines
- 12 Data Governance (parked, before any work material enters the vault)

## Reading order
1. [[09 Working Agreement]]: how we work together.
2. [[01 Project Charter]]: what the MVP is and isn't.
3. [[02 System Architecture]]: the pattern we adopted and what we add to it.
4. [[03 Trust and Provenance]]: what keeps a compiled wiki honest.
5. [[08 Claude Operating Instructions]]: exactly what Claude will be told and allowed to do.
6. [[07 Decision Log]]: accept or reject the proposed decisions.
7. [[05 Obsidian Essentials]]: the one page of Obsidian you need.

## Origin of the pattern
The foundation is Andrej Karpathy's "LLM Wiki" idea file, at https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f. It will also be the first source you ingest, so the vault's first pages will be about the pattern the vault is built on.

## Learn Obsidian from this document set
These notes use Obsidian's own syntax, so reading them is your first lesson:
- `[[01 Project Charter]]` is a **wikilink**. Click it to jump; the target lists this note under **Backlinks**.
- The block between the `---` lines is **Properties** (YAML frontmatter), shown as an editable table.
- The `> [!abstract]` boxes are **callouts**.
- The diagrams in [[02 System Architecture]] are **Mermaid** code blocks, which Obsidian draws without a plugin.

## Change log
| Version | Date | Changes |
|---|---|---|
| 0.1 | 2026-09-16 | First document set (00–07) |
| 0.2 | 2026-09-16 | Claude Code chosen as the main tool; doc 08 added; folders renamed with hyphens |
| 0.3 | 2026-09-16 | Doc 09 Working Agreement added |
| 0.4 | 2026-09-16 | Preferences agreed; modules added to the roadmap |
| **1.0** | 2026-09-18 | **Adopted the LLM Wiki pattern as the foundation.** Vault restructured into `raw/`, `wiki/`, `mine/`; ingest, query, and lint become the core operations; doc 03 narrowed to trust and provenance, with bank data governance parked as doc 12 |
| 1.1 | 2026-09-19 | **Documents 00–09 accepted** and promoted to `working`. Doc 13 (Input Zones) added: one input door per operation, all run inside Claude. |
| 1.2 | 2026-09-19 | Input zones accepted (D-023 to D-025); draft queue renamed `mine/drafts/`; M0 closed and handover written |
| 1.3 | 2026-09-19 | Obsidian curriculum removed (D-026): doc 05 becomes a reference page, goal G5 narrowed to verification (D-027), module estimates cut |
| 1.4 | 2026-09-21 | Documents moved to a private GitHub repo synced into project knowledge (D-028); the repo is now the master copy; Q-014 opened |
| **1.5** | 2026-09-21 | **M1 closed.** D-026 and D-027 accepted. D-029: your own new notes go to `mine/scratch/`. D-030: the vault repo is the single source of truth, project knowledge syncs `mine/projects/thinking-system/`, and the documents repo is archived (supersedes D-028). Docs 02, 03, 04, 05, 06, 08, 09 and 13 updated to match, including two broken links to the retired 05 Learning Path; doc 15 (M1 Handover) added |
| 1.6 | 2026-09-21 | Doc 15 (M1 Handover) accepted and promoted to `working` |
| 1.7 | 2026-09-21 | **M2 started.** Schema files created in the vault: `CLAUDE.md`, `.claude/settings.json`, `system/context.md`, `system/conventions.md`, `index.md`, `log.md`, and eight templates. Doc 10 (Templates) added. Tool facts rechecked against the current Claude Code docs; D-031 to D-035 proposed. Docs 04, 06, 08 and 13 updated to match |
| 1.8 | 2026-09-22 | First Claude Code session: claude.ai connectors, the synced `data` plugin and synced skills found loading into vault sessions. D-036 (connectors off) and D-037 (`data` plugin off) proposed; Q-015 opened (remaining synced skills, due at M3). Docs 06, 07 and 08 updated |
| **1.9** | 2026-09-22 | **M2 closed.** D-031 to D-037 accepted; D-038 added and accepted (stop when a permission rule blocks). All setup checks and the smoke test passed. Docs 06, 07, 08 and `CLAUDE.md` updated; doc 16 (M2 Handover) added |
| 1.10 | 2026-09-22 | Q-013 answered: the first five sources are the LLM-knowledge set (D-039). Docs 07 and 16 updated |
| **1.11** | 2026-09-22 | **M3 started.** `ingest` skill drafted (arrives as `ingest-SKILL.md` for you to move into `.claude/skills/ingest/`) and mirrored in doc 08 §4.1; the ingest section of `CLAUDE.md` becomes a pointer. Overview page type and template added. D-040 (answers Q-015) to D-044 proposed. Docs 04, 06, 07, 08, 10 and 13 and `system/conventions.md` updated |
| 1.12 | 2026-09-22 | D-040 to D-044 accepted. Q-015 decided: synced skills hidden in vault sessions, which takes effect once their names are in `.claude/settings.json`. Docs 06, 07 and 08 updated |
| 1.13 | 2026-09-22 | First ingest (LLM Wiki gist) reviewed. `ingest` skill revised: the status rule is clarified (one source can make a page `verified`), links are checked before the report, and the move check uses file tools instead of a shell command. Docs 06 and 08 updated |
| 1.14 | 2026-09-22 | Source 1 committed. The `raw/` deny rule blocked Claude's shell move, so the move becomes yours, with the command given in the skill's first message. D-045 proposed and accepted. Docs 06, 07, 08 and 13 updated |
| 1.15 | 2026-09-22 | Source 2 (As We May Think) ingested. The ingest missed that source 1 already discusses Bush's Memex, so the skill now searches `wiki/` and `raw/` for every new source, and also gets ground rules (file tools only, no working files, no deletions), PDF page citations (D-046, accepted) and a partial-clip check. `system/conventions.md` and docs 06, 07 and 08 updated |
| 1.16 | 2026-09-22 | Source 3 (Evergreen notes) ingested from the hub page. Its principle notes, the D-040 settings entry and one skill tweak are parked; doc 06 §6 lists them |
| 1.17 | 2026-09-22 | Source 4 (Contextual Retrieval) ingested, with the first real disagreement between sources recorded on both sides. D-047 proposed and accepted: `contested` belongs on the pages carrying the disputed claim, not on source pages or the overview. Docs 03, 06, 07 and 08 and the `ingest` skill updated |
| **1.18** | 2026-09-22 | **M3 closed.** Source 5 (The PARA Method) ingested: 6 existing pages updated, 3 with new cited claims, against a bar of 3, and a second disagreement recorded on both sides. Five sources in `raw/`, 26 wiki pages, 11 insight drafts. Doc 17 (M3 Handover) added; docs 00 and 06 updated |
| **1.19** | 2026-09-24 | **M4 started.** `ask` and `file-answer` skills drafted (arrive as `ask-SKILL.md` and `file-answer-SKILL.md` for you to move into `.claude/skills/`) and mirrored in doc 08 §4.2–4.3; the ask section of `CLAUDE.md` becomes a pointer. Test prompts made concrete, `system/test-results.md` and the test 7 file drafted. D-048 to D-052 proposed. Docs 06, 07, 08 and 13 updated |
