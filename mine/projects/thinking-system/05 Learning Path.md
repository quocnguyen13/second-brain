---
type: project-doc
project: thinking-system
status: active
trust: working
origin: claude
created: 2026-09-16
reviewed: 2026-09-19
tags: [project/thinking-system, learning]
---

# 05 Learning Path: Obsidian as a Second Brain

Back to [[00 Project Home]] · Structure from [[04 Vault Blueprint]]

> [!tip] How this fits the build
> Stages 0–2 come before Claude is connected (module M1), so you can navigate the vault. Stages 3–4 run alongside the first ingests, since reading what Claude produces is how you learn the shape of a wiki. Stages 5–6 build your own thinking layer.

**Mod** below means Ctrl on Windows.

## Stage 0: Setup (30 minutes, module M1)
- [ ] Install Obsidian from obsidian.md.
- [ ] Create a vault named `Second-Brain` at `C:\Users\<you>\Vaults\Second-Brain`, outside any OneDrive folder.
- [ ] Settings → Files and links: turn on "Automatically update internal links"; set new notes to go to `mine/drafts`; set the attachment folder to `raw/assets`.
- [ ] Settings → Core plugins: enable Backlinks, Outgoing links, Graph view, Daily notes, Templates, Properties view, Bases, Canvas, Bookmarks.
- [ ] Create the folders from [[04 Vault Blueprint]] §1.

## Stage 1: Reading and writing notes (days 1–2)
**Learn:** headings, lists, checkboxes, quotes, callouts; Live Preview versus Reading view (Mod+E); command palette (Mod+P); quick switcher (Mod+O).
**Do:** put this document set into `mine/projects/thinking-system/` and read it in Obsidian, following the links.
**Done when:** you can move around the vault without the mouse.

## Stage 2: Links and the graph (days 3–4)
**Learn:** `[[wikilinks]]`, links to headings, display text with `|`, embeds `![[ ]]`, Backlinks and Outgoing links panes, unlinked mentions, graph view (Mod+G) and the local graph.
**Do:** open the local graph for this project's Home note and follow the connections.
**Why it matters here:** the wiki Claude builds *is* a link graph. The graph view is how you see whether it's healthy: hubs, clusters, and orphans.
**Done when:** you can tell, from the graph, which pages are central and which are stranded.

## Stage 3: Properties, index, and log (alongside the first ingests, M3)
**Learn:** the Properties editor; how `status`, `sources`, and `updated` drive everything in [[03 Trust and Provenance]]; reading `index.md` and `log.md`.
**Do:** after your first ingest, check each new page's properties and trace one claim back to its source in `raw/`.
**Done when:** you can spot an `unverified` page and say what's missing.

## Stage 4: Capture (M3)
**Learn:** Obsidian Web Clipper (browser extension) for turning articles into Markdown; downloading images locally; daily notes.
**Do:**
- Clip three articles into `raw/`.
- Set a hotkey for "Download attachments for current file" so a clipped article's images are stored locally, where Claude can look at them.
- Write a short daily note each day: what you fed the vault, what you asked it.
**Done when:** clipping and ingesting takes under 5 minutes.

## Stage 5: Your thinking layer (M6)
**Learn:** atomic notes, evergreen writing in your own words, Relations blocks, Canvas for arranging ideas.
**Do:** work through `mine/drafts/`: for each draft Claude proposed, rewrite it in your words or delete it. Keep the ones you'd defend.
**Done when:** you have 5 insight pages that you wrote, linked to wiki pages that back them.

## Stage 6: Finding and reviewing (M5–M6)
**Learn:** search operators (`path:`, `file:`, `tag:`, `"exact phrase"`, `-exclude`); Bases for views built on properties.
**Do:** build two Bases: "Needs attention" (`status` is `unverified` or `contested`) and "Draft queue" (`mine/drafts`).
**Done when:** your weekly review starts from those two views plus a lint pass.

## Stage 7: The weekly habit (ongoing)
30 minutes: run lint → fix what it found → empty `mine/drafts` → update `system/context.md` → write the weekly note.

## Methods behind the design
| Method | Idea | Where it shows up |
|---|---|---|
| LLM Wiki (Karpathy) | Compile sources into a maintained wiki rather than retrieving per query | `raw/` → `wiki/` |
| Zettelkasten (Luhmann) | Single-idea notes, densely linked | `mine/insights` |
| Maps of Content (Milo) | Hub pages instead of rigid hierarchies | `index.md`, `wiki/overview.md` |
| CODE (Forte) | Capture, organize, distill, express | The operations in [[02 System Architecture]] |

## Beginner traps
- Batch-ingesting twenty sources before you've read a single output
- Installing plugins you don't need yet
- Treating Claude's summaries as facts without checking a citation
- Letting `mine/drafts` become a graveyard
