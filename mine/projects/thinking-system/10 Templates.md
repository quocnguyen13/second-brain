---
type: project-doc
project: thinking-system
status: active
trust: ai-draft
origin: claude
created: 2026-09-21
reviewed: 2026-09-21
tags: [project/thinking-system, templates]
---

# 10 Templates

Back to [[00 Project Home]] · Page types in [[04 Vault Blueprint]] §2–3 · Rules in [[08 Claude Operating Instructions]]

> [!abstract] What this is
> One template per page type, in `system/templates/`. The wiki templates are the page shape Claude follows when it writes; the `mine/` templates are for your own notes in Obsidian. The files are the source of truth; this page describes them so project chats can see them ([[07 Decision Log]] D-034).

## 1. The set
| Template file | `type` | Used by | Goes in | Headings |
|---|---|---|---|---|
| `Source template` | source | Claude, at ingest | `wiki/sources/` | Summary · Key claims · Entities and concepts · Conflicts and open points |
| `Entity template` | entity | Claude | `wiki/entities/` | What the sources say · Mentioned in · Related |
| `Concept template` | concept | Claude | `wiki/concepts/` | What the sources say · Where sources disagree · Mentioned in · Related |
| `Analysis template` | analysis | Claude, when filing an answer | `wiki/analyses/` | Answer · Evidence · Caveats and gaps · Related |
| `Insight template` | insight | You; Claude for drafts | `mine/insights/`, `mine/drafts/` | Why I think this · Relations |
| `Decision template` | decision | You | `mine/decisions/` | Context · Options · Decision · Reasoning · Revisit when |
| `Project template` | project | You | `mine/projects/` | Goal · Status · Next steps · Links |
| `Journal template` | journal | You, via Daily notes | `mine/journal/` | Notes · Questions to queue |

**Properties.** Wiki templates carry `type`, `status: unverified`, `sources: []`, `created`, `updated`, `tags`. `mine/` templates carry `type`, `status` (`draft` for insights and decisions, `active` for projects and journals), `origin: me`, `created`, `related`. Claude's insight drafts set `origin: claude`. All as in [[04 Vault Blueprint]] §3.

**Why wiki templates start `unverified`.** Claude has to set `verified` deliberately, once every claim on the page cites a file in `raw/`. A page that is never checked stays flagged.

## 2. Using them
- **Your notes:** create the note, then Mod+P → "Templates: Insert template" → pick one. `{{title}}` and `{{date:YYYY-MM-DD}}` fill in on insert.
- **Daily notes:** Settings → Daily notes → Template file location → `system/templates/Journal template`. Then the Daily notes button creates each day's note from it.
- **Claude:** `system/conventions.md` tells Claude to read a page's template before creating it and to fill the variables itself. Claude Code doesn't run Obsidian's template engine.

## 3. Rules
- **Edit templates in Source mode** (Mod+E switches). In Live Preview, the Properties panel can rewrite unquoted `{{date}}` values, so the templates keep them in quotes.
- **Templates hold no wikilinks.** Placeholder links would show up as ghost nodes in the graph and as broken links in lint.
- **Views and lint are scoped by folder.** The templates carry `status: unverified` and `draft`, so the Bases views in module M5 and `/lint` look only at `wiki/` and `mine/`, never `system/`.
- **Change a template and this page together**, in the same commit.
