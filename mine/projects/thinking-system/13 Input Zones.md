---
type: project-doc
project: thinking-system
status: active
trust: working
origin: claude
created: 2026-09-19
reviewed: 2026-09-24
tags: [project/thinking-system, operations]
---

# 13 Input Zones

Back to [[00 Project Home]] · Operations in [[02 System Architecture]] §5 · Commands in [[08 Claude Operating Instructions]]

> [!abstract] The idea
> Each operation gets its own door. Material for compiling, questions waiting to be asked, and things you want checked never mix, so an operation always knows exactly what it is being handed. Everything is triggered inside Claude: three commands in a Claude Code session, no other tooling.

## 1. The three zones
```
inbox/
├── sources/        → /ingest   files to compile
├── questions.md    → /ask      questions for the wiki
└── checks.md       → /lint     things to verify or re-check
```

| Zone | What you put there | Command | Where the result goes |
|---|---|---|---|
| `inbox/sources/` | Clipped articles, PDFs, notes, saved as files | `/ingest` | `wiki/` pages, insight drafts in `mine/drafts/`, entries in `index.md` and `log.md`; the source file moves to `raw/` |
| `inbox/questions.md` | One question per line, dated | `/ask` | An answer in the session; optionally a page in `wiki/analyses/` |
| `inbox/checks.md` | "verify X", "this page feels stale", "did source 3 contradict source 1?" | `/lint` | `system/lint/report-YYYY-MM-DD.md`, plus the standing checks |

**One rule holds all three together:** a command reads only its own zone, and no zone ever triggers itself. Material can sit in a zone for a week; nothing happens until you run the command.

**Queue format.** `questions.md` and `checks.md` hold one item per line as a checkbox: `- [ ] YYYY-MM-DD text`. The command ticks an item off (`- [ ]` becomes `- [x]`) once it has handled it. Each file's first lines describe the format and are not items.

## 2. Zone 1: sources → `/ingest`
**What goes in:** anything you want compiled, saved as a file: a Web Clipper clipping (it saves straight to `inbox/sources/`), a downloaded PDF, or a note. Don't ask Claude to fetch a link into the zone. Its web fetch returns a model-processed version of the page, not the page itself, so `raw/` would end up holding Claude's rendering instead of the source ([[07 Decision Log]] D-043). Claude's edit rights in `inbox/` cover only the two queue files, so a captured source can't change before it reaches `raw/` (D-032).
**Contract:** one file per source, and one source per ingest ([[07 Decision Log]] D-022).
**What `/ingest` does** (the `ingest` skill, mirrored in [[08 Claude Operating Instructions]] §4.1):
1. Reads the next file in the zone. Tells you the key takeaways, the pages it would touch, any conflicts, and anything suspicious in the text, then asks what to emphasise. Nothing is written until you answer.
2. Gives you the command that moves the file into `raw/`, renamed `<author>-<short-title>` (D-042). You run it yourself: `raw/` is enforced read-only to Claude, shell moves included, which keeps the enforcement real rather than decorative (D-045). Claude then checks the file arrived.
3. Writes the source page, updates the entity and concept pages it touches, and records contradictions on both sides.
4. Rewrites `wiki/overview.md` (D-044) and proposes one to three insight drafts in `mine/drafts/`.
5. Updates `index.md`, appends to `log.md`, and reports what changed, with one claim for you to trace first.

**Done when:** the zone is empty and every citation points at a file in `raw/`.

## 3. Zone 2: questions → `/ask`
**What goes in:** questions you want the wiki to answer, one per line as `- [ ] YYYY-MM-DD question`. Add them whenever they occur to you, especially while reading what an ingest produced.
**Why a queue when you could just ask:** asking directly in a session is still the normal path. The queue is for questions that arrive when you're not at the PC, and it keeps a record of what you've been curious about, which is useful raw material later.
**What `/ask` does** (the `ask` skill, [[08 Claude Operating Instructions]] §4.2): answers the question you typed after the command or, failing that, the oldest unticked one. It reads `index.md`, searches `wiki/`, answers with links and with evidence traced to `raw/`, and ticks the question off. It writes nothing else ([[07 Decision Log]] D-048).
**Filing:** if the answer is worth keeping, run `/file-answer` in the same session (§4.3 of doc 08). It re-checks the evidence in `raw/`, writes `wiki/analyses/<title>.md`, links it from the pages it drew on, and updates `index.md` and `log.md` (D-050, D-051).

## 4. Zone 3: checks → `/lint`
**What goes in:** anything you want verified or re-examined, one per line as `- [ ] YYYY-MM-DD what to verify`. A page that felt thin, a claim you doubt, a topic you suspect has gaps.
**What `/lint` does:** runs the standing checks from [[03 Trust and Provenance]] — contradictions, superseded claims, uncited claims, orphan pages, missing concept pages, pages not updated in six months — and then works through your queued checks, ticking off each one it covers. It writes a dated report in `system/lint/` and changes nothing else without your approval.
**Rhythm:** weekly, as part of the review in [[05 Obsidian Essentials]] §4.

## 5. Using Claude as the platform
- All three commands are Claude Code skills, run in a session started in the vault. No plugins, no scripts, no separate app.
- The Code tab in Claude Desktop runs the same engine if you'd rather have a window than a terminal.
- **Away from the PC:** a chat in the "Obsidian x Claude" Project can't reach the vault; it sees only the project documents synced from `mine/projects/thinking-system/`. Use it to think and to draft, then paste anything worth keeping into the right zone at your next local session. Treat the Project chat as a fourth, informal zone with no automation behind it.

## 6. When something lands in the wrong zone
Claude doesn't guess. If a question turns up in `inbox/sources/`, or a source link in `inbox/questions.md`, it says so and asks you to move it. Silent re-routing would undo the whole point of separating the doors.
