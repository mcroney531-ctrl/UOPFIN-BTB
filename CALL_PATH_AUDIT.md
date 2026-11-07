# Guide Call Path: PO-117 source audit

Nov 7. Checks every operational instruction in `TN-UOP-FIN/deliverables/wn7-guide-call-path.html` (and its PDF) against the case packet.

**Key sources**
- **PO-117**: `sources/care-desk-september-bulletin.md`, the Product Operations reference, effective Sep 12 (Specialist Care), "current as of September 24." It describes itself as "an operational reference, not a learning design."
- **BH-4419**: `sources/beacon-article-export.md`, v1, Sep 21. It links to PO-117 and the Orbit eligibility panel; its body uses `Eligible` / `Not eligible`.
- **Weekly update, Sep 21**: `sources/2026-09-21-care-weekly-update.md`. "PO-117 is now available through Beacon article BH-4419."
- **Product reference**: `sources/connected-home-products.md`.
- **Product/comms notes**: `sources/meetings/product-comms-notes.md` (demo, fulfillment, and a customer account systems note).

| Instruction in the Call Path | PO-117 explicit? | Other packet support | Still to validate before release |
|---|---|---|---|
| Orbit's `WN7 eligibility` panel | Yes ("Enter the serial in Orbit's `WN7 eligibility` panel") | BH-4419 "links to … the Orbit eligibility panel"; Sep 9 demo | Care Systems: where the result appears and General Care access (Sep 22: a Guide didn't know "which value on the screen counted"; Sep 24: possible permissions gap) |
| `Eligible` / `Not eligible` | Yes | BH-4419 body; demo "shows eligible or not eligible" | Same as above: how the values are displayed |
| Serial from the Northstar app or the hub | Yes ("in the Northstar app or on the hub") | Product reference: "Northstar Home app or on the bottom of the hub" | None. Note: the product reference supports Sofia's underside-of-hub tip, which we previously treated as unverified. The Call Path keeps the PO-117 wording. |
| Replacement order has a confirmation number | Yes ("Verify that the order has a confirmation number") | Product reference: the path "produces a confirmation number and shipping estimate" | None |
| Use the shipping estimate shown on the order | Yes ("subject to the estimate shown on the order") | Fulfillment: estimates "should come from the order flow rather than a memorized number" | None. PO-117 also states a 5–7 day standard; the Call Path deliberately leaves it out |
| Plus credit shows `Applied` | Yes ("Verify that the credit transaction says `Applied`") | Account systems note: separate status messages, and "an order confirmation can be available while the credit is pending" | Account Systems / Product Ops: the other status values and their meaning (see Gap 1) |
| Keep the recovery case open when unresolved | Yes ("If either transaction fails, keep the recovery case open") | Account systems note: "If either transaction fails, the case should remain open for follow-up" | See Gap 1 |
| Unresolved recovery queue | Yes ("arrange follow-up through the unresolved recovery queue") | None. The earlier account systems note "did not state a new queue" (it predates PO-117, so this isn't a contradiction) | Care Systems / Product Ops: that General Care can route to the queue |
| Eligibility review case when no serial / tool unavailable | Yes ("open an eligibility review case and give the customer a specific follow-up expectation. Do not guess.") | None | Product Ops: the follow-up expectation itself isn't defined anywhere (see Gap 2) |
| Don't ask for restart steps to qualify | Yes ("Do not ask an eligible customer to repeat generic restart steps as a condition for the approved remedy") | Product reference: Guides "should not repeatedly ask a verified eligible customer to retry generic troubleshooting"; Dana, Sep 10 | None |
| Plus is a goodwill benefit, not a repair | Yes ("It is a goodwill benefit, not a repair for the WN7 defect") | Sep 24 review flagged Plus described as "backup internet" | None |
| Not eligible: continue troubleshooting/escalation; no replacement or free year | Yes | BH-4419 body ("continue normal diagnosis") | None |
| Recap and check understanding | PO-117 step 5: "Invite the customer to repeat back any part that is unclear." | Northstar value "Make it clear": "a next step they can repeat back" | See Gap 3 |

## Gaps and conflicts (reported, not silently resolved)
1. **A pending credit isn't covered.** PO-117 and the account systems note only say what to do when a transaction *fails*. Both the account systems note and Guide feedback (Dev Sep 18; Guide E., Sep 22) describe a *pending* credit. PO-117 also says "A completed replacement order with a missing Plus credit is an incomplete recovery." The Call Path therefore treats anything other than `Applied` as not complete. Whether a pending credit also goes to the unresolved recovery queue is shown as a before-release dependency for Account Systems / Product Ops.
2. **No defined follow-up expectation.** PO-117 tells Guides to give "a specific follow-up expectation" but doesn't say what it is. The first draft wrongly said "give the follow-up expectation it specifies"; that's now corrected to "tell the customer what happens next," with a Product Ops dependency.
3. **Repeat-back wording.** At your request, the line now reads "Check that the customer understands the next step." PO-117 explicitly says "Invite the customer to repeat back any part that is unclear," which is a more specific technique. Not a contradiction, but the Call Path is now less specific than its source.
4. **Not documented anywhere:** the Call Path's "tell your Lead so it goes through the existing escalation channel" (when a Guide can't open the panel or order) and "use the established fallback" when a Lead is unavailable. Both reflect the approved design (Guide → Lead first), but the packet doesn't define the fallback.

No click paths, field locations, timings, prices or customer scripts are included.
