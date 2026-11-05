# Workbook pass — quantitative check on the qualitative story

Quick pass over `Orbit_operations.xlsx` and `Quality_and_feedback.xlsx` (case packet, `sources/data/`). Purpose: size the problem and test the discovery log's priorities, not produce a precise WN7 impact estimate. Analysis by [Claude] with pandas; script kept in the session scratchpad (not a deliverable).

**Phases used:** Apr–Jul baseline · Aug 1–30 · Aug 31–Sep 9 (issue known, no remedy) · Sep 10–20 (remedy approved, Specialist only) · Sep 21–30 (`BH-4419` live for General Care).

**Read every number with these limits**
- Daily operations and staffing are full populations. The call sample is a systematic 20,000-call sample (28 duplicate rows removed). QA and feedback are **deliberately nonrandom** (WN7-risk, long-call, and outreach oversamples) — patterns, not rates.
- "WN7-related" + "WNM-7-related" daily counts are answered contacts in WN7-containing product codes — a proxy, **not** an eligibility or incident count.
- "Eligible for recovery" is a retrospective analytic label; before Sep 10 Guides had no path to act on it.
- Last data day is Sep 30. Nothing after Dana's request is in the data.

---

## 1. How big is the problem? (General Care, daily means)

| Phase | Offered | Answered | AHT (min) | Wait (min) | Abandon | WN7-containing answered | Total handle min/day |
|---|---|---|---|---|---|---|---|
| Apr–Jul | 21,741 | 20,794 | 8.48 | 1.76 | 4% | 172 | 176,389 |
| Aug 1–30 | 22,047 | 21,241 | 8.54 | 1.60 | 4% | 175 | 181,315 |
| Aug 31–Sep 9 | 24,719 | 18,813 | 10.60 | 3.78 | 24% | 4,087 | 198,981 |
| Sep 10–20 | 27,082 | 18,979 | 11.11 | 4.43 | 30% | 5,286 | 210,862 |
| Sep 21–30 | 29,154 | 20,408 | 11.57 | 4.69 | 30% | 8,047 | 236,139 |

- **Abandonment went from ~4% to ~30%.** Offered contacts rose ~34%; answered contacts did not. That is the "queue feeling it."
- **WN7-containing contacts went from ~170/day to ~8,000/day — about 39% of answered General Care contacts in Sep 21–30**, and still rising after the article went live.
- Specialist Care shows the same shape on a smaller scale (abandonment ~3% → ~24%).

## 2. Is the AHT rise a WN7 problem? (call sample, General Care)

| Phase | Non-WN7 calls: n / AHT | WN7-product calls: n / AHT |
|---|---|---|
| Apr–Jul | 12,586 / 8.48 | 101 / 8.00 |
| Aug 31–Sep 9 | 824 / 8.51 | 220 / 18.52 |
| Sep 10–20 | 736 / 8.37 | 300 / 17.73 |
| Sep 21–30 | 600 / 8.60 | 379 / 16.18 |

- **Non-WN7 AHT is flat at ~8.5 minutes throughout.** WN7-product calls roughly doubled in length once the defect appeared.
- Sep 21–30 check: 39% × 16.2 + 61% × 8.6 ≈ 11.6 min — matches the full-population AHT of 11.57. **By this proxy, essentially all of the General Care AHT rise comes from the WN7 call mix**, and WN7-product calls are ~55% of General Care handle minutes.
- **Nuance for Marisol's "not every long call is WN7":** about half of WN7-product calls are *not* eligible, and they're long too (~16 min, vs. 8 before the incident). So "WN7" ≠ "eligible for recovery." Ineligible WN7 callers are part of the load, and the recovery path doesn't shorten them.
- Reason codes are broad categories (Connectivity, Setup, Billing…). WN7-product calls are mostly `Connectivity` (~88%); there is no `internet slow` code at this level, so the source claims about miscoding can't be tested here.

## 3. What happens on eligible calls? (call sample)

**Conversation path, eligible calls, Sep 21–30**

| | Complete recovery | Incomplete recovery | Generic troubleshooting | n |
|---|---|---|---|---|
| General Care | 76 (37%) | 13 (6%) | 115 (56%) | 204 |
| Specialist Care | 63 (82%) | 14 (18%) | 0 | 77 |

**AHT by path (eligible calls)**

| | Complete recovery | Incomplete recovery | Generic troubleshooting |
|---|---|---|---|
| General Care | 10.9 | 16.2 | 19.8 |
| Specialist Care | 10.1 | 16.4 | — |

- **Doing the recovery is the faster call.** Complete recovery runs ~11 minutes; generic troubleshooting on an eligible caller runs ~20. The difference is almost all talk time (7.3 vs. 15.7 min). Caveat: calls that completed may have been easier ones.
- **After the article went live, most eligible General Care calls still got generic troubleshooting (56%).**

