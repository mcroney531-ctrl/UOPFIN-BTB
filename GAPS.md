# Gap synthesis — draft for critical review

**Status: [Claude] first draft, for you and GPT to challenge.** Built from [`DECISIONS.md`](DECISIONS.md), [`SYNTHESIS.md`](SYNTHESIS.md), and [`WORKBOOKS.md`](WORKBOOKS.md). Nothing here is decided.

**Structure (proposed by GPT):** Layer 1 core performance gaps → Layer 2 dependencies and open questions → Layer 3 candidate design targets. Problems, plausible explanations, and proposed fixes are kept in separate columns.

**Evidence strength** (per GPT: not a source count). Rated on source type, directness, sample, and fit to the claim:
- **Strong** — systematic data *and* independent qualitative sources of different types agree.
- **Moderate** — several direct qualitative sources of different types, or data with an unclear cause.
- **Limited** — one source, self-report only, or inferred.

**Behavior column** uses Quality's six draft fields (item 52), plus three behaviors they don't score separately: stop redundant troubleshooting, explain accurately, continuity across contacts.

---

## Layer 1 — Core performance gaps

| # | Gap (confirmed problem) | Evidence | Strength | Behavior blocked | Plausible explanations (not confirmed) |
|---|---|---|---|---|---|
| **G1** | **Guides check the serial but don't act on the result** | 44% of eligible GC calls with a recorded serial check still ended in generic troubleshooting (Sep 21–30, n=159); Sep 28 Elias "older restart steps before anyone checked the serial"; Sep 24 Guide couldn't locate result, transferred | **Strong** | Appropriate path selected · stop redundant troubleshooting | Can't tell which Orbit value is the result (Sep 22) · Orbit permissions (Sep 24) · no visible next step / what to say (Guide R., item 34) · perceived review pressure to keep troubleshooting (item 31) |
| **G2** | **Plus isn't completed or its status isn't closed out** | Plus attached less often than replacement in both queues (GC 37% vs 44% of eligible; Specialist ~84% vs 100%); Dev, Harper, Sep 21–24 calibrations | **Strong** | Plus complete or follow-up opened · clear recap | Two separate transactions (Sep 9) · pending status with no guidance (items 9, 59) · Guide assumes order number = done (Priya, Sep 17) |
| **G3** | **Pattern not recognized early / serial never checked** | 22% of eligible GC calls had no serial check (Sep 21–30, n=204); Elias's 4-Guide test (1 of 4 landed on old article); Sep 22 customer-language searches failed | **Strong** on the gap; **moderate** on the search cause | Recognition of the pattern · serial eligibility checked | Search ranking and missing customer language (items 11, 24, 61) · "intermittent" title · product not recognized from customer words (item 11) · article reached shifts unevenly (Sep 28) |
| **G4** | **Plus explained inaccurately** | Guide L. (Sep 13), Micah (Sep 18), Sep 24 call "backup internet while the replacement is on the way"; customer asks if it fixes the drops | **Moderate** (recurring across 11 days, different source types; no data field) | Clear recap · explain accurately | Word of mouth before official guidance (item 8) · Plus genuinely has backup features, easy to overstate (item 13) |
| **G5** | **Acknowledgment doesn't turn into action** (the "pivot") | Quality: Guides name CLEAR but don't move to action (item 15); QA CLEAR "Act" does not meet 79/158 GC Sep 21–30 (nonrandom); Imani's experiment — generic empathy first, better on 2nd try (item 54); Sienna's "useful pivot" | **Moderate** (direct Quality observation + nonrandom QA) | Recognition · appropriate path (conversation side) | Newer Guides fear sounding cold (item 34) · reading every qualifier (item 40) · no clear next action to pivot *to* (overlaps G1) |
| **G6** | **Leads not equipped or aligned to coach the recovery** | Priya "not told Leads what to coach" (Sep 18); launch relied on Leads with no briefing (Sep 28); 2 of 18 Leads with planned huddles on launch day (Sep 21); Leads' own requests (cue, clip, pending answer); 15/18 completed generic CLEAR refresher, nothing WN7-specific tracked | **Moderate** (direct, multiple stakeholders; self-report; **center data does not show variation**) | All six fields (consistency of coaching and feedback) | No coaching cue or examples (items 18, 55) · Lead time and coverage load (items 46, 56) · no stable tool to coach to (item 38) |
| **G7** | **Next contact can't see what was done** | Dev's callback, Sep 20 four-call customer, Sep 22 serial in prior note, Sep 24 managers on sparse notes | **Moderate** (four instances, two source types; no data field) | Continuity across contacts (not in six fields) | No documentation standard (item 53) |
| **G8** | **Ineligible WN7 calls are long too** | Ineligible WN7-product GC calls ~16 min vs 8 pre-incident (data); Rina, Sofia, Priya on ineligible cases | **Moderate** — length is strong data; cause **unknown** | Appropriate path selected (ordinary path) | Real connectivity problems that take time · Guides unsure whether to stop troubleshooting · customers expecting a replacement after hearing about it |

