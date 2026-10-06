<!-- Supporting file of the ingest skill. SKILL.md A0 sends you here when a set holds a Claude output. Mirrored in mine/projects/thinking-system/40 Claude Operating Instructions §4.1; change both in the same commit. -->

# A Claude output in the set

What changes when one file in the set is a Claude output: a chat answer, a research report from claude.ai or from `/research`, an artifact. Everything this file doesn't mention runs as `SKILL.md` says.

**The rule.** A Claude output is a source at level AI. It is never the evidence for a claim that `raw/` can back, and it never makes a page `verified`. Each of its claims is checked against `raw/` before it reaches a page (D-075).

**No web here.** `/ingest` stays inside the vault. Never search or fetch while compiling. The sources the output names go on the capture list; `/research` looks for the rest.

## 1. In the brief (A1)
- **Level:** `ai`, type "Claude output". No other level applies, whatever the output cites.
- **Raw name:** `claude-<YYYY-MM-DD>-<topic>.md`, with the date the output was made. A file already named that way keeps its name; a `/research` report named `research-…` takes this form as it moves.
- **Date:** its `created` property, or the date in its name.
- Under the Sources table, add an **AI source** block:
  - its sections, with a rough count of the statements of fact in each;
  - the sources it names (footnotes, links, a bibliography): how many, and which are already in `raw/`;
  - what you'll leave out: its study plans, advice, questions to the reader, opinions and predictions. Those aren't claims of fact;
  - if it holds more than about 60 statements of fact, say that it compiles section by section and may take more than one session.
- Don't run the full check in the brief. It happens as you compile, so it is recorded as it goes.
- A diagram in the output is a set of claims, one per arrow or box. Check them as claims; don't copy the diagram into the wiki.

## 2. Plan and order (A3)
- Compile the Claude output last, after every other source in the set, so its claims meet what stronger sources have put on the pages.
- In "Plan and progress" give it one row per section: `4a`, `4b`, … Tick each section as you finish it. A run that stops resumes at the first section not ticked.
- Write its source page with the first section, titled `Source - Claude on <topic> (<YYYY-MM-DD>)`, and add to it as each section is done.

## 3. Check each statement, then write by outcome (A4)
Take one section at a time. For each statement of fact, search `raw/`:
- Grep the Markdown sources for its names, figures and terms.
- Grep can't search a PDF. Grep `wiki/` for the same terms, and open the PDF page that a wiki page cites for the point.
- **Open the passage.** A claim is backed only when the passage says all of it: the figure, the date and the scope. A source that the output cites is not a passage you have read.

| Outcome | When | What you write |
|---|---|---|
| **backed** | A passage in `raw/` states it | The claim cites that raw file, with its page or section and that source's level marker, never the Claude output. If the page already states the claim, add nothing |
| **unbacked** | Nothing in `raw/` states it, and nothing contradicts it | The claim, one fact per sentence, citing the output: `([[raw/claude-…]] · AI)` |
| **contradicted** | A passage in `raw/` says otherwise | Nothing on entity, concept or overview pages. Record it in the set review and on the output's source page |
| **not a claim of fact** | A plan, advice, an opinion, a prediction, a question | Nothing. Count it |

- A claim backed in part is split: the backed part cites `raw/`, the rest is unbacked.
- A contradicted claim is not a conflict for me to decide: an AI claim never outweighs a source. If you think the source is the one that's wrong, say so under Flags.
- Write unbacked claims so that a later source can back them one sentence at a time.

**Pages**
- The output's source page: `trust: ai`. Under Key claims, group them: "Backed by raw/", each citing its raw file; "Unbacked (AI)", each citing the output with `· AI`. Under "Conflicts and open points", list each contradicted claim with what `raw/` says and its citation, ending "Left out of the wiki." `sources` lists the output and every raw file a backed claim cites.
- A new entity or concept page whose every claim is `· AI` opens, under the title, with: `> [!warning] AI only: no source in raw/ backs this page yet.` Remove the line when one does.
- **Status** follows A4.4: any `· AI` claim leaves its page `unverified`. That includes the output's own source page while one of its key claims is unbacked.

## 4. The capture list (A7)
For each unbacked claim whose source the output names, add a line under `## To clip` in `system/research/capture.md`, unless that source is already in `raw/` or on the list:
`- [ ] YYYY-MM-DD <title> · <publisher> · <date> · <URL> · <level> · <Web Clipper | PDF download> · [[raw/claude-…]]`
One line per source, however many claims it would back. Primary sources first. Take the title, publisher and link from the output as it gives them; a source the output names without a link is listed with "no link given".

## 5. The set review (A8)
After Conflicts, add:

```
## AI source check
[[raw/claude-…]] · N statements read
- **Backed by raw/ · N:** N already on the pages; N added, listed under Facts by trust at their source's level
- **Unbacked · N:** kept and marked `· AI`, listed under Facts by trust → AI. N have a source on the capture list. N name none: `/research` on its own looks for them
- **Contradicted by raw/ · N**, left out:
  - "<the claim>" · raw says: <what the passage says> ([[raw/<name>]], s. N)
- **Not claims of fact · N**, left out: <the kinds, such as a study plan or a reading list>
```

- The Result line ends with "· N AI claims waiting".
- "Check first" gains one backed claim to trace: the output's sentence, then the raw passage it now cites.
- The log entry counts the output on its own: "N sources (N primary, N secondary, N commentary, 1 AI)", and ends "AI claims: N backed, N unbacked, N contradicted."

## 6. The report (A9)
Add: the four counts; each page left `unverified` by `· AI` claims; how many sources went on the capture list. Then, after the usual closing line: "The `· AI` claims are leads, not facts. Clip the sources on the capture list and run `/ingest`, or run `/research` on its own for the ones with no source named."

## 7. Later sets
When a later set brings a source that states an `· AI` claim, A4.2 re-cites the claim to that source and the marker goes. Nothing in this file runs then.
