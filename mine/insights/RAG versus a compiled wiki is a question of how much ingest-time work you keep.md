---
type: insight
status: active
origin: claude
created: "2026-09-25"
reviewed: "2026-09-25"
related: ["[[wiki/concepts/Compiled wiki]]", "[[wiki/concepts/Retrieval-augmented generation]]", "[[wiki/concepts/Contextual Retrieval]]", "[[wiki/sources/Source - Contextual Retrieval]]", "[[wiki/sources/Source - LLM Wiki]]"]
---
# RAG versus a compiled wiki is a question of how much ingest-time work you keep

Karpathy contrasts RAG, which keeps nothing between questions, with a wiki that compounds. Contextual Retrieval doesn't fit that binary: it runs the LLM over every chunk once, at ingest, and keeps the result. So the approaches sit on one scale, from nothing kept, to context per chunk, to synthesis across documents, and the question for any use is how far along it needs to go. For documentation that is mostly self-contained, per-chunk context may be enough; questions about how two documents interact are where compiling pays.

## Why I think this
- Karpathy: with RAG "the LLM is rediscovering knowledge from scratch on every question. There's no accumulation." ([[raw/karpathy-llm-wiki.md]])
- Anthropic: the generated context is "prepended to the chunk before embedding it and before creating the BM25 index", at a "one-time cost" ([[raw/anthropic-contextual-retrieval.md]]).
- The prompt gives the model the whole document and one chunk, and asks for context to "situate this chunk within the overall document" ([[raw/anthropic-contextual-retrieval.md]]).
- Anthropic also suggests custom prompts that include "a glossary of key terms that might only be defined in other documents", so per-chunk context can carry some knowledge from elsewhere ([[raw/anthropic-contextual-retrieval.md]]).
- (reasoning) What per-chunk context can't do is show that two sources disagree. That takes pages that compare sources, which is what this vault's `contested` pages are for.
- (reasoning) The reading for bank documentation is an extension; neither source discusses banking.

## Relations
- extends:: [[wiki/concepts/Compiled wiki]]
- extends:: [[wiki/concepts/Retrieval-augmented generation]]
- supports:: [[wiki/concepts/Contextual Retrieval]]
- source:: [[wiki/sources/Source - Contextual Retrieval]]
- source:: [[wiki/sources/Source - LLM Wiki]]
