<!-- Supporting file of the ingest skill. SKILL.md A0 sends you here for a large document and for /ingest part. Mirrored in mine/projects/thinking-system/40 Claude Operating Instructions §4.1; change both in the same commit. -->

# A large document, in parts

What changes when a source is too big for one run: a PDF over 150 pages, a Markdown file over 3,000 lines, or a file I call large. A full Act or a 1,000-page book is what this file is for. Everything it doesn't mention runs as `SKILL.md` says.

**The shape** (D-107, D-108)
- **The file stays whole in `raw/`.** Nothing is split, copied or converted, and every citation points into it at its page or section.
- **The first run maps.** It writes the document's source page as a map: every part, where it sits in the file, and which parts are compiled. The map is where progress lives between runs.
- **Every later run compiles one part:** its own short brief, set review, review and commit. A part is at most about 60 PDF pages or 2,000 lines. I clear the session between runs, so each run starts small.
- **Not every part needs compiling.** A part nobody needs stays `not compiled` on the map, and `/ask` says so when a question falls in one.

## 1. Which run this is
- **The file is in `inbox/sources/` and is large:** the map run (§2–§4). It is a set of its own, with its contents page when §2 needs one. If the zone holds other files, leave them for the next set and say so in the brief.
- **`/ingest part <document> [<part>]`:** a part run (§5–§7). The document is its raw name, or words from its map's title. With no part named, take the first part with status `planned`, lowest number first. With no document named, list each map with parts `planned` or `not compiled`, and ask. The file is already in `raw/`, so there is no import check and no move.
- **A set review with `status: compiling`:** a run that stopped. A0 resumes it at the first row not ticked (§6).

## 2. The map run: brief (A1)
Read only what the map needs, never the whole file:
- **PDF:** the first pages until the contents ends, in ranges of up to 20 pages, then the last page. If the contents prints page numbers, open one page it names to find the offset between printed and PDF page numbers.
- **Markdown:** Grep its headings (`^#{1,4} `) for their line numbers, and Read the first 200 lines.
- **A PDF with no contents pages,** such as legislation.gov.uk's whole-Act PDF, which opens on the text: the parts come from the publisher's contents page instead (D-115). If a clip of it is in the zone, it joins this set as the contents companion (below). If not, say so in the brief, ask me to clip it into `inbox/sources/`, and stop. Never name or describe a part from general knowledge, on the map or in the brief.

**The contents companion** is a clip of the publisher's contents page for this document. It lists the parts and sections and holds none of their text.
- Read it with Grep for its Part, Chapter and Schedule headings, then Read the lines between them as needed. Check it ends with the document's last division (for an Act, its last Schedule); if it stops short, say so and stop.
- Raw name: the document's stem, `-contents`, and the year and month of its own "up to date" line: `uk-parliament-fsma-2000-contents-2026-10.md`.
- No source page of its own. The map is its source page: the header line names it, `sources` lists it, and it backs only the map's Parts table and Summary. No other page cites it.
- It never ticks a capture line, even when its link matches one.
- Its date can differ from the document's. Where a located part's heading in the document differs from the contents, the map follows the document and notes the difference under "Conflicts and open points".

Then send the brief as A1 describes, with these changes:
- **Set:** the document alone, or with its contents companion: "large: N pages (or lines); this run maps it, and each part compiles in a run of its own".
- **Sources:** one row, or two with the contents companion, with the import verdict. A whole document whose part is already in `raw/` gets **part** (§8). A consolidated text's raw name ends with the year and month of its "up to date" date (§8).
- **Map:** the document's divisions in order (Parts, Chapters, Schedules), each with what it covers and its size where known. Split a division over about 60 pages or 2,000 lines at its next level (Chapters, cross-headings), and group small neighbours, so that each part fits one run. Label each part as the document does (`II`, `4A`, `Sch 17`), with `.1`, `.2` for a split.
- **Plan:** the parts to compile, numbered in order. First those that would back an `· AI` claim or a line on the capture list, or that touch existing pages; then the others the topic needs. Name the parts you'd leave `not compiled`, and why. A part another raw file already covers is marked **compare** (§8).
- **Touches** and **Likely conflicts:** for the planned parts, from their titles and a Grep of `wiki/` and `raw/`. Say they firm up part by part.
- **Move command** and **Question** as A1. Ask also whether to change the plan.

