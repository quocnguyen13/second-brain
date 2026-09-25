---
type: insight
status: active
origin: claude
created: "2026-09-25"
reviewed: "2026-09-25"
related: ["[[wiki/concepts/BM25]]", "[[wiki/concepts/Contextual Retrieval]]", "[[wiki/concepts/Retrieval-augmented generation]]", "[[wiki/concepts/Wiki index and log]]", "[[wiki/sources/Source - Contextual Retrieval]]"]
---
# Banking document search needs exact match alongside embeddings, not instead of them

Questions about banking material often turn on an identifier, such as a regulation article, a fee or product code, or a card-scheme reason code, and embeddings can blur exactly those. That makes lexical (BM25) matching a requirement. It doesn't make embeddings optional: Anthropic's results show the two work best together. The rule is hybrid by default, and the upgrade path this vault already names for `index.md`, qmd, is hybrid.

## Why I think this
- Anthropic: embeddings "can miss crucial exact matches", and BM25 is "particularly effective for queries that include unique identifiers or technical terms" ([[raw/anthropic-contextual-retrieval.md]]).
- Their example: for "Error code TS-999", an embedding model "might find content about error codes in general, but could miss the exact "TS-999" match" ([[raw/anthropic-contextual-retrieval.md]]).
- Their findings: "Embeddings+BM25 is better than embeddings on their own", and "All these benefits stack" ([[raw/anthropic-contextual-retrieval.md]]).
- Karpathy's suggested search tool, qmd, offers "hybrid BM25/vector search and LLM re-ranking" ([[raw/karpathy-llm-wiki.md]]).
- (reasoning) Banking material is full of identifiers: regulation article numbers, fee and product codes, scheme rule IDs, and reason codes in card and payment flows.
- (reasoning) Anthropic's figures are a vendor's own benchmarks on its own models. The direction is what matters here, not the numbers.

## Relations
- supports:: [[wiki/concepts/BM25]]
- supports:: [[wiki/concepts/Contextual Retrieval]]
- extends:: [[wiki/concepts/Retrieval-augmented generation]]
- extends:: [[wiki/concepts/Wiki index and log]]
- source:: [[wiki/sources/Source - Contextual Retrieval]]
