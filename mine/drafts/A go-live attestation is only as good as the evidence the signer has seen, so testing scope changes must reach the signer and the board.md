---
type: insight
status: draft
origin: claude
created: "2026-10-14"
related: ["[[wiki/sources/Source - FCA Final Notice to TSB Bank 2022]]", "[[wiki/entities/TSB Bank]]", "[[wiki/concepts/Principles for Businesses]]", "[[wiki/concepts/Operational resilience]]"]
---
# A go-live attestation is only as good as the evidence the signer has seen, so testing scope changes must reach the signer and the board

When a product owner signs that their area is ready to go live, the signature carries the risks hidden in the testing behind it. At TSB, a cut in testing scope was decided informally, the test report didn't name its risk, and the people signing relied on a two-page summary received the evening before the board met. A readiness sign-off should therefore record what was not tested and why, and any change to who attests to what should go to the board.

## Why I think this
- TSB decided informally, outside its governance and undocumented, to run performance testing in one data centre rather than the two-centre Active-Active set-up it would go live on ([[raw/fca-final-notice-tsb-2022.pdf#page=64]], para 4.192; [[raw/fca-final-notice-tsb-2022.pdf#page=65]], para 4.195). Had it tested Active-Active, the configuration fault that took internet and mobile banking down would likely have been found ([[raw/fca-final-notice-tsb-2022.pdf#page=5]], para 2.14).
- On 9 February 2018 the business functions became responsible for signing off non-functional requirements on the strength of the IT function's statement of what had been tested ([[raw/fca-final-notice-tsb-2022.pdf#page=66]], para 4.201). The board was not explicitly told of this change when it decided to proceed ([[raw/fca-final-notice-tsb-2022.pdf#page=67]], para 4.205).
- The final test report said the tests ran on "half the installed capacity (one data centre only)" but named no risk from it, so the business functions attesting were unaware of any ([[raw/fca-final-notice-tsb-2022.pdf#page=66]], [[raw/fca-final-notice-tsb-2022.pdf#page=67]], para 4.203). They relied on a two-page summary sent at 17.19 on 17 April 2018 ([[raw/fca-final-notice-tsb-2022.pdf#page=66]], para 4.202), the day before the board met to decide ([[raw/fca-final-notice-tsb-2022.pdf#page=52]], para 4.146).
- The FCA counted the testing decision and its being taken outside governance as part of TSB's Principle 2 breach ([[raw/fca-final-notice-tsb-2022.pdf#page=94]], paras 5.4–5.5).
- So an attestation template that asks "what was not tested, who decided, and where was it recorded" would have surfaced the gap (reasoning). A product owner who signs without that is attesting to someone else's judgement (reasoning).

## Relations
- supports:: [[wiki/concepts/Principles for Businesses]]
- supports:: [[wiki/concepts/Operational resilience]]
- extends:: [[wiki/entities/TSB Bank]]
- source:: [[wiki/sources/Source - FCA Final Notice to TSB Bank 2022]]
