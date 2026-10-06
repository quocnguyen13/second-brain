---
type: overview
status: verified
sources: ["[[raw/karpathy-llm-wiki.md]]", "[[raw/bush-as-we-may-think.pdf]]", "[[raw/matuschak-evergreen-notes.md]]", "[[raw/anthropic-contextual-retrieval.md]]", "[[raw/forte-para-method.md]]", "[[raw/uk-parliament-fsma-2000-part-1a.md]]", "[[raw/fca-about-the-fca.md]]"]
created: "2026-09-22"
updated: "2026-10-06"
tags: ["compiled-wiki", "knowledge-management", "memex", "note-taking", "information-retrieval", "uk-financial-regulation"]
---
# Overview

The current picture across every source, on one page. Rewritten at each ingest, not appended to.

The wiki now has two strands that don't yet touch:
- **Knowledge management:** five sources on how to build and organise a knowledge base.
- **UK financial regulation:** two primary sources, the statute that sets up the FCA and the PRA, and the FCA's own account of itself.

Regulation agreements and disagreements sit in Strand 1. The sections from "Where sources agree" on apply to the knowledge-management strand.

## Strand 1: UK financial regulation
- **FSMA 2000 Part 1A.** [[wiki/sources/Source - FSMA 2000 Part 1A]] sets up the two regulators and their relationship ([[raw/uk-parliament-fsma-2000-part-1a.md]]):
  - the [[wiki/entities/Financial Conduct Authority]]
  - the [[wiki/entities/Prudential Regulation Authority]], which is the [[wiki/entities/Bank of England]] acting through its Prudential Regulation Committee
  - the relationship between them
