# Gap synthesis — draft for critical review

**Status: core targets locked (round 2, end of file). Layers 1–3 above are the working evidence behind them.** Built from [`DECISIONS.md`](DECISIONS.md), [`SYNTHESIS.md`](SYNTHESIS.md), and [`WORKBOOKS.md`](WORKBOOKS.md). Nothing here is decided.

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
| **G1** | **Serial check recorded, recovery path not carried out** | Of 204 eligible GC calls Sep 21–30, 159 had a serial check recorded; 70 of those 159 (44%) still ended in generic troubleshooting. A recorded check doesn't prove the Guide saw or understood an Eligible result [GPT] — where the decision broke is unknown; Sep 28 Elias "older restart steps before anyone checked the serial"; Sep 24 Guide couldn't locate result, transferred | **Strong** | Appropriate path selected · stop redundant troubleshooting | Can't tell which Orbit value is the result (Sep 22) · Orbit permissions (Sep 24) · no visible next step / what to say (Guide R., item 34) · perceived review pressure to keep troubleshooting (item 31) |
| **G2** | **Plus isn't completed or its status isn't closed out** | Plus attached less often than replacement in both queues (GC 37% vs 44% of eligible; Specialist ~84% vs 100%); Dev, Harper, Sep 21–24 calibrations | **Strong** | Plus complete or follow-up opened · clear recap | Two separate transactions (Sep 9) · pending status with no guidance (items 9, 59) · Guide assumes order number = done (Priya, Sep 17) |
| **G3** | **Pattern not recognized early / serial never checked** | 22% of eligible GC calls had no serial check (Sep 21–30, n=204); Elias's 4-Guide test (1 of 4 landed on old article); Sep 22 customer-language searches failed | **Strong** on the gap; **moderate** on the search cause | Recognition of the pattern · serial eligibility checked | Search ranking and missing customer language (items 11, 24, 61) · "intermittent" title · product not recognized from customer words (item 11) · article reached shifts unevenly (Sep 28) |
| **G4** | **Plus explained inaccurately** | Guide L. (Sep 13), Micah (Sep 18), Sep 24 call "backup internet while the replacement is on the way"; customer asks if it fixes the drops | **Moderate** (recurring across 11 days, different source types; no data field) | Clear recap · explain accurately | Word of mouth before official guidance (item 8) · Plus genuinely has backup features, easy to overstate (item 13) |
| **G5** | **Acknowledgment doesn't turn into action** (the "pivot") | Quality: Guides name CLEAR but don't move to action (item 15); QA CLEAR "Act" does not meet 79/158 GC Sep 21–30 (nonrandom); Imani's experiment — generic empathy first, better on 2nd try (item 54); Sienna's "useful pivot" | **Moderate** (direct Quality observation + nonrandom QA) | Recognition · appropriate path (conversation side) | Newer Guides fear sounding cold (item 34) · reading every qualifier (item 40) · no clear next action to pivot *to* (overlaps G1) |
| **G6** | **Leads not equipped or aligned to coach the recovery** | Priya "not told Leads what to coach" (Sep 18); launch relied on Leads with no briefing (Sep 28); 2 of 18 Leads with planned huddles on launch day (Sep 21); Leads' own requests (cue, clip, pending answer); 15/18 completed generic CLEAR refresher, nothing WN7-specific tracked | **Moderate** (direct, multiple stakeholders; self-report; **center data does not show variation**) | All six fields (consistency of coaching and feedback) | No coaching cue or examples (items 18, 55) · Lead time and coverage load (items 46, 56) · no stable tool to coach to (item 38) |
| **G7** | **Next contact can't see what was done** | Dev's callback, Sep 20 four-call customer, Sep 22 serial in prior note, Sep 24 managers on sparse notes | **Moderate** (four instances, two source types; no data field) | Continuity across contacts (not in six fields) | No documentation standard (item 53) |
| **G8** | **Ineligible WN7 calls are long too** | Ineligible WN7-product GC calls ~16 min vs 8 pre-incident (data); Rina, Sofia, Priya on ineligible cases | **Moderate** — length is strong data; cause **unknown** | Appropriate path selected (ordinary path) | Real connectivity problems that take time · Guides unsure whether to stop troubleshooting · customers expecting a replacement after hearing about it |

**Context gap, not a Guide behavior:** Volume. WN7-containing contacts (a product-code proxy, not a defect incidence rate) rose to ~39% of answered GC contacts and kept rising after Sep 21. Learning can shorten eligible calls (complete recovery ~11 min vs ~20 generic) but cannot reduce volume; the proactive notice may change volume again (Jules, Oct 1).

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

## Layer 3 — Candidate design targets (not decided; revised in round 1)

**Separate two questions [GPT]:**
- **What behavior most needs to change?** Guides consistently interpret the eligibility result and carry out the appropriate path — recovery with both transactions (or documented follow-up), or ordinary support — and explain it accurately.
- **What enables that change at scale?** Verified operational guidance, Lead calibration, in-call support, targeted practice, and Quality feedback.

### One end-to-end Guide target [GPT; replaces T1–T3]
Recognize the pattern → verify eligibility → choose the path → complete the applicable actions → explain and document the outcome.
- Closes G1–G5, G7, G8. T1–T3 from the first draft stay as **diagnostic lenses** for where a call breaks, not separate targets.
- Practice covers the whole call, including **ineligible** and **pending-Plus** cases, so eligible recovery isn't optimized into "every WN7 is a replacement" [GPT; Sofia, Rina, Priya].

