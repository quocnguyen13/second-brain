---
type: concept
status: verified
sources: ["[[raw/anthropic-contextual-retrieval.md]]"]
created: "2026-09-22"
updated: "2026-09-22"
tags: ["information-retrieval"]
---
# Prompt caching

A Claude API feature that caches frequently used prompt content between API calls so it doesn't have to be reprocessed each time ([[raw/anthropic-contextual-retrieval.md]]).

## What the sources say
- Anthropic says it reduces latency by "> 2x" and costs by "up to 90%"; the post gives no conditions for these figures beyond caching "frequently used prompts between API calls" ([[raw/anthropic-contextual-retrieval.md]]).
- It makes the no-retrieval option more practical: for knowledge bases under 200,000 tokens, put the whole knowledge base in the prompt ([[raw/anthropic-contextual-retrieval.md]]).
- It makes [[wiki/concepts/Contextual Retrieval]] cheap: the document is cached once and each chunk's request references it, giving $1.02 per million document tokens under the assumptions stated there ([[raw/anthropic-contextual-retrieval.md]]).

## Where sources disagree
- None found.

## Mentioned in
- [[wiki/sources/Source - Contextual Retrieval]]

## Related
- [[wiki/concepts/Retrieval-augmented generation]]
- [[wiki/concepts/Contextual Retrieval]]
- [[wiki/entities/Anthropic]]
