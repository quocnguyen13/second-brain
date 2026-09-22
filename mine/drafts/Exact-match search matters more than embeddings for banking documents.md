---
type: insight
status: draft
origin: claude
created: "2026-09-22"
related: ["[[wiki/concepts/BM25]]", "[[wiki/concepts/Retrieval-augmented generation]]", "[[wiki/concepts/Wiki index and log]]", "[[wiki/sources/Source - Contextual Retrieval]]"]
---
# Exact-match search matters more than embeddings for banking documents

If this vault, or a lending or payments knowledge base at work, ever needs search, BM25-style exact matching should come first and embeddings second. Banking questions often hinge on identifiers that embeddings blur.

## Why I think this
- Anthropic's own example of embeddings failing is an identifier ("Error code TS-999"), and it says BM25 is "particularly effective for queries that include unique identifiers or technical terms".
- Banking material is full of those: regulation article numbers, product and fee codes, scheme rule IDs, and error or reason codes in card and payment flows. That's my reading, not something a source says.
- Karpathy's suggested upgrade from `index.md` (qmd) is already hybrid BM25/vector, so choosing it doesn't mean a separate embedding project.

## Relations
- supports:: [[wiki/concepts/BM25]]
- contradicts::
- extends:: [[wiki/concepts/Wiki index and log]]
- source:: [[wiki/sources/Source - Contextual Retrieval]]