### Enabling components (rollout sequence, not problem ranking)

| Order | Component | Audience | Observable outcome | Format options (open) | Next week? |
|---|---|---|---|---|---|
| 1 (parallel) | **Operational readiness** — partner asks | Product Ops, Care Systems, Knowledge Ops, Quality, Workforce | Owners named for pending Plus, screen reference, permissions, search terms, rubric, capacity | One-page owner list for Dana (her "what each would need to own"); Learning drafts, partners approve | Yes (the list) |
| 2 | **Lead calibration** | Leads (18 GC + Specialist) | Leads recognize the same decisions and coach from a clip with a cue | Common performance model + de-identified clips (Elias offered) + cue + one call listen (Priya's "smallest manager behavior"); optional short Sana readiness check | Yes |
| 3 | **Guide practice + in-call support** | Guides | The end-to-end target above | Full-call decision practice (Imani's format); concise in-call reference; model calls (Sep 16, Sep 24 pending, Sep 24 ineligible) | Yes, except pending wording (draft for approval) and exact screen |
| 4 | **Observe and refine** | Quality, Leads | Targeted call listening on the six draft fields, used for coaching and exceptions — **an observation framework, not a scoring rubric** (Priya, Elias, Sep 24) | Small pilot; outcomes beyond completion (repeat calls, complete recovery, handle time, queue impact) | Starts the following week |

**Priority vs. sequence [GPT]:** the eligibility-to-action behavior is the top *problem*; Lead calibration is the first *enablement* step. Not competing positions — this keeps the Lead-anchored approach grounded in the most consequential Guide behavior.

**Design question still open [GPT]:** how little can be built while still making this system work?

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

---

## Review round 1 — changes and checks

| Change | By | Basis |
|---|---|---|
| T1–T3 merged into one end-to-end Guide target; kept as diagnostic lenses | GPT | The Guide experiences one continuous call |
| Lead calibration moved first in *rollout*; eligibility-to-action stays top *problem* | GPT (supports your Lead-anchored position) | Priority ≠ sequence |
| Six fields framed as a draft observation framework, not a rubric | GPT | Sep 24 Priya and Elias |
| G1 reworded: "serial check recorded, recovery path not carried out" | GPT | A recorded check ≠ an understood result |
| 39% labeled a product-code proxy, not defect incidence | GPT | Data dictionary |
| Ineligible cases kept in practice explicitly | GPT | Half of WN7-product calls are ineligible |

**Checks run on GPT's challenges [Claude]:**
- **Denominators for 44%:** 204 eligible General Care calls (Sep 21–30) → 159 with a serial check recorded → 70 ended in generic troubleshooting. 45 had no check.
- **Is 11 vs. 20 minutes explained by something else?** The gap holds within every cut the data allows: serial-verified calls only (10.9 vs 19.8), WN7 vs WNM-7 (10.9 vs 19.8; 10.8 vs 20.0), each of the four centers (10.6–11.1 vs 19.6–20.0). Generic troubleshooting on eligible calls was ~19.8 min before the path existed too, and Specialist complete recoveries run ~10.1. **But the data has no measure of case complexity** (e.g., the account/address complications in Sep 13), so selection can't be ruled out. Supports the hypothesis; not causal; don't promise nine minutes saved per call. The data is also unusually uniform across cuts, which suggests synthetic precision — another reason to present ranges, not point estimates.
- **Three vs. four centers:** still unreconciled. The staffing sheet is by queue, not center, so the data can't settle it. Label in any rollout coverage claim.

---

## Review round 2 — core targets (LOCKED by you, Nov 5, 2026)

GPT reviewed `DECISIONS.md`, `SYNTHESIS.md`, and the revised `GAPS.md`: core performance model holds; uncertainties preserved.

**Proposed core targets [GPT]:**
1. One end-to-end Guide recovery behavior, practiced with eligible, ineligible, and pending cases.
2. A common Lead coaching and observation standard.
3. An in-call reference that helps Guides act without memorizing a speech.
4. Operational fixes assigned to their actual owners.
5. A small, capacity-conscious pilot evaluated on complete recovery and call behavior.

Unresolved questions stay explicit dependencies, not reasons to stall.

**Tightening [GPT], with sources added [Claude]:**
- **Failed action ≠ failed decision.** The 70 checked-but-troubleshot calls may be misinterpretation (Sep 22 screen value), tool unavailability (Sep 24 permissions), or deliberate choice (perceived review pressure, item 31). Lead coaching diagnoses first — Ben: "I need to know what the Guide heard and what they did next" (Sep 24).
- **Size the pilot; don't promise all Leads next week.** 18 General Care Leads plus Specialist; Workforce hasn't confirmed protected time. State group size and minutes per person (Renee, Sep 19, Oct 1); sample new hires and experienced Guides (item 57).
- **Define pilot success.** Correct path selected; transactions completed or follow-up opened; outcome explained. Operational checks: repeat calls, complete recovery, handle time, queue impact (Marisol, Oct 1) — checks, not guaranteed savings; "promising," not causal (Elias).
- **Practice format already exists:** Imani's two-call comparison → one-sentence transition → "what action does it unlock?" (item 54).

**Status:** locked by you. Proposed by GPT; tightening sourced by Claude. Changes from here are new decisions, logged as such.
