---
type: overview
status: verified
sources: ["[[raw/karpathy-llm-wiki.md]]", "[[raw/bush-as-we-may-think.pdf]]", "[[raw/matuschak-evergreen-notes.md]]", "[[raw/anthropic-contextual-retrieval.md]]", "[[raw/forte-para-method.md]]", "[[raw/uk-parliament-fsma-2000-part-1a.md]]", "[[raw/fca-about-the-fca.md]]", "[[raw/pra-approach-banking-supervision-2023.pdf]]", "[[raw/fca-boe-memorandum-of-understanding-2024.pdf]]", "[[raw/bank-of-england-prudential-regulation.md]]", "[[raw/edmonds-financial-conduct-authority-2016.pdf]]", "[[raw/wikipedia-financial-conduct-authority.md]]"]
created: "2026-09-22"
updated: "2026-10-06"
tags: ["compiled-wiki", "knowledge-management", "memex", "note-taking", "information-retrieval", "uk-financial-regulation"]
---
# Overview

The current picture across every source, on one page. Rewritten at each ingest, not appended to.

The wiki has two strands that don't yet touch:
- **UK financial regulation:** seven sources. Five primary (the statute, the FCA's and the PRA's own pages, the PRA's banking supervision approach, the FCA–Bank MoU), one secondary (a 2016 Commons Library briefing), one commentary (Wikipedia).
- **Knowledge management:** five sources on how to build and organise a knowledge base.

Regulation agreements and disagreements sit in Strand 1. The sections from "Where sources agree" on apply to the knowledge-management strand.

## Strand 1: UK financial regulation

### The two regulators
- **Statute.** [[wiki/sources/Source - FSMA 2000 Part 1A]] sets up the [[wiki/entities/Financial Conduct Authority]] and the [[wiki/entities/Prudential Regulation Authority]], which is the [[wiki/entities/Bank of England]] acting through its [[wiki/entities/Prudential Regulation Committee]] ([[raw/uk-parliament-fsma-2000-part-1a.md]], ss. 1A, 2A).
- **Who regulates whom.** The FCA supervises every authorised person; the PRA supervises those with at least one PRA-regulated activity ([[raw/uk-parliament-fsma-2000-part-1a.md]], ss. 1L, 2B(5), 2K). The regulators call these "dual-regulated" and "solo-regulated" firms; the PRA's firms are deposit-takers (banks, building societies, credit unions), insurers and designated investment firms ([[raw/fca-boe-memorandum-of-understanding-2024.pdf#page=4]], [[raw/fca-boe-memorandum-of-understanding-2024.pdf#page=6]]). See [[wiki/concepts/Solo and dual regulation]].
- **How many firms.** The FCA regulates the conduct of ~35,500 firms and prudentially supervises ~34,000 ([[raw/fca-about-the-fca.md]]). The PRA regulates ~1,292 by its own count as of 2026-09-21 ([[raw/bank-of-england-prudential-regulation.md]]).
- **Different jobs.** The FCA works for well-functioning markets through consumer protection, integrity and competition; the PRA for the safety and soundness of firms, explicitly not zero failures; both carry a secondary competitiveness and growth objective since 2023 ([[raw/uk-parliament-fsma-2000-part-1a.md]], ss. 1B, 2B, 2G, 1EB, 2H). The regulators' own documents state the same objectives ([[raw/fca-about-the-fca.md]], [[raw/pra-approach-banking-supervision-2023.pdf#page=8]], [[raw/fca-boe-memorandum-of-understanding-2024.pdf#page=2]]). See [[wiki/concepts/Regulatory objectives]].

### For a dual-regulated bank (emphasis this set)
- **Who leads.** The PRA leads for dual-regulated firms and the FCA for solo-regulated ones; supervision isn't joint, and each assesses risk against its own objectives ([[raw/fca-boe-memorandum-of-understanding-2024.pdf#page=6]]). The PRA leads permissions (with FCA consent, a veto), PRA-designated senior managers, change in control and banking transfer schemes; the FCA alone approves customer-facing senior managers and keeps the single register ([[raw/fca-boe-memorandum-of-understanding-2024.pdf#page=6]], [[raw/fca-boe-memorandum-of-understanding-2024.pdf#page=21]], [[raw/fca-boe-memorandum-of-understanding-2024.pdf#page=22]], [[raw/fca-boe-memorandum-of-understanding-2024.pdf#page=24]]). Full table in [[wiki/concepts/FCA-PRA coordination]].
- **Authorising a new bank.** One application to the PRA, assessed jointly. The bank is authorised only if both regulators are satisfied on their [[wiki/concepts/Threshold Conditions]], including whether it could be resolved in an orderly way; the PRA decides ([[raw/pra-approach-banking-supervision-2023.pdf#page=42]]). See [[wiki/concepts/New bank authorisation]] and [[wiki/concepts/Senior Managers and Certification Regime]].
- **How close to failure.** The PRA puts every bank in one of four [[wiki/concepts/Potential impact categories]] and one of five [[wiki/concepts/Proactive Intervention Framework]] stages, from low risk to viability (1) to resolution (5), with escalating actions such as distribution limits and balance-sheet caps at stage 3. The PIF stage isn't disclosed to the firm, but it is shared with the FCA ([[raw/pra-approach-banking-supervision-2023.pdf#page=20]], [[raw/pra-approach-banking-supervision-2023.pdf#page=45]], [[raw/pra-approach-banking-supervision-2023.pdf#page=46]], [[raw/pra-approach-banking-supervision-2023.pdf#page=47]], [[raw/fca-boe-memorandum-of-understanding-2024.pdf#page=7]]).
- **Ring-fencing.** Core services, "retail deposits and related payment and overdraft services", sit in ring-fenced bodies protected from the rest of the group; RFBs face extra requirements and group restructuring powers ([[raw/pra-approach-banking-supervision-2023.pdf#page=8]], [[raw/pra-approach-banking-supervision-2023.pdf#page=54]]). See [[wiki/concepts/Ring-fencing]].
- **Capital and failure.** Pillar 1 plus 2A is the minimum, with buffers on top and a 3.25% leverage ratio ([[raw/pra-approach-banking-supervision-2023.pdf#page=31]], [[raw/pra-approach-banking-supervision-2023.pdf#page=33]]); small banks fail through insolvency with FSCS payout targeted within seven days ([[raw/pra-approach-banking-supervision-2023.pdf#page=38]]). See [[wiki/concepts/Regulatory capital framework]], [[wiki/concepts/Resolvability]], [[wiki/entities/Financial Services Compensation Scheme]].

### Products and payments
- The FCA's reach is set by [[wiki/concepts/Regulated financial services]], which names payment services and e-money ([[raw/uk-parliament-fsma-2000-part-1a.md]], s. 1H(2)). Its [[wiki/concepts/Consumer protection objective]] weighs product risk and consumer capability against firms' duty of care ([[raw/uk-parliament-fsma-2000-part-1a.md]], s. 1C(2)).
- Commentary adds payments history: consumer credit from the OFT in 2014, the [[wiki/entities/Payment Systems Regulator]] from 2015, and [[wiki/concepts/Strong customer authentication]] from 2019 ([[raw/wikipedia-financial-conduct-authority.md]] · commentary).

### Coordination and accountability
- [[wiki/concepts/FCA-PRA coordination]]: a statutory duty to consult, the MoU, a one-way PRA veto decided by the PRC, and consolidated-supervision directions ([[raw/uk-parliament-fsma-2000-part-1a.md]], ss. 3D–3M; [[raw/fca-boe-memorandum-of-understanding-2024.pdf#page=17]]). The [[wiki/entities/Financial Policy Committee]] can direct the PRA on macroprudential tools ([[raw/pra-approach-banking-supervision-2023.pdf#page=15]]).
- [[wiki/entities/HM Treasury]] holds the political levers ([[raw/uk-parliament-fsma-2000-part-1a.md]], ss. 1JA, 1S, 3RC, 3RE).
- **Outside views.** The Commons Library (2016) said the FCA is criticised most on investigating and punishing breaches, when it can't sort out "scandals" ([[raw/edmonds-financial-conduct-authority-2016.pdf#page=2]] · secondary); Wikipedia records later criticism, including a 2024 APPG report ([[raw/wikipedia-financial-conduct-authority.md]] · commentary).

### Where the regulation sources agree
- **Objectives.** The statute, the FCA's page, the PRA's approach and the MoU state the same objectives ([[raw/uk-parliament-fsma-2000-part-1a.md]], s. 1B; [[raw/fca-about-the-fca.md]]; [[raw/pra-approach-banking-supervision-2023.pdf#page=8]]; [[raw/fca-boe-memorandum-of-understanding-2024.pdf#page=2]]).
- **Not zero-failure.** The Act and the PRA agree the PRA need not prevent every failure ([[raw/uk-parliament-fsma-2000-part-1a.md]], s. 2G; [[raw/pra-approach-banking-supervision-2023.pdf#page=11]]).
- **Funding.** Both regulators are funded by fees on firms ([[raw/fca-about-the-fca.md]], [[raw/fca-boe-memorandum-of-understanding-2024.pdf#page=17]]).

### Where the regulation sources disagree
None open. Resolved 2026-10-06, [[system/ingest/set-2026-10-06-2]]:
- **PRA firm count (conflict 1):** ~1,292 per the PRA, updated 2026-09-21 ([[raw/bank-of-england-prudential-regulation.md]]), stated; ~1,500 per the FCA, updated 2026-07-09 ([[raw/fca-about-the-fca.md]]), superseded, newer.
- **FCA conduct count (conflict 2):** ~35,500 per the FCA ([[raw/fca-about-the-fca.md]]) stated; ~58,000 on Wikipedia, sourced to 2010 ([[raw/wikipedia-financial-conduct-authority.md]] · commentary), outweighed, higher level.
- **FSA renamed or abolished (conflict 3):** "renamed" per FSMA s. 1A(1) ([[raw/uk-parliament-fsma-2000-part-1a.md]]) stated; "abolished" per Wikipedia ([[raw/wikipedia-financial-conduct-authority.md]] · commentary), outweighed, higher level.
- **Resolved earlier, by scope:** the FCA "established on 1 April 2013" vs "renamed" (set-2026-10-06). The Commons Library's "established three new regulatory bodies" fits the same reading ([[raw/edmonds-financial-conduct-authority-2016.pdf#page=2]] · secondary).

### Open points
- Which activities are PRA-regulated: the MoU names deposit-taking, insurance and certain large-scale investment business ([[raw/fca-boe-memorandum-of-understanding-2024.pdf#page=15]]), but s. 22A isn't in any source, and the FCA-only status of payment and e-money institutions is still general knowledge.
- Which text of the s. 3B(1)(c) principle applies to the FCA. The PRA says the net-zero "have regard" applies to it ([[raw/pra-approach-banking-supervision-2023.pdf#page=13]]).
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
- The FCA's own approach to supervision, and its prudential supervision page: what "prudentially supervise" and "subject to the prudential standards" each cover.
- The Financial Services Act 2012 itself: settles renamed vs abolished at primary level beyond Part 1A.
- The PRA's approach to insurance supervision (the companion document), if insurers matter.
- The FCA's SCA page and the Payment Services Regulations 2017, to put payments claims on primary sources; the PSR's own about page.
- FCA conduct rules for lending, cards and payments: the Consumer Duty and the consumer credit sourcebook.
- The New Bank Start-up Unit's guidance: what a new bank's application must contain.
- The PRA's ring-fencing rules and the Banking Reform Act 2013: which firms must ring-fence and the threshold.
- The rest of FSMA: Schedules 1ZA and 1ZB, and Part 4A permissions.
- The rest of Forte's PARA material, if the clip is partial.
- Matuschak's uncaptured notes, especially "concept-oriented" and "prefer associative ontologies to hierarchical taxonomies".
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
- [[wiki/sources/Source - The PRA's approach to banking supervision]]: the PRA's 2023 statement of how it supervises banks.
- [[wiki/sources/Source - FCA and Bank of England MoU 2024]]: who leads on what between the FCA and the PRA.
- [[wiki/sources/Source - Bank of England prudential regulation page]]: the PRA's own landing page and firm count.
- [[wiki/sources/Source - Commons Library briefing on the FCA 2016]]: a 2016 parliamentary briefing on the FCA and its critics (secondary).
- [[wiki/sources/Source - Wikipedia on the FCA]]: history, powers, leaders and criticism of the FCA (commentary).
