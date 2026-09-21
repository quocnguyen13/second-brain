---
type: moc
project: thinking-system
status: active
trust: working
origin: claude
created: 2026-09-16
reviewed: 2026-09-21
tags: [project/thinking-system, moc]
---

# Thinking System: Project Home

> [!abstract] What this is
> A personal knowledge base built on the **LLM Wiki** pattern: you collect sources, Claude compiles and maintains a linked wiki from them, and you read it in Obsidian. On top of that foundation we add a thinking layer you own, provenance rules, and product-owner workflows.

**Setup:** personal Windows PC · Claude Pro · Claude Code running inside the vault
**Current module:** M1 closed 2026-09-21 → next, M2 – Connect Claude Code (see [[06 Roadmap]])

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
| 13 | [[13 Input Zones]] | One input door per operation, all triggered inside Claude | **Accepted** |
| 14 | [[14 M0 Handover]] | Closing state of M0, used to open the M1 chat | Closed |
| 15 | [[15 M1 Handover]] | Closing state of M1, to open the M2 chat with | Current |

**Planned (not written yet)**
- 10 Templates (module M2): page templates for each type
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
