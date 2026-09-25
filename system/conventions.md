# Conventions

<!-- Short version of doc 04 Vault Blueprint, loaded every session. Templates are in system/templates/ (doc 10). -->

## Page types
| `type` | Folder | Title | Template |
|---|---|---|---|
| `source` | `wiki/sources/` | `Source - <title>` | `system/templates/Source template.md` |
| `entity` | `wiki/entities/` | The name | `system/templates/Entity template.md` |
| `concept` | `wiki/concepts/` | The term | `system/templates/Concept template.md` |
| `analysis` | `wiki/analyses/` | The question or claim | `system/templates/Analysis template.md` |
| `overview` | `wiki/overview.md`, one page | `Overview` | `system/templates/Overview template.md` |
| `insight` | `mine/drafts/` when you draft one. A kept insight is a new page I write in `mine/insights/` | A claim someone could disagree with | `system/templates/Insight template.md` |
| `decision`, `project`, `journal` | `mine/decisions/`, `mine/projects/`, `mine/journal/` | Mine only; you never create these | |

When you create a page, read its template first and follow its properties and headings. Replace `{{title}}` and `{{date:YYYY-MM-DD}}` yourself.

## Properties
- Wiki pages: `type`, `status` (verified | unverified | contested), `sources` (links into `raw/`), `created`, `updated`, `tags`.
- Pages in `mine/`: `type`, `status` (draft | active | archived), `origin` (me | claude), `created`, `related`. My insights also carry `reviewed`, the date I last wrote or re-read one.
- You set `status` on wiki pages when you write them. Your insight drafts are `status: draft`, `origin: claude`, and `/drafts` adds `checked`. Only I change the `status` of anything in `mine/`.
- Dates are `YYYY-MM-DD`. Update `updated` whenever you change a wiki page.

## Linking
- Link in sentences with `[[wikilinks]]`, using page titles.
- Every entity and concept page links to the source pages that mention it, and each source page links back.
- Cite a claim inline with a link to the raw file, e.g. `([[raw/karpathy-llm-wiki.md]])`. For a PDF, add the page, e.g. `([[raw/bush-as-we-may-think.pdf#page=16]])`; Obsidian opens the PDF at that page.
- Insight pages end with a Relations block: `- supports:: [[...]]`, `- contradicts:: [[...]]`, `- extends:: [[...]]`, `- source:: [[...]]`. Read each line as "this insight supports / contradicts / extends the page"; `source::` names the source page the idea came from.

## `index.md`
Grouped by folder (Overview, Sources, Entities, Concepts, Analyses), one line per page:
`- [[wiki/concepts/Compiled wiki]] — one-line summary (N sources)`. Read it first when answering.

## `log.md`
Append-only. One entry per operation, newest at the bottom:
```
## [YYYY-MM-DD] ingest | <title>
Pages: +N new, N updated. <conflicts or notes>
```

## Naming
- Folders: lower case with hyphens. Page titles: plain language.
- Files in `raw/`: `<author>-<short-title>.<ext>`, lower case with hyphens, e.g. `karpathy-llm-wiki.md`. Named when they move in; content never changed.
- Never use these characters in titles: `# ^ [ ] | \ / : * " < > ?`
- One idea per insight page. Your drafts cite `raw/` inline, as wiki pages do, and mark reasoning no source states "(reasoning)".