**Context gap, not a Guide behavior:** Volume. WN7-containing contacts rose to ~39% of answered GC contacts and kept rising after Sep 21. Learning can shorten eligible calls (complete recovery ~11 min vs ~20 generic) but cannot reduce volume; the proactive notice may change volume again (Jules, Oct 1).

---

## Layer 2 — Dependencies and open questions (needed before Learning can responsibly teach)

| Dependency / question | Gap | Owner | Learning's role | Blocks next week? |
|---|---|---|---|---|
| What to say/do when Plus is **pending**; is pending normal | G2 | Account systems / Product Ops | **Draft** wording for approval; use Sep 9 rule ("case stays open") + Sep 24 model call meanwhile | Partly — "keep it open, follow up" is usable now |
| Orbit screen reference for the eligibility result | G1 | Care Systems + Product Ops | **Draft** the request; name the `WN7 eligibility` panel only | Partly — practice can use the panel name; exact screen can't be shown |
| General Care Orbit permissions for the panel | G1, G3 | Care Systems / Orbit admin | Ask the question | Unknown — could block G1 for some Guides |
| Customer-language search terms; title | G3 | Content editor / Knowledge Ops | **Submit** phrases via the existing feedback form (item 60) | No — runs in parallel |
| Six-field rubric adopted; coaching use first | G6 | Care Quality | Align Lead materials to it | No — can use as draft |
| Documentation expectation for repeat contacts | G7 | Care Ops / Quality | Propose as a reminder, not a standard | No |
| Group size × minutes per person | All | Workforce (Renee) | State both numbers in the proposal | **Yes** — Renee can't model without them |
| "900 Guides" vs ~650 in staffing data | Sizing | Workforce | Ask; label assumption | No, but label it |
| Is any customer disclosure required? | G4, G5 | Product / Legal | Ask | No |
| Why ineligible WN7 calls are long | G8 | Quality (call listening) | Ask Quality to tag in sample | No |

---

## Layer 3 — Candidate design targets (not decided)

| Target | Audience | Observable behavior | Closes | Format options (open) | Next week? |
|---|---|---|---|---|---|
| **T1** Act on the result | Guides | After a serial check: take the recovery path if Eligible, ordinary support if not — and stop the restart loop | G1, G8 | Decision practice with eligible / ineligible / pending cases (Imani's format, Rina's ask); in-call prompt | Yes (practice); screen detail pending |
| **T2** Close both transactions and explain Plus | Guides | Plus complete or follow-up opened; Plus described accurately; recap with confirmation number, shipping, Plus status | G2, G4, G7 | Short in-call reference; model calls (Sep 24 pending, Sep 16); wording from Nina Sep 21 + Specialist Sep 12 | Yes, except pending wording (draft for approval) |
| **T3** Recognize early, impact first | Guides | Hear impact → recognize pattern → get serial early (app, hub, or prior note) | G3, G5 | Ben's cue + Imani's reminder; one-sentence transition practice | Yes (cue); search fix runs in parallel |
| **T4** Calibrate Leads | Leads (18 GC + Specialist) | Leads recognize the same six behaviors, coach from a clip with a cue, listen to one call | G6 (and reinforces T1–T3) | Cue + de-identified clips (Elias offered) + one call listen (Priya's "smallest manager behavior"); optional short Sana readiness check | Yes |
| **T5** Partner asks (Learning drafts, others own) | Product Ops, Care Systems, Knowledge Ops, Quality, Workforce | Decisions made on pending Plus, screen reference, permissions, search terms, rubric, capacity | Dependencies | One-page owner list for Dana (her "what each would need to own") | Yes (the list itself) |

**Suggested priority** (for challenge):
1. **T1** — largest gap in the data, directly tied to handle time and satisfaction.
2. **T2** — strong evidence, recurs in both queues, causes callbacks.
3. **T4** — the mechanism that makes T1–T3 stick across centers; small, fits next week.
4. **T3** — real but partly owned by Knowledge Ops (search).
5. **T5** — in parallel from day one; it's what Dana asked for on Sep 30.

---

## Not targeting, and why

| Not targeting | Why |
|---|---|
| A standalone video as the main intervention | Can't support in-call decisions (G1 is the biggest gap); Guides asked for "what I click and what I say" (item 34). A short video could still demonstrate a model call. |
| A course, curriculum, or 40-slide module | Dana: nothing that "arrives in November"; Imani: "the incident will change before we finish"; Nola. |
| An all-Guide, all-shift assignment | Renee: "a different proposition… more unanswered calls"; Marisol needs a reason to believe first. |
| A manager course | Priya: "not… a substitute for giving them the right information." |
| Reducing call volume | Not a Learning lever; proactive notice (Comms) and routing (Orbit admin). |
| Desktop prompt / routing change | Systems change after an approved design (Cam Hall) — name as a later option. |
| Setting the documentation standard or QA rubric | Owned by Care Ops / Quality; Learning aligns to them. |
| Center-by-center intervention | Data doesn't show meaningful center differences. |
| Precise ROI or handle-time savings claims | Sample-based, selection effects, Elias: "promising," not causal. An illustrative range at most, labeled. |
