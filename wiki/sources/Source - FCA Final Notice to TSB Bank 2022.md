---
type: source
status: verified
trust: primary
sources: ["[[raw/fca-final-notice-tsb-2022.pdf]]", "[[raw/claude-2026-09-27-foundations-1-1-who-regulates-what.md]]"]
created: "2026-10-14"
updated: "2026-10-14"
tags: ["uk-financial-regulation", "operational-resilience"]
---
# Source - FCA Final Notice to TSB Bank 2022

**Raw file:** [[raw/fca-final-notice-tsb-2022.pdf]] · **Author or publisher:** Financial Conduct Authority, Enforcement and Market Oversight Division · **Published:** 2022-12-20 · **Trust:** primary (a regulator's own publication) · **Ingested:** 2026-10-14

Page citations use the PDF's page numbers, which match the printed ones. Paragraph numbers are the notice's own.

## Summary
The FCA's Final Notice fining [[wiki/entities/TSB Bank]] £29.75m for its 2015–2018 IT migration programme. TSB moved its customer services off the Lloyds Banking Group platform onto Proteo4UK, a new platform built and run by Sabadell's IT subsidiary SABIS. The data migrated, but from the go-live on 22 April 2018 digital, telephone and branch services failed, and TSB did not return to business as usual until 10 December 2018. The FCA found breaches of [[wiki/concepts/Principles for Businesses]] 2 (due skill, care and diligence, in managing SABIS and in one testing decision) and 3 (organisation, control and risk management: planning, governance, risk reporting and business continuity). The notice sets out the facts, the failings, the five-step penalty calculation and, in Annex A, the rules relied on, including the SYSC [[wiki/concepts/Outsourcing of critical or important functions]] rules ([[raw/fca-final-notice-tsb-2022.pdf#page=1]], [[raw/fca-final-notice-tsb-2022.pdf#page=2]], [[raw/fca-final-notice-tsb-2022.pdf#page=3]], [[raw/fca-final-notice-tsb-2022.pdf#page=10]]).

## Key claims

### The incident
- **Go-live.** The main migration event (MME) was authorised at about 1pm on 22 April 2018. Telephony and internet banking were live by 6pm and the mobile app by 6.45pm ([[raw/fca-final-notice-tsb-2022.pdf#page=14]], para 4.5). The notice puts the MME weekend at "20 - 22 April 2018" in some places (paras 2.5, 4.128) and "21/22 April 2018" in others (paras 4.139, 4.151–4.153); 22 April is the go-live date in every passage ([[raw/fca-final-notice-tsb-2022.pdf#page=2]], [[raw/fca-final-notice-tsb-2022.pdf#page=50]], [[raw/fca-final-notice-tsb-2022.pdf#page=54]]).
- **What failed.** The data migration itself was successful, but from an early point after go-live TSB had data breaches and failures in digital, telephone and branch banking, with knock-on problems for payments and debit cards ([[raw/fca-final-notice-tsb-2022.pdf#page=14]], para 4.4).
  - About 40 customers reported seeing other people's finances, and digital banking was taken down at 7pm on 22 April. 440 customers were later confirmed to have had this issue ([[raw/fca-final-notice-tsb-2022.pdf#page=14]], [[raw/fca-final-notice-tsb-2022.pdf#page=15]], paras 4.6–4.7).
  - On 23 April about 10% of roughly 900,000 internet banking logins succeeded, and 48% of mobile-app and 59% of internet-banking payments failed ([[raw/fca-final-notice-tsb-2022.pdf#page=15]], para 4.9).
  - IVR configuration left only c.25% of planned telephone capacity. Callers who reached the IVR waited about 90 minutes, with a 70% abandon rate ([[raw/fca-final-notice-tsb-2022.pdf#page=15]], [[raw/fca-final-notice-tsb-2022.pdf#page=16]], paras 4.11–4.12).
- **Root cause in digital.** In the Active-Active set-up of two data centres, customer sessions were not kept on one data centre: OpenAM requests went to the Global Load Balancer instead of the local one, and OpenAM was wrongly configured as a cross-site cluster. Customers saw "your session has expired" errors, and digital channels were at times wholly unavailable in week one ([[raw/fca-final-notice-tsb-2022.pdf#page=61]], [[raw/fca-final-notice-tsb-2022.pdf#page=62]], paras 4.184–4.186).
- **Duration.** TSB did not return to business as usual until 10 December 2018 ([[raw/fca-final-notice-tsb-2022.pdf#page=3]], para 2.7).
- **Scale.** TSB had about 5.2 million customers ([[raw/fca-final-notice-tsb-2022.pdf#page=13]], para 4.2). The disruption hit all 550 branches and a significant proportion of customers ([[raw/fca-final-notice-tsb-2022.pdf#page=98]], para 6.8).
- **Complaints and redress.** 225,492 complaints between 22 April 2018 and 7 April 2019 (c.4.3% of customers), and £32,705,762 paid in redress ([[raw/fca-final-notice-tsb-2022.pdf#page=3]], para 2.8). By 26 April, 10,315 complaints had been logged against 1,146 expected ([[raw/fca-final-notice-tsb-2022.pdf#page=19]], para 4.25). TSB expected 2,000 complaints in week one and received about 37,000, and took almost 12 months to deal with migration complaints ([[raw/fca-final-notice-tsb-2022.pdf#page=91]], paras 4.304, 4.307).

### Background
- TSB was created by a divestment from Lloyds Banking Group in June 2014 and kept using the LBG IT platform under an outsourcing agreement, with an option to stay until July 2024 ([[raw/fca-final-notice-tsb-2022.pdf#page=2]], para 2.1).
- Sabadell acquired TSB in July 2015. A full migration onto Sabadell's Proteo platform, aimed for the end of 2017, was part of the strategic rationale for the takeover ([[raw/fca-final-notice-tsb-2022.pdf#page=2]], para 2.2). Sabadell had migrated seven banks onto Proteo, but never customised it for the UK ([[raw/fca-final-notice-tsb-2022.pdf#page=22]], paras 4.32, 4.34).
- SABIS Spain designed, built and tested Proteo4UK and migrated TSB's data. SABIS would also run the platform ([[raw/fca-final-notice-tsb-2022.pdf#page=2]], para 2.4).
- **Why exit LBG.** Strategic flexibility, cost savings, and capital: the PRA had required TSB to hold extra capital against the risk of outsourcing to another major UK bank, and a successful migration was hoped to release it ([[raw/fca-final-notice-tsb-2022.pdf#page=21]], para 4.30).
- **No roll-back.** With a predominantly single-event migration, once TSB served notice on LBG and migrated, it was "essentially impossible" to revert to the LBG platform ([[raw/fca-final-notice-tsb-2022.pdf#page=26]], [[raw/fca-final-notice-tsb-2022.pdf#page=27]], paras 4.48, 4.50–4.51).

### Product-owner lessons (emphasis)
**A date-driven plan**
- The first plan was "designed back from the y/end 2017 deadline" and was "top-down and 'right-to-left'" ([[raw/fca-final-notice-tsb-2022.pdf#page=24]], para 4.40). The March 2016 IMP kept the late-2017 date although the design phase was three months late ([[raw/fca-final-notice-tsb-2022.pdf#page=35]], paras 4.85–4.86).
- In September 2017 TSB admitted the date had been "deliberately very ambitious" and "based on very little information" ([[raw/fca-final-notice-tsb-2022.pdf#page=41]], para 4.105). Nine days after deciding to re-plan, before the re-plan was done, it publicly announced migration in Q1 2018 ([[raw/fca-final-notice-tsb-2022.pdf#page=41]], para 4.106).
- The re-plan ("Defender Plan") set 15 Guiding Principles, including fewer parallel workstreams (3), a clean migration acceptance cycle before dress rehearsals (4) and an explicit regression test phase (10) ([[raw/fca-final-notice-tsb-2022.pdf#page=43]], para 4.112). All three were departed from to migrate in April 2018 ([[raw/fca-final-notice-tsb-2022.pdf#page=53]], para 4.149).
- **The clock.** In January 2018 TSB learned that keeping its Internal Ratings Based approach to capital required migration by June 2018. Risk Oversight called this "a regulatory reputational risk" ([[raw/fca-final-notice-tsb-2022.pdf#page=47]], para 4.126). On 23 February 2018 Sabadell announced publicly that the MME would be on 21 April 2018 ([[raw/fca-final-notice-tsb-2022.pdf#page=47]], para 4.127).

**Testing scope**
- Functional testing, due by March 2017 under the IMP and January 2018 under the Defender Plan, ran into April 2018 and was closed by deferring and de-scoping functionality ([[raw/fca-final-notice-tsb-2022.pdf#page=55]], [[raw/fca-final-notice-tsb-2022.pdf#page=56]], paras 4.161, 4.163). The planned regression phase did not happen ([[raw/fca-final-notice-tsb-2022.pdf#page=56]], para 4.164).
- No pre-production environment was available, so most non-functional testing ran in production ([[raw/fca-final-notice-tsb-2022.pdf#page=58]], para 4.173).
- **The Active-Active decision.** After the Migration Testing Forum of 28 February 2018, TSB accepted a SABIS "counter-proposal" to run performance testing in one data centre, to avoid taking live services (e.g. ATMs) down for three to four hours ([[raw/fca-final-notice-tsb-2022.pdf#page=64]], para 4.192). TSB treated it as purely technical: it was taken informally, outside governance, undocumented and not escalated ([[raw/fca-final-notice-tsb-2022.pdf#page=65]], para 4.195). Had Active-Active testing been done, the configuration problem would likely have been found ([[raw/fca-final-notice-tsb-2022.pdf#page=5]], para 2.14; [[raw/fca-final-notice-tsb-2022.pdf#page=65]], para 4.194).
- The NFT Final Report said tests ran "on half the installed capacity (one data centre only)" but named no risk from that, so the business functions attesting were unaware of any ([[raw/fca-final-notice-tsb-2022.pdf#page=66]], [[raw/fca-final-notice-tsb-2022.pdf#page=67]], para 4.203).

**Go-live attestations**
- TSB's go/no-go rested on an Assurance Matrix (five programme components × four performance standards) and a 972-page "T3 Memo" ([[raw/fca-final-notice-tsb-2022.pdf#page=49]], [[raw/fca-final-notice-tsb-2022.pdf#page=50]], paras 4.134, 4.137). Each Bank Executive Committee (BEC) business function had to attest in writing that its area was ready ([[raw/fca-final-notice-tsb-2022.pdf#page=49]], para 4.136).
- On 9 February 2018 the BEC Design Executive changed this: business functions would sign off their non-functional requirements, relying on the IT function's statement of what had been tested ([[raw/fca-final-notice-tsb-2022.pdf#page=66]], para 4.201). The board was not explicitly told of the change when deciding to go ahead ([[raw/fca-final-notice-tsb-2022.pdf#page=67]], para 4.205).
- The NFT Final Report (65 pages) circulated on the afternoon of 17 April 2018, and its two-page summary went to the business functions at 17.19 that day. They relied on the summary to answer the testing questions ([[raw/fca-final-notice-tsb-2022.pdf#page=66]], para 4.202). On 10 April none of the attestations was complete, and the board did not challenge that ([[raw/fca-final-notice-tsb-2022.pdf#page=51]], para 4.142). On 18 April eight areas of "must-have" functionality were still open ([[raw/fca-final-notice-tsb-2022.pdf#page=52]], para 4.147).
- Risk Oversight's oversight of the programme ended on 8 April 2018, about two weeks before MME, at the BEC's request ([[raw/fca-final-notice-tsb-2022.pdf#page=71]], para 4.224).

**Outsourcer readiness**
- TSB never ran a formal, comprehensive assessment of SABIS's ability to deliver and operate Proteo4UK, at the outset or once its requirements were defined ([[raw/fca-final-notice-tsb-2022.pdf#page=72]], [[raw/fca-final-notice-tsb-2022.pdf#page=73]], paras 4.229, 4.235).
- SABIS relied on 85 fourth parties, 11 of them Material Subcontractors. TSB had no contract with them but kept its regulatory responsibility ([[raw/fca-final-notice-tsb-2022.pdf#page=76]], para 4.247).
- SABIS's readiness letter of 5 April 2018 and the fourth-party confirmations were "forward looking statements of good intention or expectations rather than statements of fact", all but one caveated, and TSB did not ask for updates before the 18 April decision ([[raw/fca-final-notice-tsb-2022.pdf#page=78]], [[raw/fca-final-notice-tsb-2022.pdf#page=79]], paras 4.255, 4.258).
- The IT function's attestation on SABIS was a single paragraph repeating SABIS's expectation. It did not attest to any steps SABIS had taken; "only a SABIS employee would be able to attest to those steps" ([[raw/fca-final-notice-tsb-2022.pdf#page=79]], [[raw/fca-final-notice-tsb-2022.pdf#page=80]], paras 4.260–4.261).
- Internal Audit tested SABIS's readiness on services already live, which were simpler than those that went live at MME, and did not clearly say so ([[raw/fca-final-notice-tsb-2022.pdf#page=78]], para 4.254).

**Business continuity**
- TSB prepared for "bumps in the road", not "a massive failure in the configuration leading to an erratic digital service" ([[raw/fca-final-notice-tsb-2022.pdf#page=81]], para 4.267). In its view it would not have migrated had it thought an incident of that scale possible ([[raw/fca-final-notice-tsb-2022.pdf#page=80]], para 4.264).
- Its practice Gold events assumed incidents resolved in a few days and involved BEC members only, not SABIS ([[raw/fca-final-notice-tsb-2022.pdf#page=87]], paras 4.286–4.287). Its Incident Management Playbooks covered the first 48 hours ([[raw/fca-final-notice-tsb-2022.pdf#page=88]], para 4.291).
- One senior executive later estimated TSB would have needed seven times the telephony staff ([[raw/fca-final-notice-tsb-2022.pdf#page=91]], para 4.302). Complaints plans allowed for a 100% increase, mostly from internal staff who were not available in a bank-wide disruption ([[raw/fca-final-notice-tsb-2022.pdf#page=91]], para 4.305).
- No playbook made specific provision for vulnerable customers. TSB began reaching out to them only after setting up a Customer War Room four days after MME ([[raw/fca-final-notice-tsb-2022.pdf#page=89]], para 4.294).

### The breaches
- **Principle 2.** TSB failed to exercise due skill, care and diligence in managing the outsourcing to SABIS and its risks: no formal assessment of SABIS at the outset; testing departing from plans; no ongoing reassessment; too little grasp of SABIS's infrastructure design and build; too little assurance on fourth parties and on readiness; GTE service problems not interrogated ([[raw/fca-final-notice-tsb-2022.pdf#page=93]], [[raw/fca-final-notice-tsb-2022.pdf#page=94]], paras 5.2–5.3). Also the Active-Active testing decision and its being taken outside governance ([[raw/fca-final-notice-tsb-2022.pdf#page=94]], paras 5.4–5.5).
- **Principle 3.** TSB failed to organise and control the programme with adequate risk management: an "overly right-to-left" plan and re-plan, a public commitment before the re-plan was approved, board governance that did not challenge the timetable, deviations or readiness, risk management that missed SABIS non-performance and passed on qualified assurances unflagged, and incident management and business continuity that were "insufficiently robust and ineffective" ([[raw/fca-final-notice-tsb-2022.pdf#page=95]], [[raw/fca-final-notice-tsb-2022.pdf#page=96]], para 5.6).
- **Negligent, not deliberate.** The breaches were committed negligently; the FCA did not find that TSB acted deliberately or recklessly ([[raw/fca-final-notice-tsb-2022.pdf#page=99]], paras 6.13–6.14).

### The penalty
- **Power.** Financial penalty under s. 206 FSMA, which lets the FCA fine an authorised person that has contravened a requirement imposed by or under the Act ([[raw/fca-final-notice-tsb-2022.pdf#page=1]], para 1.1; [[raw/fca-final-notice-tsb-2022.pdf#page=103]], Annex A 1.2).
- **Five steps (DEPP 6.5A).** For conduct from 6 March 2010 the FCA uses a five-step framework ([[raw/fca-final-notice-tsb-2022.pdf#page=96]], para 6.1):
  1. disgorgement of financial benefit: £0, none identified ([[raw/fca-final-notice-tsb-2022.pdf#page=97]], paras 6.3–6.4);
  2. seriousness: revenue (about £3.3bn) was not used as an indicator because it would be disproportionate; level 4, £50m ([[raw/fca-final-notice-tsb-2022.pdf#page=97]], para 6.6; [[raw/fca-final-notice-tsb-2022.pdf#page=99]], para 6.15);
  3. aggravating and mitigating factors: none aggravating; the remediation programme and voluntary reviews mitigated; the FCA also took account of the PRA's proposed penalty for the same events; minus 15% to £42.50m ([[raw/fca-final-notice-tsb-2022.pdf#page=99]], [[raw/fca-final-notice-tsb-2022.pdf#page=100]], paras 6.17–6.19);
  4. deterrence: no increase, £42.50m ([[raw/fca-final-notice-tsb-2022.pdf#page=100]], paras 6.21–6.22);
  5. settlement discount: agreement at Stage 1 gives 30%, so £29.75m ([[raw/fca-final-notice-tsb-2022.pdf#page=101]], paras 6.24–6.25).
- **The PRA.** The FCA took into account "the action proposed by the PRA to impose a financial penalty on TSB arising from the same events and substantially the same facts and matters" ([[raw/fca-final-notice-tsb-2022.pdf#page=100]], para 6.18). The notice gives no PRA amount.
- **Payment.** Due in full by 4 January 2023 ([[raw/fca-final-notice-tsb-2022.pdf#page=101]], para 7.4).

### The rules (Annex A)
- The Principles are "a general statement of the fundamental obligations of firms under the regulatory system". Principle 2: conduct business with due skill, care and diligence. Principle 3: take reasonable care to organise and control affairs responsibly and effectively, with adequate risk management systems ([[raw/fca-final-notice-tsb-2022.pdf#page=103]], [[raw/fca-final-notice-tsb-2022.pdf#page=104]], Annex A 2.2). See [[wiki/concepts/Principles for Businesses]].
- SYSC 8.1 outsourcing rules, SYSC 7.1.2R risk control and SYSC 4.1.6R–4.1.7R business continuity are quoted for 2015–2018, with the MiFID Org Regulation from 3 January 2018; the FCA says the post-2018 rules are not substantively different ([[raw/fca-final-notice-tsb-2022.pdf#page=104]], Annex A 2.3; [[raw/fca-final-notice-tsb-2022.pdf#page=112]], [[raw/fca-final-notice-tsb-2022.pdf#page=113]]). See [[wiki/concepts/Outsourcing of critical or important functions]] and [[wiki/concepts/Operational resilience]].

## Entities and concepts
- [[wiki/entities/TSB Bank]] (Sabadell, SABIS and Proteo facts kept there)
- [[wiki/entities/Financial Conduct Authority]] (penalty mechanics)
- [[wiki/concepts/Principles for Businesses]] (new)
- [[wiki/concepts/Outsourcing of critical or important functions]] (new)
- [[wiki/concepts/Operational resilience]]
- [[wiki/concepts/Solo and dual regulation]]
- Mentioned without a page: Banco Sabadell and SABIS, DEPP 6.5A, the MiFID Org Regulation.

## Conflicts and open points
- **The migration weekend.** The notice itself gives "20 - 22 April 2018" and "21/22 April 2018" in different paragraphs. The go-live date, 22 April 2018, is common to both and is the one the wiki states.
- **Backs a Claude output.** 20 claims about TSB that [[raw/claude-2026-09-27-foundations-1-1-who-regulates-what.md]] credited to this notice are now cited to it on [[wiki/entities/TSB Bank]]. The note's PRA figures (£18.9m, a £48.65m total) and the PRA's safety-and-soundness framing are not in this notice; they need the Bank of England's release of the same day, which is on the capture list.
- **Rules as at 2015–2018.** Annex A quotes the rules in force during the relevant period. Current SYSC text is not in `raw/`.
