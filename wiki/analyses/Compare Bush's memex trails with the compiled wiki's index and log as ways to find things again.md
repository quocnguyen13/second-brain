---
type: analysis
status: verified
sources: ["[[raw/bush-as-we-may-think.pdf]]", "[[raw/karpathy-llm-wiki.md]]"]
created: "2026-10-20"
updated: "2026-10-20"
tags: ["memex", "compiled-wiki"]
---
# Compare Bush's memex trails with the compiled wiki's index and log as ways to find things again

**Question:** Compare Bush's memex trails with the compiled wiki's index and log as ways to find things again.

## Answer
They answer different finding needs. A trail is a path the user builds by hand, joining items one at a time: it is named, recorded in a code book, stepped through in order, branched, annotated and shared. It finds things again by replaying a line of thought. The index is a catalog of every page by category with a one-line summary, read first to locate pages: it finds things by what they are about. The log is a dated, append-only record of operations: it finds when something happened to the wiki, not content. The memex itself had index-style lookup too, by tapping a book's code, and trails were found through the code book, so Bush paired a catalog with trails. In the compiled wiki, the nearer match to trails is the cross-references the LLM maintains between pages, not the index or the log. The main difference is upkeep: Bush's user builds the trails; the LLM keeps the index, log and cross-references current.

## Evidence
- To build a trail the user names it, enters the name in a code book, and joins two items with one key press. The join is permanent; when either item is in view, the other is recalled with one button ([[raw/bush-as-we-may-think.pdf#page=16]]), via [[wiki/concepts/Associative indexing]]
- Joined items form a trail that can be reviewed in turn like a book; the user adds comments and branches off on side trails ([[raw/bush-as-we-may-think.pdf#page=16]]), via [[wiki/concepts/Memex]]
- Years later, a touch brings up the code book, a few keys project the head of the trail, and the user can photograph the whole trail out and pass it to a friend to link into their own memex ([[raw/bush-as-we-may-think.pdf#page=17]]), via [[wiki/concepts/Memex]]
- The memex also supports "the usual scheme of indexing": the user taps a book's code and its title page appears ([[raw/bush-as-we-may-think.pdf#page=15]]), via [[wiki/concepts/Memex]]
- Bush expects a profession of "trail blazers" who establish useful trails through the common record ([[raw/bush-as-we-may-think.pdf#page=17]]), via [[wiki/sources/Source - As We May Think]]
- `index.md` is content-oriented: every page with a link and one-line summary, by category, updated on every ingest; the LLM reads it first when answering, then drills into pages. This works at ~100 sources without embedding-based RAG ([[raw/karpathy-llm-wiki.md]]), via [[wiki/concepts/Wiki index and log]]
- `log.md` is chronological and append-only: a record of ingests, queries and lint passes, giving a timeline of the wiki's evolution; a consistent entry prefix makes it greppable ([[raw/karpathy-llm-wiki.md]]), via [[wiki/concepts/Wiki index and log]]
- The LLM creates and updates the wiki's pages and maintains cross-references between them ([[raw/karpathy-llm-wiki.md]]), via [[wiki/concepts/Compiled wiki]]
- The gist calls itself "related in spirit to" the memex, "with associative trails between documents", and says the part Bush couldn't solve was who does the maintenance, which the LLM handles ([[raw/karpathy-llm-wiki.md]]), via [[wiki/concepts/Compiled wiki]]

## Caveats and gaps
- No source compares trails with the index and log directly. The mapping in the Answer, including cross-references as the nearer match to trails, is this page's reasoning from the Evidence.
- [[wiki/concepts/Associative indexing]] is `contested` (Bush vs PARA's one home per item). The dispute is about organising, not about how trails work, so this page carries no disputed claim.
- Nothing in the wiki tests which approach finds things better.

## Related
- [[wiki/concepts/Memex]]
- [[wiki/concepts/Associative indexing]]
- [[wiki/concepts/Wiki index and log]]
- [[wiki/concepts/Compiled wiki]]
- [[wiki/sources/Source - As We May Think]]