Write nothing until I answer.

## 3. Locate before reading
Where a part sits goes on the map as soon as it is known.
- **A contents page with page numbers:** add the offset from §2.
- **No page numbers:** find a part's pages when it is planned. Open one page at an estimate, see where it sits from its headings or running header, and step forward or back, one page at a time, until you reach the page where the part starts; do the same for its end. Never read through the document to find a part. Parts that aren't planned stay "not located yet".
- **Markdown:** the line numbers from the heading Grep.

## 4. The map run: write the map (A3–A4)
- **Set review** as usual, topic `<title>, map`, with one row under "Plan and progress": `M`.
- **The map** is `wiki/sources/Source - <title>.md`, from the Source template. For a consolidated text, the title carries the year and month: `Source - FSMA 2000 (2026-10)`. Add to the header line: `**Size:** N pages · **Compiled:** 0 of N parts`.
- **Summary:** what the document is and how it is organised, citing the contents pages.
- **Parts,** after Summary, one row per part in the document's order, every part listed. For example:
  ```
  | Part | Covers | Where | Status |
  |---|---|---|---|
  | II | Regulated and prohibited activities, ss. 19–30 | pp. 45–71 | compiled 2026-10-15 · [[wiki/sources/Source - FSMA 2000 (2026-10) - Part II]] · [[system/ingest/set-2026-10-15]] |
  | 4A.1 | Permission: applications, ss. 55A–55M | pp. 102–150 | planned 2 |
  | 1A | The regulators | not located yet | planned 4 · compare: also in [[raw/uk-parliament-fsma-2000-part-1a.md#The Regulators]] |
  | VI | Official listing | not located yet | not compiled |
  ```
  Status is one of: `compiled <date>` or `compared <date>`, each with the part's source page and set review; `in progress` with its set review; `planned <n>`; `not compiled`. A part another raw file covers adds `· compare:` and a link to that file. Under the table: "Parts and what they cover, from the contents ([[raw/<name>.pdf#page=N]] to page N)", or "from the publisher's contents page ([[raw/<stem>-contents-<yyyy-mm>.md]])" for a contents companion. Where and Status describe the file and the wiki, not what the document says, and need no citation.
- `status` on the map follows A4.4, for its Summary and Covers.
- **Overview, index, log:** add the document to `overview.md` among the sources and the gaps, without a rewrite; a line for the map in `index.md`; the log entry as A7, "Pages: +1 new (the map)".
- **Capture list:** no ticks yet; lines are ticked as parts are compiled (§7).
- Tick `M`, finish the set review and report: the number of parts, the plan, and "Run `/clear`, then `/ingest part <document>` for part 1 of the plan." No `/lint` line yet, since nothing is compiled. Commit as A10 when I say the review is done.

## 5. A part run: brief (A1)
Short, and nothing written until I answer:
- the part, its pages or lines and its sections, located as §3 says, now if not before;
- the pages it touches, found by Grep of `wiki/` and `raw/` for its key terms;
- each `· AI` claim and each capture-list line it may back;
- likely conflicts, flags, and the question (what to emphasise). No move block.

