---
type: overview
status: verified
sources: ["[[raw/karpathy-llm-wiki.md]]", "[[raw/bush-as-we-may-think.pdf]]", "[[raw/matuschak-evergreen-notes.md]]", "[[raw/anthropic-contextual-retrieval.md]]", "[[raw/forte-para-method.md]]", "[[raw/uk-parliament-fsma-2000-part-1a.md]]", "[[raw/fca-about-the-fca.md]]", "[[raw/pra-approach-banking-supervision-2023.pdf]]", "[[raw/fca-boe-memorandum-of-understanding-2024.pdf]]", "[[raw/bank-of-england-prudential-regulation.md]]", "[[raw/edmonds-financial-conduct-authority-2016.pdf]]", "[[raw/wikipedia-financial-conduct-authority.md]]", "[[raw/fca-disp-1-6-complaints-time-limits.md]]", "[[raw/fca-disp-2-7-complainant-eligibility.md]]", "[[raw/fca-disp-2-8-referral-time-limits.md]]", "[[raw/fca-disp-3-7-ombudsman-awards.md]]", "[[raw/fca-glossary-small-business.md]]", "[[raw/fca-glossary-micro-enterprise.md]]", "[[raw/financial-ombudsman-how-to-complain.md]]", "[[raw/fca-final-notice-tsb-2022.pdf]]", "[[raw/uk-parliament-fsma-2000-2026-09.pdf]]"]
created: "2026-09-22"
updated: "2026-10-20"
tags: ["compiled-wiki", "knowledge-management", "memex", "note-taking", "information-retrieval", "uk-financial-regulation", "complaints"]
---
# Overview

The current picture across every source, on one page. Rewritten at each ingest, not appended to.

The wiki has two strands that don't yet touch:
- **UK financial regulation:** seventeen sources.
  - Fourteen primary: the statute's Part 1A; the whole Act (2026-09), mapped, with Part II compiled; the FCA's and the PRA's own pages; the PRA's banking supervision approach; the FCA–Bank MoU; four DISP sections and two Glossary terms from the FCA Handbook; the Financial Ombudsman Service's own guide; and the FCA's Final Notice to TSB (2022).
  - One secondary: a 2016 Commons Library briefing.
  - One commentary: Wikipedia.
  - One AI: a Claude study note on who regulates what (2026-09-27). Its unbacked claims stay marked `· AI` and are kept off this page.

  The 2026-10-14 sets added complaints and the FOS, the Claude note, and the TSB Final Notice, the wiki's first enforcement case. On 2026-10-17 the whole of FSMA 2000 entered `raw/`. [[wiki/sources/Source - FSMA 2000 (2026-09)]] maps its Parts and Schedules; eight parts are planned, one per run, starting with Part II (the perimeter), Part 4A (permission) and Part XVI (the ombudsman scheme). Part II was compiled the same day: [[wiki/sources/Source - FSMA 2000 (2026-09) - Part II]]. Part 4A followed on 2026-10-20: [[wiki/sources/Source - FSMA 2000 (2026-09) - Part 4A]], with the new [[wiki/concepts/Part 4A permission]].
- **Knowledge management:** five sources on how to build and organise a knowledge base.

Regulation agreements and disagreements sit in Strand 1. The sections from "Where sources agree" on apply to the knowledge-management strand.

## Strand 1: UK financial regulation

