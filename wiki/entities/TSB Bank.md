---
type: entity
status: unverified
sources: ["[[raw/fca-final-notice-tsb-2022.pdf]]", "[[raw/claude-2026-09-27-foundations-1-1-who-regulates-what.md]]"]
created: "2026-10-14"
updated: "2026-10-14"
tags: ["uk-financial-regulation", "operational-resilience"]
---
# TSB Bank

A UK retail bank whose 2018 IT migration failed and was fined £29.75m by the FCA ([[raw/fca-final-notice-tsb-2022.pdf#page=1]], para 1.1; [[raw/fca-final-notice-tsb-2022.pdf#page=13]], para 4.2). The PRA also fined it for the same incident ([[raw/claude-2026-09-27-foundations-1-1-who-regulates-what.md]] · AI).

## What the sources say

### History
- TSB was created by a divestment from Lloyds Banking Group (LBG) in June 2014 ([[raw/fca-final-notice-tsb-2022.pdf#page=2]], para 2.1).
- It offers current accounts, business banking, savings, mortgages, insurance, loans and credit cards, through internet, mobile, telephone and branches. It had about 5.2 million customers in 2015–2018 ([[raw/fca-final-notice-tsb-2022.pdf#page=13]], para 4.2).
- After the divestment it kept using the LBG IT platform under an outsourcing agreement, with an option to stay until July 2024 ([[raw/fca-final-notice-tsb-2022.pdf#page=2]], para 2.1).
- **Sabadell.** Banco de Sabadell, registered in Spain, bid for TSB in March 2015 and acquired it in July 2015 ([[raw/fca-final-notice-tsb-2022.pdf#page=2]], para 2.2; [[raw/fca-final-notice-tsb-2022.pdf#page=22]], para 4.32). Sabadell had migrated seven acquired banks onto its own platform, Proteo, built in 2000 with acquisitions in mind, but had never customised it for the UK ([[raw/fca-final-notice-tsb-2022.pdf#page=22]], paras 4.32, 4.34). Its offer estimated IT cost savings of about £160m a year from a full migration of TSB onto Proteo, and that migration was part of the takeover's rationale ([[raw/fca-final-notice-tsb-2022.pdf#page=22]], paras 4.32–4.33).
- **SABIS.** Sabadell's IT subsidiaries, SABIS Spain and SABIS UK, designed, built and tested the new UK platform, Proteo4UK, migrated the data, and would run the platform afterwards ([[raw/fca-final-notice-tsb-2022.pdf#page=2]], para 2.4; [[raw/fca-final-notice-tsb-2022.pdf#page=27]], para 4.53).

### The 2018 migration
- The main migration went live on 22 April 2018, moving most of TSB's corporate systems, customer services and customer data from the LBG platform to Proteo4UK ([[raw/fca-final-notice-tsb-2022.pdf#page=14]], paras 4.4–4.5). The notice gives the weekend as "20 - 22 April" in some paragraphs and "21/22 April" in others ([[raw/fca-final-notice-tsb-2022.pdf#page=2]], para 2.5; [[raw/fca-final-notice-tsb-2022.pdf#page=50]], para 4.139).
- The data migration itself was successful, but serious problems began from an early point after go-live ([[raw/fca-final-notice-tsb-2022.pdf#page=14]], para 4.4).
- Digital, telephone and branch banking were disrupted, with data breaches and knock-on payment and debit-card problems ([[raw/fca-final-notice-tsb-2022.pdf#page=3]], para 2.5).
- The disruption hit all 550 branches and a significant proportion of customers ([[raw/fca-final-notice-tsb-2022.pdf#page=98]], para 6.8).
- TSB did not return to business as usual until 10 December 2018 ([[raw/fca-final-notice-tsb-2022.pdf#page=3]], para 2.7).
- The digital outage came from a configuration fault in the Active-Active set-up of the two data centres: customer sessions moved between them ([[raw/fca-final-notice-tsb-2022.pdf#page=61]], para 4.184). Details are on [[wiki/sources/Source - FCA Final Notice to TSB Bank 2022]].

### Two regulators, one incident
- In December 2022 the FCA fined TSB £29.75m ([[raw/fca-final-notice-tsb-2022.pdf#page=1]], para 1.1).
- The FCA's figure was after a 30% Stage 1 settlement discount; without it the penalty would have been £42.50m ([[raw/fca-final-notice-tsb-2022.pdf#page=1]], para 1.2).
- The FCA took into account the PRA's proposed penalty on TSB "arising from the same events and substantially the same facts and matters" ([[raw/fca-final-notice-tsb-2022.pdf#page=100]], para 6.18).
- In December 2022 the PRA fined TSB £18.9m ([[raw/claude-2026-09-27-foundations-1-1-who-regulates-what.md]] · AI).
- The two fines totalled £48.65m ([[raw/claude-2026-09-27-foundations-1-1-who-regulates-what.md]] · AI).
- **The FCA's findings.**
  - A breach of [[wiki/concepts/Principles for Businesses]] Principle 2 (due skill, care and diligence), in managing the outsourcing to SABIS and in the decision not to test in Active-Active configuration ([[raw/fca-final-notice-tsb-2022.pdf#page=93]], [[raw/fca-final-notice-tsb-2022.pdf#page=94]], paras 5.2–5.5).
  - A breach of Principle 3 (organising and controlling the programme with adequate risk management) ([[raw/fca-final-notice-tsb-2022.pdf#page=95]], para 5.6).
  - TSB received 225,492 complaints between 22 April 2018 and 7 April 2019 ([[raw/fca-final-notice-tsb-2022.pdf#page=3]], para 2.8).
  - It paid £32,705,762 in redress over that period ([[raw/fca-final-notice-tsb-2022.pdf#page=3]], para 2.8).
  - Its planning for vulnerable customers in a long incident was inadequate ([[raw/fca-final-notice-tsb-2022.pdf#page=96]], para 5.6(d)(iii)).
- **The PRA's framing: prudential.**
  - The PRA treated the same events as a safety-and-soundness failure ([[raw/claude-2026-09-27-foundations-1-1-who-regulates-what.md]] · AI).
  - The Bank's release said governance, operational risk, business continuity and outsourcing management have long been part of prudential rules ([[raw/claude-2026-09-27-foundations-1-1-who-regulates-what.md]] · AI).
  - The PRA's general expectation that firms manage operational as well as financial risks is in `raw/`: see [[wiki/concepts/Operational resilience]]. That the release said so about TSB is not.

### What drove the decisions
- The first migration plan was "designed back from the y/end 2017 deadline", on a "right-to-left" basis ([[raw/fca-final-notice-tsb-2022.pdf#page=24]], para 4.40).
- TSB publicly announced migration in Q1 2018 nine days after deciding to re-plan, before the re-plan was complete ([[raw/fca-final-notice-tsb-2022.pdf#page=41]], para 4.106).
- A decision to cut performance testing on the digital channels to one data centre, instead of Active-Active, was treated as purely technical and taken informally, outside the governance structure ([[raw/fca-final-notice-tsb-2022.pdf#page=5]], para 2.14; [[raw/fca-final-notice-tsb-2022.pdf#page=65]], para 4.195).
- Had that testing been done, the configuration problem that took internet and mobile banking down would likely have been found ([[raw/fca-final-notice-tsb-2022.pdf#page=5]], para 2.14).
- To keep its Internal Ratings Based approach to capital, TSB had to migrate to Proteo4UK by June 2018 ([[raw/fca-final-notice-tsb-2022.pdf#page=47]], para 4.126).
- A successful migration was hoped to release extra capital the PRA had required against the risks of outsourcing to another major UK bank ([[raw/fca-final-notice-tsb-2022.pdf#page=21]], para 4.30).
- Go-live attestations, testing scope and SABIS's readiness are set out in full on [[wiki/sources/Source - FCA Final Notice to TSB Bank 2022]].

## Mentioned in
- [[wiki/sources/Source - FCA Final Notice to TSB Bank 2022]]
- [[wiki/sources/Source - Claude on who regulates what (2026-09-27)]]

## Related
- [[wiki/concepts/Operational resilience]]
- [[wiki/concepts/Outsourcing of critical or important functions]]
- [[wiki/concepts/Principles for Businesses]]
- [[wiki/concepts/Solo and dual regulation]]
- [[wiki/entities/Financial Conduct Authority]]
- [[wiki/entities/Prudential Regulation Authority]]
