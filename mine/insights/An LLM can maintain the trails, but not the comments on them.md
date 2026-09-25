---
type: insight
status: active
origin: claude
created: "2026-09-25"
reviewed: "2026-09-25"
related: ["[[wiki/concepts/Memex]]", "[[wiki/concepts/Associative indexing]]", "[[wiki/concepts/Compiled wiki]]", "[[wiki/sources/Source - As We May Think]]", "[[wiki/sources/Source - LLM Wiki]]"]
---
# An LLM can maintain the trails, but not the comments on them

Bush's memex did two jobs on one trail: it joined items from the record, and it let the user insert comments and analysis of their own. Karpathy's point is that the LLM takes over the first job, the maintenance Bush couldn't solve. The second job doesn't move with it: the gist still leaves sourcing, exploration and questions to the person. A compiled wiki therefore needs a layer the LLM doesn't write, which in this vault is `mine/`.

## Why I think this
- Bush's user joins two items on adjacent viewing positions with a single key, and the joined items form a trail that can be reviewed in turn ([[raw/bush-as-we-may-think.pdf#page=16]]).
- On the same trail he "inserts a comment of his own" ([[raw/bush-as-we-may-think.pdf#page=16]]), and later "a page of longhand analysis of his own" ([[raw/bush-as-we-may-think.pdf#page=17]]).
- Karpathy: the part Bush "couldn't solve was who does the maintenance. The LLM handles that." ([[raw/karpathy-llm-wiki.md]])
- Karpathy: the LLM writes and maintains the wiki, and "You're in charge of sourcing, exploration, and asking the right questions." ([[raw/karpathy-llm-wiki.md]])
- (reasoning) The maintenance the gist hands over is joining and cross-referencing. The user's own comments are the other half of Bush's trail, and nothing in the gist hands them over.
- (reasoning) This vault draws the same line: `wiki/` is the maintained trail, `mine/` holds the comments.

## Relations
- extends:: [[wiki/concepts/Memex]]
- extends:: [[wiki/concepts/Associative indexing]]
- supports:: [[wiki/concepts/Compiled wiki]]
- source:: [[wiki/sources/Source - As We May Think]]
- source:: [[wiki/sources/Source - LLM Wiki]]
