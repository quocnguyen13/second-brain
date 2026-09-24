---
type: project-doc
project: thinking-system
status: active
trust: working
origin: claude
created: 2026-09-16
reviewed: 2026-09-24
tags: [project/thinking-system, obsidian]
---

# 05 Obsidian Essentials

Back to [[00 Project Home]] · Structure in [[04 Vault Blueprint]]

> [!info] What changed
> This was a seven-stage curriculum. It is now a one-page reference. There are no lessons, stages, or exercises: you pick things up inside the modules as you need them, and everything below can be learned in the minutes it takes to use it ([[07 Decision Log]] D-026).

**Mod** means Ctrl on Windows.

## 1. One-time setup (module M1, about 20 minutes)
- Install Obsidian; create the vault `Second-Brain` at `C:\Users\<you>\Vaults\Second-Brain`, outside OneDrive.
- Settings → Files and links: "Automatically update internal links" on; new notes to `mine/scratch` ([[07 Decision Log]] D-029); attachment folder `raw/assets`.
- Settings → Core plugins: Backlinks, Outgoing links, Graph view, Properties view, Bases, Templates, Daily notes, Bookmarks. Sync and Publish off.
- Settings → Daily notes: new file location `mine/journal`. Settings → Templates: template folder location `system/templates`.
- Install the Obsidian Web Clipper browser extension. In its settings, add `Second-Brain` under General → Vaults, then set the Default template's Note location to `inbox/sources` (the folder only, no vault name). This isn't learning, it's the capture pipeline for [[13 Input Zones]].
- Inside Obsidian and in Markdown, folder paths use `/`. PowerShell uses `\`.

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

## 4. The weekly review (module M5)
Two views live in one Bases file, `system/views/Review.base` ([[07 Decision Log]] D-058). Bookmark it once (right-click the file → Bookmark); the view switcher at the top of the table moves between the two.
- **Needs attention:** wiki pages that are `unverified` or `contested`, `unverified` first. `unverified` means a claim needs a citation or a fix; `contested` means two sources disagree and the call is yours (D-057).
- **Draft queue:** Claude's insight drafts in `mine/drafts/`, oldest first.

About 30 minutes, once a week. The first `/lint` of each month takes longest, because it checks every page against `raw/` (D-060); other weeks check only what changed (D-056).
1. **Start clean.** At the vault root, `git status`; commit anything left over.
2. **Lint.** Start `claude` at the vault root and run `/lint`. Open the new report in `system/lint/`. Trace any finding you doubt to `raw/`, as in §3.
3. **Apply.** Run `/lint apply <numbers>` for the fixes you agree with, adding the letter where a finding offers options, e.g. `/lint apply 1 2 4b`. Then `git add -A`, `git diff --staged`, and `git commit -m "lint: report-YYYY-MM-DD"`. Findings you leave come back next week marked "Open since".
4. **Needs attention.** For each page, read its one-line reason under "Already flagged" in the report. Leave it, add a check to `inbox/checks.md`, or clip a source that would settle it.
5. **Draft queue.** For each draft, keep it or delete it. To keep one, move it to `mine/insights/`, rewrite it in your own words, and set `status: active`. Five insights kept or written is the last MVP criterion ([[01 Project Charter]] §6).
6. **Scratch.** Empty `mine/scratch/`: a source goes to `inbox/sources/`, a question to `inbox/questions.md`, a doubt about a wiki page to `inbox/checks.md`, your own thinking to `mine/insights/`, `mine/decisions/` or `mine/projects/`. Delete the rest.
7. **Commit and push.** `git add -A`, `git diff --staged`, `git commit -m "review: YYYY-Www"`, then `git push`.

## 5. Where the thinking layer fits
`mine/` is not a learning exercise; it's goal G4. Claude proposes insight drafts into `mine/drafts/`, and you keep the ones you'd defend, in your own words. Module M6 sets up that routine.

## 6. `system/views/Review.base`
Mirrored here because project chats can't see `system/`; change both in the same commit. Obsidian rewrites the file in its own style when you change a view, so copy it from the vault after any change. Bases syntax: https://obsidian.md/help/bases/syntax (checked 2026-09-24).
```yaml
properties:
  file.name:
    displayName: Page
  note.status:
    displayName: Status
  note.type:
    displayName: Type
  note.updated:
    displayName: Updated
  note.sources:
    displayName: Sources
  note.created:
    displayName: Created
  note.origin:
    displayName: Origin
  note.related:
    displayName: Related
views:
  - type: table
    name: Needs attention
    filters:
      and:
        - file.inFolder("wiki")
        - file.ext == "md"
        - or:
            - status == "unverified"
            - status == "contested"
    groupBy:
      property: status
      direction: DESC
    order:
      - file.name
      - type
      - updated
      - sources
    sort:
      - property: updated
        direction: ASC
    columnSize:
      note.type: 103
  - type: table
    name: Draft queue
    filters:
      and:
        - file.inFolder("mine/drafts")
        - file.ext == "md"
    order:
      - file.name
      - created
      - origin
      - related
    sort:
      - property: created
        direction: ASC
```
