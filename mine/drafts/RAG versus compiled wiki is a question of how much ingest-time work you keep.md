---
type: insight
status: draft
origin: claude
created: "2026-09-22"
checked: "2026-09-25"
related: ["[[wiki/concepts/Compiled wiki]]", "[[wiki/concepts/Retrieval-augmented generation]]", "[[wiki/concepts/Contextual Retrieval]]", "[[wiki/sources/Source - Contextual Retrieval]]", "[[wiki/sources/Source - LLM Wiki]]"]
---
# RAG versus compiled wiki is a question of how much ingest-time work you keep

Karpathy's case rests on RAG doing no LLM work before a question is asked. Contextual Retrieval breaks that premise: it runs the LLM once per chunk at ingest and keeps the result. So the two approaches sit on one scale, from none of the reading kept, to per-chunk context kept, to cross-document synthesis kept, and the real question is how far along it a given use case needs to go.

## Why I think this
- The gist's contrast is "no accumulation" in RAG versus a wiki that compounds; in Anthropic's method, an LLM generates context for each chunk once at preprocessing, and that context is prepended to the chunk before embedding and before building the BM25 index. The binary no longer holds as stated.
- What Contextual Retrieval keeps is narrow: context within one document. It won't surface that two sources disagree, which is exactly what this vault's lint and `contested` status exist for.
- Practical reading for a bank: policy and product documentation that is mostly self-contained per document probably only needs per-chunk context; questions that span documents (e.g. how two policies interact) are where compiling pays.

## Relations
- supports:: [[wiki/concepts/Contextual Retrieval]]
- contradicts:: [[wiki/concepts/Compiled wiki]]
- extends:: [[wiki/concepts/Retrieval-augmented generation]]
- source:: [[wiki/sources/Source - Contextual Retrieval]]

## Check 2026-09-25
**Evidence:** 2 problems
- Karpathy's case rests on RAG building nothing before the question → holds, uncited · raw/karpathy-llm-wiki.md line 20
- Quote "no accumulation" → holds, uncited · raw/karpathy-llm-wiki.md line 20
- Contextual Retrieval runs the LLM once per chunk at preprocessing and keeps the result → holds, uncited · raw/anthropic-contextual-retrieval.md lines 84–97, 109 ("one-time cost")
- Context is prepended before embedding and before the BM25 index → holds, uncited · raw/anthropic-contextual-retrieval.md lines 70, 97
- What it keeps is context within one document → holds, uncited · raw/anthropic-contextual-retrieval.md line 84
- The vault's lint and `contested` status exist for sources that disagree → holds · `CLAUDE.md`, Citation discipline
- Left out: Anthropic suggests custom prompts with "a glossary of key terms that might only be defined in other documents", so per-chunk context can carry some cross-document knowledge · raw/anthropic-contextual-retrieval.md line 134
- `contradicts::` [[wiki/concepts/Compiled wiki]] doesn't match: the page already records this disagreement under "Where sources disagree"; the draft agrees with the page and contradicts Karpathy's premise
**Reasoning, not in a source:** the two approaches sit on one scale; Contextual Retrieval won't surface disagreements between sources; self-contained bank policy docs need only per-chunk context, cross-document questions need compiling
**Leans on:** [[wiki/concepts/Compiled wiki]] · contested: whether RAG builds nothing up; [[wiki/concepts/Retrieval-augmented generation]] · contested: the same point, and RAG as the thing to replace or improve
**Links:** 1 mismatched Relations line (see above)
**Overlaps:** none
