---
type: insight
status: draft
origin: claude
created: "2026-09-22"
checked: "2026-09-25"
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

## Check 2026-09-25
**Evidence:** 1 problem
- Anthropic's example of embeddings failing is "Error code TS-999" → holds, uncited · raw/anthropic-contextual-retrieval.md line 41
- Quote "particularly effective for queries that include unique identifiers or technical terms" → holds, uncited · raw/anthropic-contextual-retrieval.md line 37
- Karpathy's suggested upgrade, qmd, is hybrid BM25/vector → holds, uncited · raw/karpathy-llm-wiki.md line 64
- Left out: Anthropic recommends combining the two, not ranking them: "Embeddings+BM25 is better than embeddings on their own", and the benefits stack · raw/anthropic-contextual-retrieval.md lines 52, 172–177
**Reasoning, not in a source:** banking material is full of identifiers (labelled in the draft); therefore BM25 first, embeddings second
**Leans on:** [[wiki/concepts/Retrieval-augmented generation]] · contested: whether RAG accumulates anything, and RAG as the thing to replace or improve
**Links:** fine
**Overlaps:** [[The index file will need to become a search index before 100 sources]] · builds on
