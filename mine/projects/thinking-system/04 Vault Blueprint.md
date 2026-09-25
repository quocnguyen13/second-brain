---
type: project-doc
project: thinking-system
status: active
trust: working
origin: claude
created: 2026-09-16
reviewed: 2026-09-24
tags: [project/thinking-system, vault-design]
---

# 04 Vault Blueprint

Back to [[00 Project Home]] · Related: [[02 System Architecture]] · [[03 Trust and Provenance]]

## 1. Structure
```
Second-Brain/              ← the vault; a git repository pushed to the private repo second-brain (D-030)
├── CLAUDE.md              the schema: rules Claude loads every session
├── index.md               catalog of every wiki page (Claude maintains)
├── log.md                 append-only history of ingests, filings, lints (Claude appends)
├── .gitignore             files git never tracks (doc 08 §6)
├── .gitattributes         one line-ending rule for every text file (doc 08 §6)
├── .obsidian/             Obsidian's own settings; git ignores workspace*.json
├── inbox/                 THREE INPUT ZONES, one per operation (doc 13)
│   ├── sources/           files awaiting /ingest
│   ├── questions.md       questions awaiting /ask
│   └── checks.md          things awaiting /lint
├── raw/                   YOUR sources, after ingest. Claude reads, never edits.
│   ├── assets/            images and attachments
│   └── *.md, *.pdf
├── wiki/                  CLAUDE'S compiled pages. You read.
│   ├── overview.md        the current picture, in one page
│   ├── sources/           one summary page per source
│   ├── entities/          people, organisations, products, tools
│   ├── concepts/          ideas, methods, patterns, regulations
│   └── analyses/          comparisons and answers worth keeping
├── mine/                  YOURS. Claude drafts into drafts/ only.
│   ├── scratch/           your own new notes, not yet sorted (D-029)
│   ├── drafts/            Claude's insight drafts awaiting your decision
│   ├── insights/          single ideas, in your words; you write every one (D-063)
│   ├── decisions/         what you decided in your own work and life, and why
│   ├── projects/          your active work
│   └── journal/           daily and weekly notes
├── system/
│   ├── context.md         who you are, current focus, glossary (you maintain)
│   ├── conventions.md     short version of this document, for Claude
│   ├── lint/              dated lint reports
│   ├── views/             Review.base: the weekly review views (D-058)
│   └── templates/         one template per page type (doc 10)
└── .claude/               Claude Code settings and skills (hidden in Obsidian)
```
Three rules make the structure work: **`raw/` is immutable, `wiki/` is Claude's, `mine/` is yours.** Everything enters through `inbox/`, where each operation has its own door ([[13 Input Zones]]).

Every folder that would otherwise be empty holds a hidden `.gitkeep` file, because git doesn't track empty folders. Without them, a fresh clone of the repo would come back without the structure.

## 2. Page types
| `type` | Folder | Purpose | Title style |
|---|---|---|---|
| `source` | wiki/sources | What one source says, in summary | "Source - <title>" |
| `entity` | wiki/entities | A person, company, product, or tool | The name |
| `concept` | wiki/concepts | An idea, method, or regulation | The term |
| `analysis` | wiki/analyses | A comparison or filed answer | The question or claim |
| `overview` | wiki/overview.md | The current picture across all sources, rewritten at each ingest (D-044) | "Overview" |
| `insight` | mine/insights | One idea of yours | A claim: "Compiled wikis need a provenance rule to stay honest" |
| `decision` | mine/decisions | A choice in your own work or life: context, options, choice, reasoning. Decisions about this system go in [[07 Decision Log]] (D-066) | "Decision - <topic> - YYYY-MM-DD" |
| `project` | mine/projects | Goal, status, links | The project name |
| `journal` | mine/journal | Daily or weekly note | "YYYY-MM-DD" or "YYYY-Www" |

## 3. Properties
Wiki pages:
```yaml
---
type: concept
status: verified        # verified | unverified | contested
sources: ["[[raw/karpathy-llm-wiki.md]]"]
created: 2026-09-18
updated: 2026-09-18
tags: [knowledge-management]
---
```
Pages in `mine/`:
```yaml
---
type: insight
status: draft           # draft | active | archived
origin: me              # me | claude
created: 2026-09-18
reviewed: 2026-09-18    # insights only: the date you last wrote or re-read it
related: ["[[Compiled wiki]]"]
---
```
- `status`: `draft` while you write it, `active` once you'd defend it, `archived` when you no longer hold it, with a line saying why. Only you change it (D-065).
- `origin: me` means you wrote every sentence. Claude's drafts are `origin: claude` and never move into `mine/insights/`; a kept idea is a new page (D-063).
- `/drafts` adds `checked: <date>` to each draft it checks (D-064).

## 4. Linking
- Link freely in sentences, with `[[wikilinks]]`.
- Insight pages end with a Relations block:
  ```markdown
  ## Relations
  - supports:: [[...]]
  - contradicts:: [[...]]
  - extends:: [[...]]
  - source:: [[...]]
  ```
  Read each line as "this insight *supports / contradicts / extends* the page". `source::` names the source page the idea came from. At least one line links a page in `wiki/`; lines can also link your other insights. `related` lists the same pages (D-065).
- Every entity and concept page links to the source pages that mention it, and back.
- Claude adds cross-references during ingest. That's the bookkeeping you're handing over.

## 5. `index.md`
A catalog, grouped by folder, one line per page, updated on every ingest:
```markdown
## Concepts
- [[wiki/concepts/Compiled wiki]] — a knowledge base compiled once and kept current, rather than retrieved per query (3 sources)
- [[wiki/concepts/Provenance]] — rules that tie each claim to a source (2 sources)
```
Claude reads this first when answering, then opens the pages it needs.

## 6. `log.md`
Append-only, one entry per operation, always with the same prefix so it can be filtered from a terminal:
```markdown
## [2026-09-18] ingest | LLM Wiki gist
Pages: +4 new, 3 updated. Contradiction noted on [[wiki/concepts/RAG]].
```
`grep "^## \[" log.md | tail -5` then shows the last five things that happened.

## 7. Naming
- Folders are lower case with hyphens; page titles are plain language.
- Avoid these characters in titles: `# ^ [ ] | \ / : * " < > ?`
- Files in `raw/` are named as they move in: `<author>-<short-title>.<ext>`, lower case with hyphens, e.g. `karpathy-llm-wiki.md`. The content is never changed (D-042).
- Dates as `YYYY-MM-DD`.
- One idea per insight page, titled as a statement you could agree or disagree with.