### The perimeter (FSMA Part II, emphasis 2026-10-17)
- **What needs authorisation.** The [[wiki/concepts/General prohibition]]: no one may carry on a regulated activity in the UK unless authorised or exempt. A regulated activity is one of a kind [[wiki/entities/HM Treasury]] specifies by order ([[raw/uk-parliament-fsma-2000-2026-09.pdf#page=51]], s. 19(1); [[raw/uk-parliament-fsma-2000-2026-09.pdf#page=56]], s. 22(1); [[raw/uk-parliament-fsma-2000-2026-09.pdf#page=57]], s. 22(5)). Breaching it is a crime, and the customer can walk away from the deal ([[raw/uk-parliament-fsma-2000-2026-09.pdf#page=60]], s. 23(1); [[raw/uk-parliament-fsma-2000-2026-09.pdf#page=63]], s. 26(1)–(2)).
- **Outside permission.** An authorised firm acting outside its permission breaches a regulator's requirement, but it is not an offence and its contracts stand, except for credit ([[raw/uk-parliament-fsma-2000-2026-09.pdf#page=52]], s. 20(1)–(2)). For credit-related activities it is an offence, and the agreements can't be enforced against borrowers unless the FCA allows it ([[raw/uk-parliament-fsma-2000-2026-09.pdf#page=60]], s. 23(1A); [[raw/uk-parliament-fsma-2000-2026-09.pdf#page=63]], s. 26A(1); [[raw/uk-parliament-fsma-2000-2026-09.pdf#page=67]], s. 28A(3)).
- **Promotions.** [[wiki/concepts/Financial promotion]]: only an authorised person may communicate an invitation or inducement to engage in investment activity, or approve one, and approving others' promotions needs FCA permission under s. 55NA (from 2024). Breach is an offence, and resulting agreements are unenforceable against the customer ([[raw/uk-parliament-fsma-2000-2026-09.pdf#page=53]], s. 21(1); [[raw/uk-parliament-fsma-2000-2026-09.pdf#page=54]], s. 21(2)–(2A); [[raw/uk-parliament-fsma-2000-2026-09.pdf#page=55]], F136; [[raw/uk-parliament-fsma-2000-2026-09.pdf#page=62]], s. 25(1); [[raw/uk-parliament-fsma-2000-2026-09.pdf#page=69]], s. 30(2)).

### The two regulators
- **Statute.** [[wiki/sources/Source - FSMA 2000 Part 1A]] sets up the [[wiki/entities/Financial Conduct Authority]] and the [[wiki/entities/Prudential Regulation Authority]], which is the [[wiki/entities/Bank of England]] acting through its [[wiki/entities/Prudential Regulation Committee]] ([[raw/uk-parliament-fsma-2000-part-1a.md]], ss. 1A, 2A).
- **Who regulates whom.** The FCA supervises every authorised person; the PRA supervises those with at least one PRA-regulated activity ([[raw/uk-parliament-fsma-2000-part-1a.md]], ss. 1L, 2B(5), 2K). The regulators call these "dual-regulated" and "solo-regulated" firms; the PRA's firms are deposit-takers (banks, building societies, credit unions), insurers and designated investment firms ([[raw/fca-boe-memorandum-of-understanding-2024.pdf#page=4]], [[raw/fca-boe-memorandum-of-understanding-2024.pdf#page=6]]). See [[wiki/concepts/Solo and dual regulation]].
- **How many firms.** The FCA regulates the conduct of ~35,500 firms and prudentially supervises ~34,000 ([[raw/fca-about-the-fca.md]]). The PRA regulates ~1,292 by its own count as of 2026-09-21 ([[raw/bank-of-england-prudential-regulation.md]]).
- **Different jobs.** The FCA works for well-functioning markets through consumer protection, integrity and competition; the PRA for the safety and soundness of firms, explicitly not zero failures; both carry a secondary competitiveness and growth objective since 2023 ([[raw/uk-parliament-fsma-2000-part-1a.md]], ss. 1B, 2B, 2G, 1EB, 2H). The regulators' own documents state the same objectives ([[raw/fca-about-the-fca.md]], [[raw/pra-approach-banking-supervision-2023.pdf#page=8]], [[raw/fca-boe-memorandum-of-understanding-2024.pdf#page=2]]). See [[wiki/concepts/Regulatory objectives]].

### For a dual-regulated bank (emphasis this set)
- **Who leads.** The PRA leads for dual-regulated firms and the FCA for solo-regulated ones; supervision isn't joint, and each assesses risk against its own objectives ([[raw/fca-boe-memorandum-of-understanding-2024.pdf#page=6]]). The PRA leads permissions (with FCA consent, a veto), PRA-designated senior managers, change in control and banking transfer schemes; the FCA alone approves customer-facing senior managers and keeps the single register ([[raw/fca-boe-memorandum-of-understanding-2024.pdf#page=6]], [[raw/fca-boe-memorandum-of-understanding-2024.pdf#page=21]], [[raw/fca-boe-memorandum-of-understanding-2024.pdf#page=22]], [[raw/fca-boe-memorandum-of-understanding-2024.pdf#page=24]]). Full table in [[wiki/concepts/FCA-PRA coordination]].
- **Authorising a new bank.** One application to the PRA, assessed jointly. The bank is authorised only if both regulators are satisfied on their [[wiki/concepts/Threshold Conditions]], including whether it could be resolved in an orderly way; the PRA decides ([[raw/pra-approach-banking-supervision-2023.pdf#page=42]]). In the Act, the PRA may give the permission only with the FCA's consent, and must decide within 6 months of a complete application (12 at most for an incomplete one), the FCA's consent included ([[raw/uk-parliament-fsma-2000-2026-09.pdf#page=86]], s. 55F(2); [[raw/uk-parliament-fsma-2000-2026-09.pdf#page=110]], s. 55V(1)–(3)). See [[wiki/concepts/New bank authorisation]] and [[wiki/concepts/Senior Managers and Certification Regime]].
- **A new product outside the permission (FSMA Part 4A, emphasis 2026-10-20).** A firm can hold one [[wiki/concepts/Part 4A permission]], a list of described activities; to carry on another regulated activity it applies to vary it. A bank applies to the PRA, which needs the FCA's consent; the same 6-month maximum applies ([[raw/uk-parliament-fsma-2000-2026-09.pdf#page=83]], s. 55A(3); [[raw/uk-parliament-fsma-2000-2026-09.pdf#page=89]], s. 55I(1); [[raw/uk-parliament-fsma-2000-2026-09.pdf#page=110]], s. 55V(1)). Either regulator can also vary the permission or impose requirements on its own initiative, with a right to refer to the Tribunal ([[raw/uk-parliament-fsma-2000-2026-09.pdf#page=90]], s. 55J(1); [[raw/uk-parliament-fsma-2000-2026-09.pdf#page=118]], s. 55Z3(2)).
- **How close to failure.** The PRA puts every bank in one of four [[wiki/concepts/Potential impact categories]] and one of five [[wiki/concepts/Proactive Intervention Framework]] stages, from low risk to viability (1) to resolution (5), with escalating actions such as distribution limits and balance-sheet caps at stage 3. The PIF stage isn't disclosed to the firm, but it is shared with the FCA ([[raw/pra-approach-banking-supervision-2023.pdf#page=20]], [[raw/pra-approach-banking-supervision-2023.pdf#page=45]], [[raw/pra-approach-banking-supervision-2023.pdf#page=46]], [[raw/pra-approach-banking-supervision-2023.pdf#page=47]], [[raw/fca-boe-memorandum-of-understanding-2024.pdf#page=7]]).
- **Ring-fencing.** Core services, "retail deposits and related payment and overdraft services", sit in ring-fenced bodies protected from the rest of the group; RFBs face extra requirements and group restructuring powers ([[raw/pra-approach-banking-supervision-2023.pdf#page=8]], [[raw/pra-approach-banking-supervision-2023.pdf#page=54]]). See [[wiki/concepts/Ring-fencing]].
- **Operational resilience is prudential.** The PRA expects banks to manage operational as well as financial risks. It assumes disruptions will happen, and expects firms to stay within impact tolerances for their important business services; the board is accountable ([[raw/pra-approach-banking-supervision-2023.pdf#page=36]]). See [[wiki/concepts/Operational resilience]]. The FCA's side of the worked case, [[wiki/entities/TSB Bank]], is now primary-sourced (next section); the PRA's side waits for the Bank's release.
- **Capital and failure.** Pillar 1 plus 2A is the minimum, with buffers on top and a 3.25% leverage ratio ([[raw/pra-approach-banking-supervision-2023.pdf#page=31]], [[raw/pra-approach-banking-supervision-2023.pdf#page=33]]); small banks fail through insolvency with FSCS payout targeted within seven days ([[raw/pra-approach-banking-supervision-2023.pdf#page=38]]). See [[wiki/concepts/Regulatory capital framework]], [[wiki/concepts/Resolvability]], [[wiki/entities/Financial Services Compensation Scheme]].

### A failed migration: TSB, 2018 (emphasis 2026-10-14-3)
- **What happened.** TSB moved its customer services from the Lloyds Banking Group platform to Proteo4UK, built and run by Sabadell's IT subsidiary SABIS, with go-live on 22 April 2018. The data migrated, but digital, telephone and branch banking failed; business as usual returned only on 10 December 2018, after 225,492 complaints and £32.7m in redress ([[raw/fca-final-notice-tsb-2022.pdf#page=2]], [[raw/fca-final-notice-tsb-2022.pdf#page=3]], paras 2.4–2.8; [[raw/fca-final-notice-tsb-2022.pdf#page=14]], para 4.4). See [[wiki/sources/Source - FCA Final Notice to TSB Bank 2022]].
- **The finding.** The FCA fined TSB £29.75m for breaching [[wiki/concepts/Principles for Businesses]] 2 and 3 ([[raw/fca-final-notice-tsb-2022.pdf#page=1]], para 1.1; [[raw/fca-final-notice-tsb-2022.pdf#page=10]], para 2.33). The amount came from the five DEPP steps, ending with a 30% settlement discount; see [[wiki/entities/Financial Conduct Authority]] ([[raw/fca-final-notice-tsb-2022.pdf#page=101]], paras 6.24–6.25).
- **Go-live attestations.** After a February 2018 change, business functions signed off non-functional requirements relying on the IT function's confirmation of testing; the board wasn't explicitly told of the change, and the test report's two-page summary reached the business functions at 17.19 on 17 April, the day before the board's go-ahead meeting ([[raw/fca-final-notice-tsb-2022.pdf#page=66]], [[raw/fca-final-notice-tsb-2022.pdf#page=67]], paras 4.201–4.205).
- **Testing scope.** Performance testing was cut to one data centre in an informal decision outside governance; testing in the live two-centre set-up would likely have found the fault that took digital banking down ([[raw/fca-final-notice-tsb-2022.pdf#page=5]], para 2.14; [[raw/fca-final-notice-tsb-2022.pdf#page=65]], para 4.195).
- **Outsourcer readiness.** TSB never formally assessed SABIS's capability and accepted readiness letters that were statements of expectation, not fact ([[raw/fca-final-notice-tsb-2022.pdf#page=93]], para 5.3; [[raw/fca-final-notice-tsb-2022.pdf#page=79]], para 4.258). The rules it fell short of are on [[wiki/concepts/Outsourcing of critical or important functions]].
- **Two regulators.** The FCA set its penalty taking account of a PRA penalty proposed for the same events ([[raw/fca-final-notice-tsb-2022.pdf#page=100]], para 6.18). The PRA's amount and framing aren't in `raw/` yet.

### Products and payments
- The FCA's reach is set by [[wiki/concepts/Regulated financial services]], which names payment services and e-money ([[raw/uk-parliament-fsma-2000-part-1a.md]], s. 1H(2)). Its [[wiki/concepts/Consumer protection objective]] weighs product risk and consumer capability against firms' duty of care ([[raw/uk-parliament-fsma-2000-part-1a.md]], s. 1C(2)).
- Commentary adds payments history: consumer credit from the OFT in 2014, the [[wiki/entities/Payment Systems Regulator]] from 2015, and [[wiki/concepts/Strong customer authentication]] from 2019 ([[raw/wikipedia-financial-conduct-authority.md]] · commentary).

### Complaints and the Financial Ombudsman Service (emphasis 2026-10-14)
- **The bank's deadlines.** On receipt, the bank sends a prompt acknowledgement and keeps the complainant informed. It must send a final response, or a written delay response, within eight weeks ([[raw/fca-disp-1-6-complaints-time-limits.md]], DISP 1.6.1R, 1.6.2R). EMD and PSD complaints must be answered within 15 business days, or within 35 with a holding response in exceptional circumstances ([[raw/fca-disp-1-6-complaints-time-limits.md]], DISP 1.6.2AR). See [[wiki/concepts/Complaint handling time limits]].
- **What a final response contains.** It accepts the complaint, offers redress or rejects it with reasons. It encloses the FOS leaflet, gives the FOS website, says the complainant may now go to the FOS, and says whether the bank waives the time limits, all prominently ([[raw/fca-disp-1-6-complaints-time-limits.md]], DISP 1.6.2R(1)). It must also mention the six-month limit ([[raw/fca-disp-2-8-referral-time-limits.md]]). See [[wiki/concepts/Final response]].
- **When the FOS can act.** After the final response or a missed deadline. A complaint is out of time six months after the final response, or six years after the event or three years after awareness, unless there are exceptional circumstances or the firm consents, which it cannot withdraw ([[raw/fca-disp-2-8-referral-time-limits.md]], DISP 2.8.1R, 2.8.2R). See [[wiki/concepts/Ombudsman referral time limits]].
- **Business customers.** These are eligible as a micro-enterprise (fewer than 10 staff, and turnover or balance sheet up to €2 million) or a small business (turnover under £6.5 million, and fewer than 50 staff or a balance sheet under £5 million). Group enterprises count, and a firm in doubt should treat the business as eligible ([[raw/fca-glossary-micro-enterprise.md]]; [[raw/fca-glossary-small-business.md]]; [[raw/fca-disp-2-7-complainant-eligibility.md]]). APP fraud victims are eligible against an involved firm even when the complaint isn't a PSD complaint ([[raw/fca-disp-2-7-complainant-eligibility.md]], DISP 2.7.6R(2B)). See [[wiki/concepts/Eligible complainant]].
- **What it can award.** For complaints referred from 1 April 2026: up to £455,000 for acts on or after 1 April 2019, and £205,000 for earlier acts. The cap is CPI-indexed each April. Interest, costs and directions come on top, and firms must comply promptly ([[raw/fca-disp-3-7-ombudsman-awards.md]]). See [[wiki/concepts/Ombudsman awards]] and [[wiki/entities/Financial Ombudsman Service]].

### Coordination and accountability
- [[wiki/concepts/FCA-PRA coordination]]: a statutory duty to consult, the MoU, a one-way PRA veto decided by the PRC, and consolidated-supervision directions ([[raw/uk-parliament-fsma-2000-part-1a.md]], ss. 3D–3M; [[raw/fca-boe-memorandum-of-understanding-2024.pdf#page=17]]). The [[wiki/entities/Financial Policy Committee]] can direct the PRA on macroprudential tools ([[raw/pra-approach-banking-supervision-2023.pdf#page=15]]).
- [[wiki/entities/HM Treasury]] holds the political levers ([[raw/uk-parliament-fsma-2000-part-1a.md]], ss. 1JA, 1S, 3RC, 3RE).
- The Bank's other committees: the [[wiki/entities/Monetary Policy Committee]] and the FPC carry its monetary-policy and financial-stability work ([[raw/fca-boe-memorandum-of-understanding-2024.pdf#page=1]]).
- **Pending change.** The wiki holds AI-only leads on the [[wiki/entities/Financial Services and Markets Bill 2026–27]], which would reform the PSR, the FOS, authorisation and ring-fencing. No primary source on it is in `raw/` yet.
- **Outside views.** The Commons Library (2016) said the FCA is criticised most on investigating and punishing breaches, when it can't sort out "scandals" ([[raw/edmonds-financial-conduct-authority-2016.pdf#page=2]] · secondary); Wikipedia records later criticism, including a 2024 APPG report ([[raw/wikipedia-financial-conduct-authority.md]] · commentary).

### Where the regulation sources agree
- **Objectives.** The statute, the FCA's page, the PRA's approach and the MoU state the same objectives ([[raw/uk-parliament-fsma-2000-part-1a.md]], s. 1B; [[raw/fca-about-the-fca.md]]; [[raw/pra-approach-banking-supervision-2023.pdf#page=8]]; [[raw/fca-boe-memorandum-of-understanding-2024.pdf#page=2]]).
- **Not zero-failure.** The Act and the PRA agree the PRA need not prevent every failure ([[raw/uk-parliament-fsma-2000-part-1a.md]], s. 2G; [[raw/pra-approach-banking-supervision-2023.pdf#page=11]]).
- **Funding.** Both regulators are funded by fees on firms ([[raw/fca-about-the-fca.md]], [[raw/fca-boe-memorandum-of-understanding-2024.pdf#page=17]]).

### Where the regulation sources disagree
None open.

Resolved 2026-10-20 as scope (c), [[system/ingest/set-2026-10-20]] conflict 1, on [[wiki/concepts/FCA-PRA coordination]]:
- **Consent or consultation on varying and cancelling a permission.** Not a conflict once scoped. The MoU says the PRA obtains the FCA's consent before granting, removing or adding an activity, and consults before cancelling ([[raw/fca-boe-memorandum-of-understanding-2024.pdf#page=21]]). The Act says the same for a firm's application, but on the PRA's own initiative only adding an activity or widening a description needs consent ([[raw/uk-parliament-fsma-2000-2026-09.pdf#page=89]], s. 55I(1)–(2); [[raw/uk-parliament-fsma-2000-2026-09.pdf#page=91]], s. 55J(5)). The MoU paragraph sits under "Applications to grant, vary or cancel a regulatory permission", so it describes the application route ([[raw/fca-boe-memorandum-of-understanding-2024.pdf#page=21]]).

Resolved 2026-10-14, [[system/ingest/set-2026-10-14]], both on [[wiki/concepts/Complaint handling time limits]]:
- **Conflict 1, 15 days or 15 business days.** DISP 1.6.2AR's 15 business days, or 35, is stated ([[raw/fca-disp-1-6-complaints-time-limits.md]]). The FOS guide's "only 15 days" ([[raw/financial-ombudsman-how-to-complain.md]]) is marked outweighed, as DISP is the FCA's own statement.
- **Conflict 2, fraud and scams.** DISP's scope is stated: the short deadline is for EMD and PSD complaints only ([[raw/fca-disp-1-6-complaints-time-limits.md]], DISP 1.6.2AR). DISP also recognises APP fraud complaints that are not PSD complaints ([[raw/fca-disp-2-7-complainant-eligibility.md]], DISP 2.7.6R(2B)). The FOS guide's "fraud and scams" ([[raw/financial-ombudsman-how-to-complain.md]]) is marked outweighed, as DISP is the FCA's own statement.

Resolved 2026-10-06, [[system/ingest/set-2026-10-06-2]]:
- **PRA firm count (conflict 1):** ~1,292 per the PRA, updated 2026-09-21 ([[raw/bank-of-england-prudential-regulation.md]]), stated; ~1,500 per the FCA, updated 2026-07-09 ([[raw/fca-about-the-fca.md]]), superseded, newer.
- **FCA conduct count (conflict 2):** ~35,500 per the FCA ([[raw/fca-about-the-fca.md]]) stated; ~58,000 on Wikipedia, sourced to 2010 ([[raw/wikipedia-financial-conduct-authority.md]] · commentary), outweighed, higher level.
- **FSA renamed or abolished (conflict 3):** "renamed" per FSMA s. 1A(1) ([[raw/uk-parliament-fsma-2000-part-1a.md]]) stated; "abolished" per Wikipedia ([[raw/wikipedia-financial-conduct-authority.md]] · commentary), outweighed, higher level.
- **Resolved earlier, by scope:** the FCA "established on 1 April 2013" vs "renamed" (set-2026-10-06). The Commons Library's "established three new regulatory bodies" fits the same reading ([[raw/edmonds-financial-conduct-authority-2016.pdf#page=2]] · secondary).

### Open points
- Which activities are PRA-regulated: the MoU names deposit-taking, insurance and certain large-scale investment business ([[raw/fca-boe-memorandum-of-understanding-2024.pdf#page=15]]). Section 22A leaves the list to a Treasury order ([[raw/uk-parliament-fsma-2000-2026-09.pdf#page=59]], s. 22A(1)), which isn't in `raw/`. The FCA-only status of payment and e-money institutions now rests only on the Claude note, which is AI level.
- The Claude note's "around 1,500" PRA firms repeats the FCA's superseded figure. It was left out of the wiki.
- Which text of the s. 3B(1)(c) principle applies to the FCA. The PRA says the net-zero "have regard" applies to it ([[raw/pra-approach-banking-supervision-2023.pdf#page=13]]).
- How the FCA's ~34,000 prudentially supervised firms relate to the ~14,000 under its Handbook's prudential standards.
- Which body runs the "ombudsman scheme" in FSMA s. 1C(2). No source in the wiki says it is the FOS.

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
- FSMA s. 228 is in `raw/` inside the whole Act and waits for Part XVI (plan 3). Parts II and 4A are compiled. See [[wiki/sources/Source - FSMA 2000 (2026-09)]].
- What the threshold conditions are: Schedule 6 (plan 5). Schedule 6A, the FCA's additional power to vary or cancel, is not in the plan. S.I. 2025/859, which excludes s. 55B(3) for specified purposes, is not in `raw/`.
- How long permission and variation decisions take in practice: the Act gives only the 6- and 12-month maximums. The regulators' published service standards would answer it.
- The Treasury's orders behind Part II: the Regulated Activities Order (with Schedule 2, plan 8), the Financial Promotion Order (exemptions under s. 21(5)), and the order designating credit-related regulated activities (s. 23(1B)).
- To back the Claude note (all on the capture list): the Bank of England's release on the TSB fines (the PRA's £18.9m and framing); the Bill's page and Parliament's report-stage news item; FCA PRIN and the PRA Fundamental Rules; the SBV's own page on its role.
- Current SYSC 8 (outsourcing) and SYSC 4.1 (business continuity), and the FCA's and PRA's operational resilience rules: the TSB notice quotes SYSC only as in force in 2015–2018.
- DEPP 6.5A and the Enforcement Guide themselves, rather than the notice's account of them.
- No source named in the note: Bank Rate and the 2% inflation target, the BNPL rules, the loan-to-income mortgage cap, and e-money safeguarding. These need `/research`.
- The Glossary definitions of "consumer", "PSD complaint" and "EMD complaint", and DISP 1 Annex 3R (the waiver wording a final response must use).
- DISP 1.3 complaint-handling rules and DISP 3.6 on how the Ombudsman decides.
- FOS guidance on APP fraud complaints: which deadline applies to them in practice.
- The PRA-Regulated Activities Order: the list of activities that makes a firm dual-regulated. Section 22A gives the Treasury the power but names no activities.
- The FCA's own approach to supervision, and its prudential supervision page: what "prudentially supervise" and "subject to the prudential standards" each cover.
- The Financial Services Act 2012 itself: settles renamed vs abolished at primary level beyond Part 1A.
- The PRA's approach to insurance supervision (the companion document), if insurers matter.
- The FCA's SCA page and the Payment Services Regulations 2017, to put payments claims on primary sources; the PSR's own about page.
- FCA conduct rules for lending, cards and payments: the Consumer Duty and the consumer credit sourcebook.
- The New Bank Start-up Unit's guidance: what a new bank's application must contain.
- The PRA's ring-fencing rules and the Banking Reform Act 2013: which firms must ring-fence and the threshold.
- The rest of FSMA is in `raw/` but not compiled: Schedules 1ZA and 1ZB are not in the plan.
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
- [[wiki/sources/Source - FSMA 2000 (2026-09)]]: the whole Act, revised text; a map of its Parts and Schedules, compiled one part per run.
- [[wiki/sources/Source - FSMA 2000 (2026-09) - Part II]]: the perimeter: general prohibition, financial promotion, regulated activities, offences, and unenforceable agreements.
- [[wiki/sources/Source - FSMA 2000 (2026-09) - Part 4A]]: permission: applying, giving, varying and cancelling, requirements, own-initiative powers, the s. 55NA approver permission, decision deadlines and the Tribunal.
- [[wiki/sources/Source - About the FCA]]: the FCA's own account of its scale, methods, funding and accountability.
- [[wiki/sources/Source - The PRA's approach to banking supervision]]: the PRA's 2023 statement of how it supervises banks.
- [[wiki/sources/Source - FCA and Bank of England MoU 2024]]: who leads on what between the FCA and the PRA.
- [[wiki/sources/Source - Bank of England prudential regulation page]]: the PRA's own landing page and firm count.
- [[wiki/sources/Source - Commons Library briefing on the FCA 2016]]: a 2016 parliamentary briefing on the FCA and its critics (secondary).
- [[wiki/sources/Source - Wikipedia on the FCA]]: history, powers, leaders and criticism of the FCA (commentary).
- [[wiki/sources/Source - DISP 1.6 Complaints time limit rules]]: a firm's complaint deadlines and what a final response must contain.
- [[wiki/sources/Source - DISP 2.7 Complainant eligibility]]: who can take a complaint to the FOS.
- [[wiki/sources/Source - DISP 2.8 Referral time limits]]: when the FOS can and can't take a complaint.
- [[wiki/sources/Source - DISP 3.7 Ombudsman awards]]: what the FOS can award, and the cap.
- [[wiki/sources/Source - FCA glossary small business]]: the small-business test.
- [[wiki/sources/Source - FCA glossary micro-enterprise]]: the micro-enterprise test.
- [[wiki/sources/Source - FOS How to complain]]: the FOS's own three-step guide for consumers.
- [[wiki/sources/Source - FCA Final Notice to TSB Bank 2022]]: the FCA's £29.75m penalty on TSB for its 2018 migration.
- [[wiki/sources/Source - Claude on who regulates what (2026-09-27)]]: a Claude study note, at AI level. Its backed claims cite `raw/`; the rest are leads.
