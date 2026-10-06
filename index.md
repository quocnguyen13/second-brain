# Index

Catalog of every wiki page, one line each. Claude maintains it; format in `system/conventions.md`.

## Overview

- [[wiki/overview.md]] — two strands. UK financial regulation: statute, both regulators' own pages, the PRA's banking approach, the FCA–Bank MoU, a Commons briefing and Wikipedia; who leads for a dual-regulated bank, PIF, ring-fencing, new-bank authorisation; three conflicts resolved 2026-10-06. Knowledge management: compiled wiki, memex, evergreen notes, retrieval, PARA (12 sources)

## Sources

- [[wiki/sources/Source - LLM Wiki]] — Karpathy's gist proposing the compiled-wiki pattern: three layers, three operations, index/log; records the Contextual Retrieval disagreement and an open point with PARA (3 sources)
- [[wiki/sources/Source - As We May Think]] — Bush's 1945 essay proposing the memex and associative indexing as a fix for one-path indexing; records the PARA disagreement (3 sources)
- [[wiki/sources/Source - Evergreen notes]] — Matuschak's hub page defining evergreen notes and five principles; linked notes not captured; records the PARA disagreement (4 sources)
- [[wiki/sources/Source - Contextual Retrieval]] — Anthropic's post: long prompt under 200k tokens, else RAG improved by contextualised chunks, BM25 and reranking (2 sources)
- [[wiki/sources/Source - The PARA Method]] — Forte's four-category system (Projects, Areas, Resources, Archives) organised by actionability; set against Matuschak, Bush and the compiled wiki (4 sources)
- [[wiki/sources/Source - FSMA 2000 Part 1A]] — UK statute setting up the FCA and PRA: solo vs dual regulation, objectives, product-owner lens, FCA–PRA coordination; "renamed" stated over Wikipedia's "abolished" (3 sources)
- [[wiki/sources/Source - About the FCA]] — the FCA's own page: firm numbers by what they count, authorise–supervise–enforce, fees-funded, accountable to Treasury and Parliament; its ~35,500 stated, its ~1,500 PRA figure superseded (4 sources)
- [[wiki/sources/Source - The PRA's approach to banking supervision]] — the PRA's July 2023 approach: three principles, impact categories, PIF, ring-fencing, capital, resolvability, new-bank authorisation (1 source)
- [[wiki/sources/Source - FCA and Bank of England MoU 2024]] — FCA–PRA MoU of March 2024: lead regulator, consent and consultation per process, information sharing, s. 3I veto via the PRC (2 sources)
- [[wiki/sources/Source - Bank of England prudential regulation page]] — the PRA's landing page: ~1,292 firms, Rulebook, purpose of supervision; its figure stated after conflict 1 (2 sources)
- [[wiki/sources/Source - Commons Library briefing on the FCA 2016]] — secondary: 2016 briefing on the FCA's origins, four areas of work and enforcement criticism (IRHP, Connaught) (2 sources)
- [[wiki/sources/Source - Wikipedia on the FCA]] — commentary: FCA history, payments (PSR, SCA), product powers, leaders, criticism; its two conflicting claims outweighed (3 sources)

## Entities

- [[wiki/entities/Karpathy]] — author of the LLM Wiki gist (1 source)
- [[wiki/entities/Vannevar Bush]] — author of "As We May Think," proposed the memex (2 sources)
- [[wiki/entities/Andy Matuschak]] — author of the "Evergreen notes" page (1 source)
- [[wiki/entities/Anthropic]] — publisher of the Contextual Retrieval post; maker of Claude and prompt caching (1 source)
- [[wiki/entities/Tiago Forte]] — author of the PARA method post; former productivity coach (1 source)
- [[wiki/entities/Financial Conduct Authority]] — UK regulator of all authorised persons; conduct regulator for dual-regulated firms; responsibilities per the MoU; product powers and history; ~35,500 conduct firms and "renamed" stated, Wikipedia's claims outweighed (6 sources)
- [[wiki/entities/Prudential Regulation Authority]] — the Bank of England acting as prudential regulator; lead regulator for dual-regulated firms; supervisory approach; ~1,292 firms by its own count, the FCA's ~1,500 superseded (5 sources)
- [[wiki/entities/HM Treasury]] — holds the levers over both regulators: recommendations, reviews, boundary orders, rule directions, designated activities; receives regulatory-failure reports (5 sources)
- [[wiki/entities/Bank of England]] — is the PRA through its Prudential Regulation Committee; monetary policy, financial stability, resolution authority, liquidity facilities (4 sources)
- [[wiki/entities/Financial Policy Committee]] — the Bank's macroprudential committee; recommendations and directions to the PRA (2 sources)
- [[wiki/entities/Prudential Regulation Committee]] — the Bank committee that is the PRA's decision-maker; decides the s. 3I veto (3 sources)
- [[wiki/entities/Financial Services Compensation Scheme]] — compensation fund of last resort; seven-day depositor payout target; rules split PRA/FCA (3 sources)
- [[wiki/entities/Payment Systems Regulator]] — payment-systems regulator set up by the FCA in 2015; mostly commentary (2 sources)

## Concepts

- [[wiki/concepts/Compiled wiki]] — an LLM-maintained, three-layer wiki that compounds knowledge instead of re-deriving it; contested on its RAG premise; topic-organised, open point with PARA (3 sources)
- [[wiki/concepts/Wiki ingest]] — the operation that files one new source into the wiki (1 source)
- [[wiki/concepts/Wiki query]] — the operation that answers a question from the wiki and can file the answer back (1 source)
- [[wiki/concepts/Wiki lint]] — the operation that health-checks the wiki for contradictions, staleness, and gaps (1 source)
- [[wiki/concepts/Wiki index and log]] — the content catalog and the chronological record that keep the wiki navigable; small-scale alternatives to RAG (2 sources)
- [[wiki/concepts/Memex]] — Bush's proposed personal device for storing and associatively linking a lifetime's records (2 sources)
- [[wiki/concepts/Associative indexing]] — finding records by association instead of fixed classification; contested by PARA's one-home-per-item filing (3 sources)
- [[wiki/concepts/Evergreen notes]] — notes written to accumulate across projects: atomic, concept-oriented, densely linked; contested by PARA's project-first hierarchy (4 sources)
- [[wiki/concepts/Retrieval-augmented generation]] — retrieving chunks at query time and adding them to the prompt; contested on whether it accumulates anything (2 sources)
- [[wiki/concepts/Contextual Retrieval]] — LLM-written per-chunk context prepended before embedding and BM25 indexing (1 source)
- [[wiki/concepts/BM25]] — lexical ranking function for exact-term matches, paired with embeddings in hybrid search (2 sources)
- [[wiki/concepts/Reranking]] — scoring retrieved chunks and keeping only the top ones; accuracy vs latency trade-off (2 sources)
- [[wiki/concepts/Prompt caching]] — caching prompt content between API calls; makes long prompts and Contextual Retrieval cheaper (1 source)
- [[wiki/concepts/PARA method]] — Projects, Areas, Resources, Archives; projects end, areas don't; contested on hierarchy vs association (3 sources)
- [[wiki/concepts/Organizing by actionability]] — organise by current projects and goals, not subjects; contested against concept-oriented, associative notes (4 sources)
- [[wiki/concepts/Solo and dual regulation]] — FCA supervises every authorised person; any PRA-regulated activity adds the PRA; MoU definitions and firm types; ~1,292 PRA firms; unverified (FCA-only payment/e-money firms still general knowledge) (5 sources)
- [[wiki/concepts/Regulatory objectives]] — FCA and PRA objectives compared; both regulators' own documents and the MoU agree with the Act (5 sources)
- [[wiki/concepts/Consumer protection objective]] — FCA's "appropriate degree of protection", weighing risk, capability, consumer responsibility and firms' duty of care (1 source)
- [[wiki/concepts/Regulated financial services]] — the s. 1H(2) list setting the FCA's reach, naming payment services and e-money (1 source)
- [[wiki/concepts/Regulatory principles]] — s. 3B principles binding both regulators; two texts of (c) unresolved; PRA applies the net-zero "have regard" (3 sources)
- [[wiki/concepts/FCA-PRA coordination]] — duty to coordinate, one-way PRA veto, Treasury boundary; who-leads-on-what table from the 2024 MoU (3 sources)
- [[wiki/concepts/New bank authorisation]] — one PRA-led application, joint assessment, FCA consent, Threshold Conditions and resolvability (2 sources)
- [[wiki/concepts/Proactive Intervention Framework]] — the PRA's five stages of proximity to failure and the actions at each (2 sources)
- [[wiki/concepts/Potential impact categories]] — the PRA's four categories of a firm's potential impact on stability (1 source)
- [[wiki/concepts/Threshold Conditions]] — minimum conditions for permission, assessed by each regulator (2 sources)
- [[wiki/concepts/Ring-fencing]] — protecting core services (deposits, payments, overdrafts) in ring-fenced bodies (3 sources)
- [[wiki/concepts/Resolvability]] — orderly failure: strategies, SCV and FSCS payout, Resolvability Assessment Framework (2 sources)
- [[wiki/concepts/Senior Managers and Certification Regime]] — SMF approval by both regulators; who leads which SMFs (2 sources)
- [[wiki/concepts/Regulatory capital framework]] — Pillar 1, Pillar 2A, combined and PRA buffers, 3.25% leverage ratio (1 source)
- [[wiki/concepts/Strong customer authentication]] — PSD2 two-factor rule for online payments from 2019; commentary only (1 source)

## Analyses

- [[wiki/analyses/Compare the PARA method and evergreen notes as ways to organise what I read]] — PARA files items by project for action; evergreen notes link concepts for thinking and suit reading better; contested on hierarchy vs association (3 sources)