- **About the FCA.** [[wiki/sources/Source - About the FCA]] is the FCA's own page: its scale, its methods, its funding and its accountability ([[raw/fca-about-the-fca.md]]).
- **Who regulates whom.** The FCA supervises every authorised person. The PRA supervises only those whose permission includes at least one PRA-regulated activity. Those firms are dual-regulated; the rest answer to the FCA alone ([[raw/uk-parliament-fsma-2000-part-1a.md]], ss. 1L, 2B(5), 2K). See [[wiki/concepts/Solo and dual regulation]].
- **How many firms.** These are the FCA's figures as of 2026-07-09 ([[raw/fca-about-the-fca.md]]):
  - conduct regulation: ~35,500 firms
  - FCA prudential supervision: ~34,000 firms
  - subject to the FCA Handbook's prudential standards: ~14,000 firms
  - PRA prudential regulation: ~1,500 banks, building societies, credit unions, insurers and major investment firms (the FCA's figure)
- **How the FCA works.** It makes rules and runs market studies. It authorises firms against requirements, supervises them proportionately by risk, and enforces, up to criminal prosecution ([[raw/fca-about-the-fca.md]]). It is funded by fees from regulated firms and is accountable to the Treasury and Parliament ([[raw/fca-about-the-fca.md]]).
- **Different jobs.** [[wiki/concepts/Regulatory objectives]]:
  - The FCA works for well-functioning markets through consumer protection, integrity and competition ([[raw/uk-parliament-fsma-2000-part-1a.md]], s. 1B).
  - The PRA works for the safety and soundness of firms, and explicitly not for zero failures ([[raw/uk-parliament-fsma-2000-part-1a.md]], ss. 2B, 2G).
  - Since 2023 both carry a secondary competitiveness and growth objective ([[raw/uk-parliament-fsma-2000-part-1a.md]], ss. 1EB, 2H).
  - **Agreement.** The FCA's own page lists the same strategic, operational and secondary objectives as the Act ([[raw/fca-about-the-fca.md]], [[raw/uk-parliament-fsma-2000-part-1a.md]], s. 1B).
- **For products.** The FCA's reach is set by [[wiki/concepts/Regulated financial services]], which names payment services and e-money directly ([[raw/uk-parliament-fsma-2000-part-1a.md]], s. 1H(2)). Its [[wiki/concepts/Consumer protection objective]] weighs product risk, consumer capability and consumer responsibility against firms' duty of care ([[raw/uk-parliament-fsma-2000-part-1a.md]], s. 1C(2)).
- **Coordination.** [[wiki/concepts/FCA-PRA coordination]]:
  - a duty to consult where one regulator's action may harm the other's objectives
  - a memorandum of understanding reviewed every year
  - a one-way PRA power to stop FCA action on stability grounds
  - two-way directions for consolidated group supervision
  - Treasury orders drawing the boundary between the regulators

  ([[raw/uk-parliament-fsma-2000-part-1a.md]], ss. 3D–3M)
- **Treasury levers.** [[wiki/entities/HM Treasury]] holds the political levers: recommendations, reviews, directed rule reviews, and requirements to make rules ([[raw/uk-parliament-fsma-2000-part-1a.md]], ss. 1JA, 1S, 3RC, 3RE).
- **Origins, scoped.** In law the FCA is the Financial Services Authority, renamed ([[raw/uk-parliament-fsma-2000-part-1a.md]], s. 1A(1)). It began operating as the FCA on 1 April 2013 ([[raw/fca-about-the-fca.md]]). This looked like a conflict and was resolved by scope on 2026-10-06.
- **Open points.**
  - Which activities are PRA-regulated: s. 22A isn't in either source.
  - Which of the two texts of the s. 3B(1)(c) principle applies where.
  - How the FCA's ~34,000 prudentially supervised firms relate to the ~14,000 under its Handbook's prudential standards.

## Strand 2: knowledge management
- **LLM Wiki.** [[wiki/sources/Source - LLM Wiki]] describes the compiled-wiki pattern that this vault implements:
  - three layers: raw sources, wiki, schema
  - three operations: ingest, query, lint
  - navigation through an index and a log ([[raw/karpathy-llm-wiki.md]])
- **As We May Think.** [[wiki/sources/Source - As We May Think]] (1945) argues that one-path indexing can't keep up with a growing record. It proposes the [[wiki/concepts/Memex]], built on [[wiki/concepts/Associative indexing]] ([[raw/bush-as-we-may-think.pdf#page=14]]): any two items can be permanently linked, and the trails that result can be replayed, branched and shared ([[raw/bush-as-we-may-think.pdf#page=16]], [[raw/bush-as-we-may-think.pdf#page=17]]).
- **Evergreen notes.** [[wiki/sources/Source - Evergreen notes]] defines [[wiki/concepts/Evergreen notes]]: notes that accumulate across projects, under five principles, aimed at "better thinking" ([[raw/matuschak-evergreen-notes.md]]). The clip is a hub page and states the principles by title only.
- **Contextual Retrieval.** [[wiki/sources/Source - Contextual Retrieval]] argues for retrieval rather than compiling:
  - below 200,000 tokens, put the whole knowledge base in the prompt
  - above that, use [[wiki/concepts/Retrieval-augmented generation]], improved by [[wiki/concepts/Contextual Retrieval]], [[wiki/concepts/BM25]] and [[wiki/concepts/Reranking]] ([[raw/anthropic-contextual-retrieval.md]])
- **The PARA Method.** [[wiki/sources/Source - The PARA Method]] is the first source about organising working material, not knowledge. The [[wiki/concepts/PARA method]] files everything into Projects, Areas, Resources and Archives. It puts [[wiki/concepts/Organizing by actionability]] first, meaning by current projects and goals rather than by subject, and it insists that projects (which end) be kept apart from areas (which don't) ([[raw/forte-para-method.md]]).

## Where sources agree
- **Subject classification fails as a way to find things.**
  - Bush: one fixed classification path ([[raw/bush-as-we-may-think.pdf#page=14]]).
  - Forte: "rummaging through a vast category like 'Psychology'" ([[raw/forte-para-method.md]]).
- **Association over hierarchy, as a principle for knowledge.**
  - Bush sets associative trails against single-path filing ([[raw/bush-as-we-may-think.pdf#page=14]]).
  - Matuschak prefers associative ontologies to hierarchical taxonomies ([[raw/matuschak-evergreen-notes.md]]).
  - Forte dissents (see below).
- **Accumulation.**
  - The gist calls the wiki "a persistent, compounding artifact" ([[raw/karpathy-llm-wiki.md]]).
  - Evergreen notes "accumulate over time, across projects" ([[raw/matuschak-evergreen-notes.md]]).
- **Simplicity of upkeep.**
  - Forte: a system as complex as your life eats the time it should save ([[raw/forte-para-method.md]]).
  - The gist hands upkeep to the LLM because humans abandon wikis when maintenance outgrows value ([[raw/karpathy-llm-wiki.md]]).
- **Memex as a kindred idea.** The gist calls itself "related in spirit to" the [[wiki/concepts/Memex]], with the LLM doing the upkeep Bush left to people ([[raw/karpathy-llm-wiki.md]], [[raw/bush-as-we-may-think.pdf#page=17]]).
- **Small corpora don't need RAG.**
  - The gist reads an index at around 100 sources ([[raw/karpathy-llm-wiki.md]]).
  - Anthropic puts everything in the prompt under 200,000 tokens ([[raw/anthropic-contextual-retrieval.md]]).
- **The search stack, when one is needed.** Both recommend hybrid BM25/vector search plus reranking ([[raw/karpathy-llm-wiki.md]], [[raw/anthropic-contextual-retrieval.md]]).

## How the units, links and organising axis compare
- **Unit.**
  - Bush: items already on the record ([[raw/bush-as-we-may-think.pdf#page=16]]).
  - Compiled wiki: entity or concept pages ([[raw/karpathy-llm-wiki.md]]).
  - Evergreen notes: an atomic note ([[raw/matuschak-evergreen-notes.md]]).
  - RAG: a chunk of a few hundred tokens ([[raw/anthropic-contextual-retrieval.md]]).
  - PARA: a file or note inside a project, area, resource or archive folder ([[raw/forte-para-method.md]]).
- **Links.**
  - Bush: ordered trails ([[raw/bush-as-we-may-think.pdf#page=16]]).
  - Compiled wiki: cross-references maintained by the LLM ([[raw/karpathy-llm-wiki.md]]).
  - Evergreen notes: dense links ([[raw/matuschak-evergreen-notes.md]]).
  - RAG: none, only similarity ([[raw/anthropic-contextual-retrieval.md]]).
  - PARA: none described. Location does the work ([[raw/forte-para-method.md]]).
- **Organising axis.**
  - Compiled wiki: topic, meaning entities and concepts ([[raw/karpathy-llm-wiki.md]]).
  - Evergreen notes: concept ([[raw/matuschak-evergreen-notes.md]]).
  - PARA: actionability, meaning projects first ([[raw/forte-para-method.md]]).

## Where sources disagree
- **Hierarchy by project, or associative ontology.** Contested on [[wiki/concepts/PARA method]], [[wiki/concepts/Organizing by actionability]], [[wiki/concepts/Evergreen notes]] and [[wiki/concepts/Associative indexing]].
  - Forte files each item in one home in a four-category hierarchy, by project, so "you'll know exactly where to put everything, and exactly where to find it" ([[raw/forte-para-method.md]]).
  - Matuschak prefers "associative ontologies to hierarchical taxonomies" and "concept-oriented" notes that outlive projects ([[raw/matuschak-evergreen-notes.md]]).
  - Bush calls single-path filing artificial ([[raw/bush-as-we-may-think.pdf#page=14]]).
  - Scope: Forte is organising material for action; the others are linking ideas and records for thinking and recall ([[raw/forte-para-method.md]], [[raw/matuschak-evergreen-notes.md]], [[raw/bush-as-we-may-think.pdf#page=14]]).
- **Does RAG build anything up?** Contested on [[wiki/concepts/Compiled wiki]] and [[wiki/concepts/Retrieval-augmented generation]].
  - The gist: "There's no accumulation" ([[raw/karpathy-llm-wiki.md]]).
  - Anthropic: an LLM generates per-chunk context once, at preprocessing ([[raw/anthropic-contextual-retrieval.md]]).
- **Replace retrieval or improve it.**
  - The gist offers the compiled wiki as the alternative ([[raw/karpathy-llm-wiki.md]]).
  - Anthropic treats RAG as the default at scale ([[raw/anthropic-contextual-retrieval.md]]).
  - Not a head-to-head result.
- **Open tensions, not contested.**
  - Who writes: Matuschak says yourself ([[raw/matuschak-evergreen-notes.md]]); the gist says the LLM ([[raw/karpathy-llm-wiki.md]]).
  - Topic pages vs. project folders: the compiled wiki's concept pages ([[raw/karpathy-llm-wiki.md]]) vs. PARA's projects-first order ([[raw/forte-para-method.md]]). Neither source addresses the other.

## Gaps worth a new source
- FSMA s. 22A and the PRA-Regulated Activities Order: the list of activities that makes a firm dual-regulated.
- A PRA source on its own firm population, to check the FCA's figure of ~1,500.
- The FCA's approach to supervision and its prudential supervision page: what "prudentially supervise" and "subject to the prudential standards" each cover.
- The Financial Services Act 2012: how the FSA became the FCA on 1 April 2013.
- The current FCA–PRA memorandum of understanding (s. 3E): how coordination works in practice.
- FCA conduct rules that build on the consumer protection objective for lending, cards and payments, such as the Consumer Duty and the consumer credit sourcebook, plus the Payment Services Regulations 2017.
- The rest of FSMA: Schedules 1ZA and 1ZB, and Part 4A permissions.
- The rest of Forte's PARA material, if the clip is partial: setting it up, moving items between categories, how PARA relates to linking. Also any Forte piece on how PARA and a knowledge base or Zettelkasten fit together.
- Matuschak's uncaptured notes, especially "concept-oriented" and "prefer associative ontologies to hierarchical taxonomies". They hold the reasons that the PARA disagreement turns on.
- A head-to-head comparison of a compiled wiki and RAG on the same corpus and questions (carried over).
- An independent evaluation of Contextual Retrieval, plus Anthropic's Appendix II (carried over).
- How the compiled-wiki pattern holds up at scale (carried over).
- A primary source on the Zettelkasten, such as Luhmann (carried over).
- The line from Bush's memex to modern hypertext and wikis (carried over).

## Sources so far
- [[wiki/sources/Source - LLM Wiki]]: Karpathy's gist proposing the compiled-wiki pattern.
- [[wiki/sources/Source - As We May Think]]: Bush's 1945 essay proposing the memex and associative indexing.
- [[wiki/sources/Source - Evergreen notes]]: Matuschak's hub page defining evergreen notes and their five principles.
- [[wiki/sources/Source - Contextual Retrieval]]: Anthropic's post on improving RAG.
- [[wiki/sources/Source - The PARA Method]]: Forte's four-category system for organising by actionability.
- [[wiki/sources/Source - FSMA 2000 Part 1A]]: the statute setting up the FCA and PRA, their objectives and their coordination.
- [[wiki/sources/Source - About the FCA]]: the FCA's own account of its scale, methods, funding and accountability.
