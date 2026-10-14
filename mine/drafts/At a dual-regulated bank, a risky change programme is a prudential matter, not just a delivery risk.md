---
type: insight
status: draft
origin: claude
created: "2026-10-14"
related: ["[[wiki/concepts/Operational resilience]]", "[[wiki/entities/TSB Bank]]", "[[wiki/concepts/Solo and dual regulation]]"]
---
# At a dual-regulated bank, a risky change programme is a prudential matter, not just a delivery risk

For a product owner at a bank, a large migration or platform change isn't only a project with a deadline. The PRA treats the bank's ability to keep its important services running as part of safety and soundness, so a failed change can bring a prudential case on top of a conduct case. Go-live decisions, and cuts to testing, belong in governance, not in a technical side-channel.

## Why I think this
- The PRA expects firms to manage operational as well as financial risks to "high standards", and assumes disruptions will happen ([[raw/pra-approach-banking-supervision-2023.pdf#page=36]]).
- Firms must stay within impact tolerances for important business services in severe but plausible scenarios, and the board is accountable for operational resilience, including the firm's technology ([[raw/pra-approach-banking-supervision-2023.pdf#page=36]]).
- The FCA supervises every authorised person, and the PRA adds itself for firms with a PRA-regulated activity, so a bank answers to both for the same event ([[raw/uk-parliament-fsma-2000-part-1a.md]], ss. 1L(1), 2K).
- TSB's 2018 migration brought an FCA fine for conduct and a PRA fine for safety and soundness ([[raw/claude-2026-09-27-foundations-1-1-who-regulates-what.md]] · AI). A cut to performance testing was decided outside the proper governance forum ([[raw/claude-2026-09-27-foundations-1-1-who-regulates-what.md]] · AI). These two steps are leads until the FCA notice is in `raw/`.
- So the product owner's role in a change programme includes making sure that go-live and testing trade-offs reach the forum that owns operational risk (reasoning).

## Relations
- supports:: [[wiki/concepts/Operational resilience]]
- extends:: [[wiki/concepts/Solo and dual regulation]]
- extends:: [[wiki/entities/TSB Bank]]
- source:: [[wiki/sources/Source - The PRA's approach to banking supervision]]
- source:: [[wiki/sources/Source - Claude on who regulates what (2026-09-27)]]