**The sharpest finding — serial verified, then not acted on (General Care eligible, Sep 21–30):**

| | Complete | Incomplete | Generic troubleshooting | Total |
|---|---|---|---|---|
| Serial verified | 76 | 13 | **70** | 159 |
| Not verified | 0 | 0 | 45 | 45 |

- 78% of eligible calls had a serial check recorded. **But 70 of those 159 (44%) still ended in generic troubleshooting.** The gap is not only finding the article or remembering to check the serial — it's **acting on the result**. Consistent with: Guides who couldn't tell which Orbit value is the result (Sep 22), possible permission gaps (Sep 24), and no visible next step (Guide R., Sep 8). The data can't say which.
- 22% never verified the serial — the recognition/finding gap.
- Of eligible calls that started recovery, Plus was attached less often than the replacement (General Care: replacement 44%, Plus 37% of eligible; Specialist: replacement 100%, Plus ~84%). The **Plus completion gap shows up even in Specialist Care.**

**By center (General Care eligible, Sep 21–30; ~50 calls each):** complete recovery Columbus 34%, Phoenix 32%, Remote 40%, Tampa 43%. Differences are small at these sample sizes — **this data does not demonstrate center-level inconsistency**. The case for Lead alignment rests on the qualitative evidence, not on these numbers.

## 4. QA reviews (nonrandom — patterns only)

General Care, Sep 21–30 (158 reviews, mostly WN7-risk and long-call oversamples):
- Recognized recovery path: 86 of 158.
- Of reviews where replacement applied: replacement arranged 32 of 75; Plus attached 26 of 75.
- CLEAR "Act": does not meet 79, meets 60, partially 19. "Does not meet" rose sharply after the article went live — consistent with the listen-to-act pivot problem, but the review mix also changed.
- Specialist Care, Sep 10–30: mostly "meets" on CLEAR Act; Plus still missed in 11 of 79 applicable reviews.

## 5. Customer feedback (voluntary, WN7 outreach oversampled — patterns only)

| Eligible callers, by path | Responses | Mean satisfaction (1–5) |
|---|---|---|
| Complete recovery | 145 | 4.57 |
| Incomplete recovery | 25 | 2.04 |
| Generic troubleshooting | 224 | 1.44 |

- A very large difference in the direction the qualitative evidence predicts. It can't prove cause (respondents self-select), but it supports Marisol's "a recovery customers believe."
- Ineligible callers average ~3.5 regardless of path.

## 6. Staffing and the "900 Guides" figure

- General Care planned Guides rose from ~572/day (Apr–Jul) to 661 (Sep 21–30); actual from ~536 to ~610. Occupancy rose from ~0.76 to ~0.89. 31 date-and-queue rows are flagged "queue pressure," 10 of them with temporary extra shifts.
- The highest daily total across both queues is **714 planned / 656 actual** — not 900. Dana (Oct 1) and Renee (Sep 5, Sep 19) both say 900. The staffing sheet may count scheduled daily headcount rather than the roster. **Unreconciled — don't quote 900 or ~650 as a hard number without labeling the difference.**

## 7. Data quality notes

- 28 duplicate export rows (removed). Product code missing 0.8%, reason code 1.3%.
- 18 product codes in the sample are not in the catalog, including WN5/6/8/9 and WNM-5/6/8/9 — none affect the WN7/WNM-7 analysis.
- Four centers in the sample (Columbus, Phoenix, Remote, Tampa); Priya says "three centers" (Sep 21). Possibly Remote isn't counted as a center — unreconciled.

---

## What this changes in the discovery log

| Discovery claim | Workbook evidence | Effect |
|---|---|---|
| WN7 drives the queue problem (Dana, Renee) | Non-WN7 AHT flat; WN7 mix explains the AHT rise; ~39% of answered GC contacts | **Strengthened** — and quantified |
| "Don't call every long call WN7" (Marisol) | Half of WN7-product calls are ineligible and still ~16 min | **Refined** — WN7 ≠ eligible; ineligible WN7 calls are a separate load |
| Finding the article is the main barrier (items 18, 49) | 78% verified the serial; 44% of those still troubleshot | **Rebalanced** — *acting on the result* is at least as big as finding |
| Plus completion gap (Plus thread) | Plus attached less than replacement in both queues | **Strengthened** |
| Recovery takes longer (implicit worry) | Complete recovery ~11 min vs. generic ~20 | **Reversed** — doing it right is the faster call (selection caveat) |
| Uneven across centers (item 45) | Small, noisy differences | **Not supported by data**; rests on qualitative evidence |
| "900 Guides" (Dana, Renee) | Staffing tops out ~714 planned | **Unreconciled** |
