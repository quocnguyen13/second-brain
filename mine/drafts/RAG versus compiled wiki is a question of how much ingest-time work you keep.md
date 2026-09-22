---
type: insight
status: draft
origin: claude
created: "2026-09-22"
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