## 6. A part run: compile (A3–A4)
- **Set review** as usual, topic `<title>, Part <label>`. Under "Plan and progress", one row per chunk, `1a`, `1b`, …: a chapter or cross-heading group, or at most 20 PDF pages (one Read) or about 500 lines, whichever ends first. Set the part's map row to `in progress` with the set review's link.
- **Read one chunk at a time,** with Read: `pages` for a PDF, `offset` and `limit` for Markdown. Never print a PDF to the terminal or save a converted copy.
- **The part's source page** is `wiki/sources/Source - <title> - Part <label>.md`, from the Source template, with this under the header line: `**Part of:** [[wiki/sources/Source - <title>]] · **Pages:** a–b · **Sections:** …`. Write it with the first chunk and add to it as each chunk is done. `sources` lists the raw file.
- **Every citation carries its place** (D-112): `([[raw/<name>.pdf#page=N]], s. 55E(2))` for legislation in a PDF; `([[raw/<name>.pdf#page=N]])` for a book, with the PDF's own page number from the page you read. In Markdown, link the heading the passage sits under, copied as written but without `# | ^ \ [ ] %`, then the section for legislation: `([[raw/uk-parliament-fsma-2000-part-1a.md#1LSupervision, monitoring and enforcementU.K.]], s. 1L(2))`.
- Entity, concept and conflict work runs as A4.2–A4.4. A claim marked `· AI` anywhere in the wiki that this part states is re-cited as A4.2 says: open the section and check it states all of the claim. Backed now, it also belongs on the page of its subject, if it isn't there yet (D-102).
- **Tick each chunk** with the date, and save the set review before the next. If the run stops, the next `/ingest` resumes at the first chunk not ticked: read the part's source page and the pages earlier chunks touched, and complete them. Never add a claim a page already makes from this file.
- **When the last chunk is done,** set the part's map row to `compiled <date>` with its links, fill in Where, update "Compiled: N of M parts", and set the map's `updated`.

## 7. A part run: finish (A5–A10)
- **A5:** revise only the paragraphs of `overview.md` this part bears on.
- **A6:** at most one draft, and only when the part changes the picture.
- **A7:** a line in `index.md` for the part's page, under the map's. Log: `## [YYYY-MM-DD] ingest | <title>, Part <label>`, then "Set: set-YYYY-MM-DD, 1 source, part <label> (pp. a–b) of N parts, primary." and the pages as usual. **Capture list:** tick a line whose link or title is this document, or a section or Part of it, once every section the line names sits in a compiled part: `- [x] … → [[raw/<name>]], Part <label>`. Until then, leave it as it is.
- **A9:** add "Part <label> done: N of M compiled. Next in the plan: Part <label>, pp. a–b." Then always: "Run `/clear`, then `/lint` before the next part. Then `/clear` and `/ingest part <document>`." (D-108)
- **A10:** one commit per part, after my review: `ingest: <title>, Part <label> (set-YYYY-MM-DD)`.

## 8. Overlaps and versions (D-110, D-111)
- **A consolidated text is dated by its "up to date" line.** Its raw name ends with that year and month: `uk-parliament-fsma-2000-2026-10.pdf`. A later capture is a **new version** (D-099), with the same stem and its own year and month.
- **A part already in another raw file** (the full Act, with Part 1A clipped earlier): both files stay. The map marks that part `compare`, with a heading or page link to the other file. Its part run is a compare:
  - Grep `wiki/` for every claim that cites the other file within the part, and find the same passage in this document.
  - Same wording: write nothing. The map row becomes `compared <date>: no change in N claims`.
  - Different wording: a conflict (A4.3), kind **newer** when this document is the later text, otherwise **fact**.
  - A claim the part makes that no page holds yet: write it as §6 says.
- **A new version of a mapped document** gets its own map. Parts compiled from the older version are marked `compare` against the older raw file and compared when I choose them; the others compile from the newest version. The older map says "Newer version: [[…]], ingested YYYY-MM-DD" under "Conflicts and open points".
- **A section or Part that arrives after the whole document,** such as a clipped section page, follows `import`'s verdict **part**. If it is the later text, it is a new version of that part, compiled as a set of one, and the claims it changes are **newer** conflicts.

## 9. The plan can change
When I say so, add a part to the plan, reorder it, or set a planned part back to `not compiled`. Only the map changes, with `updated`. A set always covers the map or exactly one part, so nothing waits half done except a stopped run, which `/ingest` resumes first.
