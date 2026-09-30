# Conventions

<!-- Short version of doc 32 Vault Blueprint, loaded every session. Templates are in system/templates/ (doc 34). -->

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
| `ingest-set` | `system/ingest/` | `set-YYYY-MM-DD` | The format is in the `ingest` skill |

When you create a page, read its template first and follow its properties and headings. Replace `{{title}}` and `{{date:YYYY-MM-DD}}` yourself.

## Properties
- Wiki pages: `type`, `status` (verified | unverified | contested), `sources` (links into `raw/`), `created`, `updated`, `tags`. Source pages also carry `trust` (primary | secondary | commentary | ai).
- Pages in `mine/`: `type`, `status` (draft | active | archived), `origin` (me | claude), `created`, `related`. My insights also carry `reviewed`, the date I last wrote or re-read one.
- You set `status` on wiki pages when you write them. Your insight drafts are `status: draft`, `origin: claude`, and `/drafts` adds `checked`. Only I change the `status` of anything in `mine/`.
- Dates are `YYYY-MM-DD`. Update `updated` whenever you change a wiki page.

## Trust levels
One level per source, set by its type. When a source fits no row, or two, propose the lower level and say why; I decide, and a level I set is recorded as mine.

| `trust` | Source types | Examples |
|---|---|---|
| `primary` | The origin of the facts, speaking for itself: legislation and regulations; a regulator's, government's, court's or standard-setter's own publications; official statistics; an organisation's own statements about itself; an author's own statement of their own idea or work | FSMA Part 1A; the PRA's supervision approach; the FCA's own website; Karpathy's gist on his pattern |
| `secondary` | Independent, accountable analysis of primary material: parliamentary library briefings and committee reports; academic papers and textbooks; reports by other public bodies; professional bodies' guidance | A House of Commons Library briefing |
| `commentary` | Opinion, news and general-audience writing: news articles, blogs, law-firm and consultancy briefings, encyclopedias including Wikipedia, forums, my own notes | A Wikipedia article |
| `ai` | A Claude output saved as a source (D-075). Its claims stay uncited until a primary source backs them | A research report from a Claude chat |

- A fact takes the level of its best source. A citation of a source below primary ends with its level, inside the brackets: `([[raw/<name>]] · secondary)`, `· commentary`, `· AI`. Primary citations carry no marker.
- A disagreement on a fact is settled by level, then by date; a disagreement of views is never settled by level. I decide either way. The claim set aside stays under "Where sources disagree", marked "outweighed by" or "superseded by", with the date it was resolved.

## Linking
- Link in sentences with `[[wikilinks]]`, using page titles.
- Every entity and concept page links to the source pages that mention it, and each source page links back.
- Cite a claim inline with a link to the raw file, e.g. `([[raw/karpathy-llm-wiki.md]])`. For a PDF, add the page, e.g. `([[raw/bush-as-we-may-think.pdf#page=16]])`; Obsidian opens the PDF at that page. For legislation, add the section, e.g. `([[raw/uk-parliament-fsma-2000-part-1a.md]], s. 3D(1))`. Add the level marker last.
- Insight pages end with a Relations block: `- supports:: [[...]]`, `- contradicts:: [[...]]`, `- extends:: [[...]]`, `- source:: [[...]]`. Read each line as "this insight supports / contradicts / extends the page"; `source::` names the source page the idea came from.

## `index.md`
Grouped by folder (Overview, Sources, Entities, Concepts, Analyses), one line per page:
`- [[wiki/concepts/Compiled wiki]] — one-line summary (N sources)`. Read it first when answering.

## `log.md`
Append-only. One entry per operation, newest at the bottom, naming the pages it created or changed:
```
## [YYYY-MM-DD] ingest | <topic>
Set: set-YYYY-MM-DD, N sources (N primary, N secondary, N commentary). Pages: +N new (<titles>); N updated (<titles>). Conflicts: N. Flags: <or "none">.
```

## Naming
- Folders: lower case with hyphens. Page titles: plain language.
- Files in `raw/`: `<author>-<short-title>.<ext>`, lower case with hyphens, e.g. `karpathy-llm-wiki.md`. With no author, the organisation or site (`fca-...`, `wikipedia-...`); add the year for a document in a dated series. Named when they move in; content never changed.
- Never use these characters in titles: `# ^ [ ] | \ / : * " < > ?`
- One idea per insight page. Your drafts cite `raw/` inline, as wiki pages do, and mark reasoning no source states "(reasoning)".
