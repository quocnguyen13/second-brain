---
type: project-doc
project: thinking-system
status: active
trust: working
origin: claude
created: 2026-09-16
reviewed: 2026-09-19
tags: [project/thinking-system, obsidian]
---

# 05 Obsidian Essentials

Back to [[00 Project Home]] · Structure in [[04 Vault Blueprint]]

> [!info] What changed
> This was a seven-stage curriculum. It is now a one-page reference. There are no lessons, stages, or exercises: you pick things up inside the modules as you need them, and everything below can be learned in the minutes it takes to use it ([[07 Decision Log]] D-026).

**Mod** means Ctrl on Windows.

## 1. One-time setup (module M1, about 20 minutes)
- Install Obsidian; create the vault `Second-Brain` at `C:\Users\<you>\Vaults\Second-Brain`, outside OneDrive.
- Settings → Files and links: "Automatically update internal links" on; new notes to `mine/drafts`; attachment folder `raw/assets`.
- Settings → Core plugins: Backlinks, Outgoing links, Graph view, Properties view, Bases, Templates, Daily notes, Bookmarks.
- Install the Obsidian Web Clipper browser extension and point it at `inbox/sources/`. This isn't learning, it's the capture pipeline for [[13 Input Zones]].

## 2. The whole toolkit
| Need | How |
|---|---|
| Find any note | Mod+O, type part of the title |
| Run any command | Mod+P |
| Switch edit and reading view | Mod+E |
| Search the vault | Mod+Shift+F, with `path:`, `tag:`, `"exact phrase"`, `-exclude` |
| See the link graph | Mod+G; the local graph shows one note's neighbourhood |
| Link a note | `[[Title]]`, `[[Title#Heading]]`, `[[Title\|display text]]` |
| Embed a note | `![[Title]]` |
| See what links here | Backlinks pane, at the bottom or in the sidebar |
| Edit properties | The table at the top of a note, in Live Preview |
| Build a filtered view | Bases: a table over properties, e.g. `status` is `unverified` |

That is the entire set this system needs. Anything else, look up at help.obsidian.md or ask in the session.

## 3. The one skill that matters: reviewing an ingest
The wiki is only trustworthy if someone checks it, and that someone is you. After each ingest, spend five minutes:
1. Open a new or updated page in `wiki/`.
2. Read its properties: `status` and `sources`.
3. Click through one `sources` link into `raw/` and confirm the claim is really there.
4. If the page says `unverified` or `contested`, read why.

If you stop doing this, the provenance rules in [[03 Trust and Provenance]] become decoration. Nothing else in this document is load-bearing; this is.

## 4. Two views worth building (module M5)
- **Needs attention:** `status` is `unverified` or `contested`.
- **Draft queue:** everything in `mine/drafts`.

Your weekly review starts from these two plus a `/lint` run.

## 5. Where the thinking layer fits
`mine/` is not a learning exercise; it's goal G4. Claude proposes insight drafts into `mine/drafts/`, and you keep the ones you'd defend, in your own words. Module M6 sets up that routine.
