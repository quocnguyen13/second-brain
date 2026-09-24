---
name: file-answer
description: File the answer just given in this session as a page in wiki/analyses/. Runs only when I type /file-answer.
disable-model-invocation: true
argument-hint: "[title]"
---
<!-- Mirrored in mine/projects/thinking-system/08 Claude Operating Instructions §4; change both in the same commit. -->

# /file-answer

Turn the answer you just gave in this session into an analysis page, so the next question can build on it. `CLAUDE.md` and `system/conventions.md` apply throughout; this file is the procedure.

**Ground rules for the whole run**
- Look around with your file tools (Glob, Grep, Read), not shell commands.
- Write only the new page in `wiki/analyses/`, the `Related` lists of the pages it drew on, `index.md` and `log.md`. Nothing in `mine/`, no working files.
- Never delete anything.
- If a tool or program is missing, say so in the report and carry on without it. Never install anything, and never ask to.

## 0. Find the answer
- Take the most recent answer you gave in this session, from `/ask` or from a question I asked directly.
- No answer in this session → say "No answer in this session to file. Run /ask first." and stop. Don't rebuild one from memory of another session.
- If the answer began "Nothing in the wiki on this", say it has no evidence to file and stop.

## 1. Check for an existing page
- Read the Analyses section of `index.md` and Glob `wiki/analyses/`.
- If a page already answers the same question, say so and ask whether to update it or file a new one. Wait for my reply.

## 2. Confirm the evidence in raw/
This page is new synthesis, so its evidence is checked again at the source before it's written.
- For each Evidence bullet, open the cited passage in `raw/` and confirm it supports the claim as worded. A PDF citation keeps its page: `([[raw/<name>.pdf#page=N]])`.
- Claim confirmed → keep it. Claim not in the passage → drop it, or reword it to what the passage says, and list it in the report.
- A claim with no raw citation (general knowledge, or a page that cites nothing for it) goes under "Caveats and gaps", labelled "(general knowledge)" or "(uncited on [[page]])".
- A raw file that won't open, even with page ranges: keep the claim under "Caveats and gaps", labelled "(not re-checked: <file> wouldn't open)". The page is then `unverified`.

## 3. Write the page
- Read `system/templates/Analysis template.md` first.
- **Title:** the question as I asked it, or the claim the answer makes, in plain language; mine if I typed one after the command. None of `# ^ [ ] | \ / : * " < > ?`.
- **Question:** the question word for word.
- **Answer:** the conclusion in a short paragraph. It may combine the evidence and draw a conclusion from it; it adds no facts that aren't in Evidence.
- **Evidence:** one bullet per claim, citing the raw file directly, with the wiki page it came from for context: `- Claim ([[raw/<name>]]), via [[wiki/concepts/<Page>]]`.
- **Where sources disagree:** both positions with their raw citations, if the answer carries a disputed claim. Leave the heading out otherwise.
- **Caveats and gaps:** what the wiki doesn't cover, uncited points from step 2, and any source that would settle an open point.
- **Related:** every wiki page the answer drew on, including the page behind each position under "Where sources disagree". These are links for context, never evidence.
- Properties: `sources` lists every raw file cited; `created` and `updated` today; one or two tags reused from the pages it drew on.

## 4. Set status
- `verified` when every claim in Evidence cites a file in `raw/` and nothing uncited sits in Answer.
- `unverified` if anything in Answer or Evidence lacks a raw citation, or a claim couldn't be re-checked in step 2.
- `contested` if the page carries a claim two sources disagree on, shown both ways (D-047).
- The Answer's conclusion is this page's reasoning from its own Evidence. It needs no separate citation, but it can't go beyond that evidence.

## 5. Link it in
- On each page listed under Related, add the analysis to that page's `Related` list and set `updated` to today. Change nothing else on those pages.
- `index.md`: add a line under Analyses: `- [[wiki/analyses/<title>]] — one-line answer (N sources)`.
- `log.md`: append
  ```
  ## [YYYY-MM-DD] file | <title>
  Pages: +1 analysis, N updated (Related links). Status: <status>. <claims dropped or reworded in step 2, or "Evidence confirmed in raw/.">
  ```

## 6. Report, then stop
Before reporting, check every `[[wiki/...]]` link on the new page points to a page that exists, under its exact file name.
- **Created:** the analysis page and its status
- **Evidence check:** claims confirmed, and any dropped or reworded, with why
- **Linked from:** the pages whose Related list changed
- **Check first:** one Evidence bullet for me to trace to its raw file
- Then remind me to review the page in Obsidian and commit: `git add -A`, `git diff --staged`, then `git commit -m "file: <title>"`.
