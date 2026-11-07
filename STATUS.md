# Northstar package: current status (Nov 7)

A single snapshot to share with collaborators who can't see the live organizer.

## Why the uploaded organizer looked out of date
The Working Organizer artifact holds only its built-in starter content in the page file. Edits are saved separately to the account's data store and load when you open the page in Claude. A downloaded or uploaded copy of the HTML therefore shows the old template: five stops, and only Lead alignment filled in. That copy doesn't reflect the current plan.

**Current saved state:** version 621, last saved Nov 7, 03:28 UTC. There are **four stops, all filled in**. The fifth stop was removed earlier.

| Stop | What it contains now | Status |
|---|---|---|
| 01 Lead alignment | What Leads know and need; 25-min meeting agenda (3 / 19 [9 cases + 10 alignment] / 3); objectives; coaching-cue table; takeaway resources (one-pager, Coaching Cues); Moving Forward (temporary thread Admin = a participating Lead designated by Care leadership; Lead actions) | Locked design (item 95) |
| 02 Equip Guides | What Guides need (incl. Customer Communication, Cues, Proper Sequence, recovery completeness); 7 Guide actions + 2 pending/readiness items; rollout dependencies; Guide resources map (Call Path, huddle slide, scenario, Plus FAQ, Orbit video) | Locked design |
| 03 Rollout & Reinforcement | Success statement; Malik quote; six observable indicators; five-phase framework with gates (Prepare, Pilot, Observe & Adjust, Expand, Sustain) | Locked design |
| 04 Ownership | Decision authority (Care leadership + partner table); accountability by area; Mateo's two separate approvals; thread Admin; sustainment ownership | Locked design (item 94) |

## Deliverables (`TN-UOP-FIN/deliverables/`)

| Deliverable | Files | Status | Decision |
|---|---|---|---|
| Rollout & Reinforcement Plan | `wn7-rollout-plan.pdf` (5 pp) + `-print.html` (the earlier long HTML draft `wn7-rollout-plan.html` is kept for reference only) | **Locked** | 100 |
| Lead Alignment 25-min meeting plan | `wn7-lead-meeting-plan.pdf` (3 pp) + `-print.html` | **Locked** | 104 |
| Lead Quick Reference (one-pager) | `wn7-lead-quick-reference.pdf` (1 p) + `-print.html` | **Locked** | 106 |
| Lead Coaching Cues | `wn7-coaching-cues.pdf` (1 p) + `-print.html` | **Locked** | 108 |
| Guide Call Path | `wn7-guide-call-path.html` (interactive) + `.pdf` (1 p) + `-print.html` | **Locked** | 111 |
| Digital practice scenario "Make the Call" | `wn7-practice-scenario.html` | **Locked** | 114 |
| Resource Overview | `wn7-resource-overview.html` (links to the deliverables by relative path; must sit in the same folder in the ZIP) | **Locked** | 115–121, 127–128 |
| Ownership Map Overview | `wn7-ownership-map.html` (single page; same folder in the ZIP) | **Locked** | 124 |
| Rollout Plan Overview | `wn7-rollout-overview.html` (single page; links to the Ownership Map and the plan PDF, so same folder in the ZIP) | **Locked** | 125–126 |
| Huddle Sequence Slide | `wn7-huddle-slide.html` (source) + `.pdf` (1 widescreen page) | **Locked** | 129–130 |
| Dana pre-read email | `email/wn7-dana-pre-read-email.md` (not sent; cover for the ZIP) | **Locked** (not sent) | 131–133 |
| Shared asset | `assets/northstar-logo-white.png` (must ship next to the HTML files) | — | — |

## Reconciling the plan against what's built

| Planned item (organizer / RESOURCES.md) | Built? | Note |
|---|---|---|
| R2 Lead meeting · R1 one-pager · R5 Coaching Cues | Yes | Lead Alignment set complete |
| R6 Guide Call Path | Yes | HTML + PDF |
| R8 individual digital scenario | Yes | |
| **R8 team huddle sequence slide** | Yes (item 130) | `wn7-huddle-slide.html` + `.pdf`; linked from the Resource Overview |
| R3 shared Lead thread | n/a | Operational arrangement; covered in the rollout plan, no artifact needed |
| R4 Orbit serial-tool video | Not planned to build | Optional and conditional on approved screen access; not a launch prerequisite |
| R7 Plus FAQ in Beacon | Not ours to build | Partner-owned proposal (Content Editor + Plus owner); Learning proposes and hands off. Could be a one-paragraph handoff note in the Dana materials |
| 04 Ownership | Covered | Inside the rollout plan, page 5 |
| **Dana's pre-read email** (required by the brief) | Yes (item 133) | Orients Dana to the materials, the recommended direction, and where to look first |
| **Interviewer note** (required by the brief, separate from Dana's materials) | **No** | Approach, harness use, sources, checks and corrections, uncertainties, with concrete examples |
| ZIP packaging | **No** | Two clearly labeled parts: Dana's pre-read, and the interviewer note |

## Suggested order for what's left
1. **Interviewer note** (draws on DECISIONS.md, CALL_PATH_AUDIT.md and the corrections log).
2. **ZIP packaging and final export check** in three folders (01 — Start Here · 02 — Detailed Planning · 03 — Learning Resources; item 131), with relative links re-tested and `assets/` (logo and `ro-*.jpg`) placed where the HTML expects it.
3. Optional visual polish, only after everything else is locked (item 101 rule).

## Carry-forward notes for the final pass
- Meeting plan p. 2: "with a verified serial" → "with a serial check recorded" (item 104).
- Release dependencies to keep visible in the proposal: Care Systems (Orbit result display, General Care access, recovery queue routing), Account Systems / Product Ops (credit not yet `Applied`), Product Ops (eligibility review case follow-up expectation), Learning Operations (Sana delivery), Workforce (practice time), Quality + Specialist Care (model answers and Lead content), Care leadership (fallback when a Lead is unavailable), Mateo (Specialist approvals A and B).
- Test claims: describe browser checks as Claude's automated suite, not independently reproduced; screen-reader testing has not been done.
