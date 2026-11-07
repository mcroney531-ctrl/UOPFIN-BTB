# Decision and discovery log — Northstar Home work sample

Discovery phase: reading the 75-file case packet, flagging evidence, and recording how thinking formed. Written up from a working session after the full chronology was read. Item numbers match the numbers used in that session.

**How to read an entry**

- **Source** — packet file (paths relative to `Northstar_Home_Case_Packet/sources/` unless noted) and timestamp or section date. Quotes are exact source wording unless marked as a note-taker's summary.
- **Attribution** — **[You]** = the candidate's own flag, read, or decision. **[GPT]** = ChatGPT, used as a separate thinking partner. **[Claude]** = Claude Code, this session. Where an idea was built jointly, each part is attributed.
- **Tags** — `finding` · `foundation` (existing material to build on) · `design idea` (not decided) · `position` (stated stance) · `dependency` (needs a non-Learning owner) · `risk` · `evaluation` · `open question` · `process` (how the work was done).
- **Status** — nothing here is a final design. "Design idea" and "possible use" mean considered, not chosen.

Companion file: [`SYNTHESIS.md`](SYNTHESIS.md) — threads, design tests, dependencies with owners, open questions, who did what, and corrections.

---

## Process decisions (before and during reading)

### 1. Built a case organizer — `process`
[You] Organized the 75 files for reference and categorization before analysis: timeline, evidence map, source index, workbook guide, HTML previews of the two workbooks. Interpretation is labeled separately from source claims ("Organizer note"). `tools/verify.py` checks links, confirms every original appears in the index, and confirms by SHA-256 that none of the 75 originals changed.
- Use for interviewer note: concrete example of directing the harness with a verification step.

### 2. Had Claude write an audio narrative of the case — `process`
[You] Listened to a narrative of the case background and progression while reading the files, to get a feel for the situation "as if in or adjacent to the meetings."
- Caution learned [Claude]: narrative wording differs from source wording in places (e.g., "The Specialist answers" vs. source "The Guide said"; "orders" vs. "arranged"). Quote sources, not the narrative.

### 22. Source triage — `process`
[You] Considered archiving low-value files rather than deleting.
- [Claude] The organizer already separates 25 routine check-in pairs (50 files) that never mention the WN7; a search for core terms (Beacon, Orbit, Plus, serial, eligibility, huddle, handle time) found nothing substantive in them. Recommended a watch list of six routine pairs that echo the case: survey choice order (affects how `Satisfaction score` is read — keep active), archive search results, invoice download, KB tag capitalization, Sana orientation, order status wording.
- [GPT] Distinguish "unnecessary" from "relevance not yet established"; don't archive on boredom; tier Core / Supporting / Reference; triage per source, not per theme. For the interviewer note: "triaging a large, uneven evidence set while preserving source traceability," not "fodder."
- Outcome [You]: superseded by the reader tool (item 23), where archive = hide, never delete. Two "routine" files later produced findings (items 24, 25).

### 23. Built a message reader for immersion — `process`
[You] Specified a minimal, mobile-friendly reader for the email/meeting exchanges: Active/Archive tabs, oldest-first chronological feed, original wording only, no AI tagging or analysis, archive never deletes, search across both. Personal utility, not a deliverable.
- [Claude] Built it: 90 exchanges (Dana's email, weekly update, 26 threads, 33 dated meeting files, 3 multi-date notes files split into 29 dated sections). Reference docs, data, brief, and organizer files excluded. Verified: text matches all 64 source files word for word; originals unchanged by checksum; Archive/Restore/reload/search tested in a headless browser at phone width.
- Iterations at your request: collapse/expand with names and initials; hosted as a private Claude artifact with archive state stored per account (local HTML on phone lost state); star + notes; navy styling; "Add quote to note" button because pasting into the artifact's note field didn't work.
- Your notes exported from the reader (35 annotations) were the input for items 54–63.

---

## Discovery log

### 3. Dana, Sep 5 — "a behavior we can change" — `finding` `open question → resolved`
**Source:** `meetings/2026-09-05-care-shift-review.md`, 08:52.
> "I can speak to Learning once we know whether there is a behavior we can change. We cannot afford a long curriculum that lands after the problem passes."
- [You] Flagged as likely close to how Dana will judge a proposal.
- Open question [GPT; also raised by Claude]: what changed between this and her Sep 29 video request — or did anything?
- Dana's statements in order [Claude]: Sep 5 behavior to change → Sep 6 usable shared language, no improvising (item 32) → Sep 10 exact search terms and stop points (item 5) → Sep 29 ≤5-minute video → Sep 30 recommendation "including what each would need to own" (item 20) → Oct 1 explains the video choice (item 63).
- **Resolved by item 63:** the short-video request was mainly a format choice driven by queue capacity ("I cannot pull 900 hourly Guides off phones for a long course"), not a change in diagnosis. She still needs "something practical for Team Leads next week."

### 4. Priya, Sep 10 — "not a new ritual" — `finding`
**Source:** `meetings/qa-team-notes.md`, Sep 10 Team Lead preparation call.
> "We need a pattern and an eligibility process, not a new ritual that slows every call."
- Context: Leads asked whether to coach Guides to ask every connectivity caller for a serial; Priya asked them to hold.
- [Claude] Keep the full quote — "that slows every call" ties the concern to handle time.

### 5. Dana, Sep 10 — ineligible offers and repeated restarts — `finding`
**Source:** `meetings/2026-09-10-product-care-sync.md`, 15:20.
> "We have more than 200 active product and bundle codes in the queue. Please give us the exact search terms and the points where a general Guide stops troubleshooting. I do not want them offering this to an ineligible customer. I also do not want them asking an eligible caller to repeat the same restart four times."
- [You] Hypothesis: need for a simple process followed consistently ("fidelity").
- [Claude] Two failures in opposite directions; any design must prevent both.
- [GPT] Fidelity in a complicated environment, not just simplicity. Search terms and stop points are needed *during* the call. Open question: **do Guides not know what to do, or is the right information too hard to find and apply in the moment?**
- [Claude] caution: at this point performance support was a possible direction, not a lean; look equally for evidence Guides don't know what to do.

### 6. Marisol, Sep 10 — customers know what's coming — `finding`
**Source:** `meetings/2026-09-10-product-care-sync.md`, 15:29.
> "Keep the pilot small enough that we can see what Guides actually do and what happens to the queue. A replacement is the right remedy, but our explanation of it matters. I want customers to know what is coming without needing to call back for the tracking number or the Plus credit."
- Works as the **definition of a complete call**: the customer leaves without needing to call back.
- Later evidence: Dev's callback (Sep 18), Harper's replacement-without-Plus callback (Sep 16), Sep 21 calibration call with no recap of credit timing.
- [You] Flagged twice — weight noted.

### 7. Sofia, Sep 13 — avoid automatic pattern matching — `finding`
**Source:** `meetings/care-observation-notes.md`, Sep 13 weekend shift (Sofia's daily log).
> "We need to avoid training a pattern match that turns every WN7 into an automatic replacement request."
- Context: a WN7 owner described slow streaming, not brief whole-home drops; normal troubleshooting was reasonable. Same entry: two Guides didn't recognize "the three-piece Wi-Fi thing" as WNM-7.
- [GPT] Label: "Conditional decision-making vs. automatic pattern matching." Recognition without discrimination.
- **Working hypothesis** [GPT phrasing; you lean toward it; not confirmed]: the performance problem may be less about memorizing what to say and more about knowing which action fits, when, and why.
- [GPT] Items 4–7 may be requirements of one workflow, not four training needs.
- [Claude] First point where you stated a lean — timestamp for "change in thinking."

### 8. Guide L., Sep 13 — what Plus does — `finding` (Plus thread)
**Source:** `meetings/care-observation-notes.md`, Sep 13.
> "I heard we are replacing the bad ones and giving them Plus. Is Plus the thing that keeps them online while the box ships?"
- [You] Filed under "communicating the conditions of the playing field to Guides."
- [Claude] Same misconception Nina marked inaccurate on Sep 6 ("Northstar Plus will keep you connected while your new hub arrives"). The liaison's reply didn't answer it. "I heard" = word of mouth.
- [GPT] Label: "Guide understanding of the offer and its purpose." One excerpt shows at least one confused Guide, not prevalence.
- **Design consideration** [your observation; GPT wording]: "Any proposed intervention should help Guides understand the recovery process well enough to explain and execute it accurately—not simply memorize its steps."

### 9. Unanswered operational questions about Plus — `dependency` (Plus thread)
**Source:** `meetings/care-observation-notes.md`, Sep 13 (observer note after the liaison reply): "The response did not state whether Plus was active before the replacement, how a customer could verify it, or what to do if one transaction failed."
- [You] Not for the solution itself; show thinking toward it, e.g., a "considerations" section.
- [GPT] Label: "Operational readiness and exception handling." Training can't clarify a process the organization hasn't clarified.
- **Sorting rule** [You]: not every finding becomes training. Sort into recommendation / dependency / risk / question for another owner.
- Partial answers [Claude]: Sep 9 (`product-comms-notes.md`): order confirmation can show while credit is pending; "If either transaction fails, the case should remain open for follow-up"; account systems lead "cannot represent automatic timing." Sep 24 call shows good practice for pending (item 50).
- **Still open:** what a Guide says when Plus is *pending* (not failed), and whether pending is normal.

### 10. Sep 17 Beacon drafting — `foundation`
**Source:** `meetings/product-comms-notes.md`, Sep 17.
- Draft sequence: hear the brief whole-home-drop pattern → acknowledge → identify model and serial → check eligibility → recovery path or resume standard troubleshooting. Quality: "Guides need to know what decision each check supports."
- Priya: call-out that order and credit are two actions. Mateo: include an ineligible example. Editor: title search favors exact terms; older high-traffic articles can outrank new ones.
- [GPT] Label: "Existing performance-support foundation." Readiness states: drafted → approved → published → accessible → usable. Risk of a competing source of truth.
- [Claude] Ladder placement: drafted Sep 17; published Sep 21; accessible partly (roundup only, no alert or briefing — Sep 28); usable doubtful (Sep 22 searches). Five general connectivity variations already existed.

### 11. Product identification — `finding` `design idea`
**Source:** `meetings/care-observation-notes.md`, Sep 13 (Sofia); `connected-home-products.md`; `care-desk-september-bulletin.md`.
- [You] Guides may need to recognize the product physically and by customer words ("three-piece thing"), not only by model number.
- [Claude] WNM-7 = WN7 hub + two satellite nodes. Bulletin: "Ask for the hub serial in the Northstar app or on the hub." `BH-4419` search terms contain no customer phrases.
- [GPT] Label: "Product identification through customer language and visual recognition." Recognition ≠ eligibility. Possible: images, everyday descriptions, a quick ID reference.
- Serial routes [Claude]: hub label (Sofia's "underside" is her suggestion, not in the bulletin), Northstar app (covers mounted units), prior case note (Sep 22). Check the case first; still verify (item 53).

### 12. Model Specialist call, Sep 16 — `foundation`
**Source:** `meetings/2026-09-16-qa-listening.md`, 11:04 (Elias).
> "That would make the hub hard to trust during your workday. I can check whether your unit is in the group we are replacing." … checked the serial, arranged the replacement, applied Plus, read back confirmation and shipping window; under ten minutes; 5/5.
- [GPT] Label: "Positive performance example / model call." Analyze for behaviors, don't copy as script.
- Caveats in same meeting: Harper 11:09 — quick call without Plus led to a callback, "Our dashboard would have looked good if we only watched handle time"; Malik 11:13 — pilot callers are transfers already recognized by another Guide, "We cannot say the temporary guide caused the better scores"; header: "should not be read as a controlled test."
- Mateo 11:18: "The strong calls use CLEAR without saying its name… The weak calls sound like a checklist read aloud." Offers two de-identified examples for a huddle.

### 13. What is Plus for? — `open question → answered in sources`
[You] Not a remedy — so what is its role beyond goodwill?
- Answered in `connected-home-products.md` (line 7): Plus normally $149/yr; network insights, device connection history, limited cellular backup during eligible broadband outages through a compatible hub; the replacement WN7 has the required backup hardware; "a goodwill benefit, not a fix for the intermittent disconnect defect. Do not promise that it prevents all future outages."
- Nina, Sep 21 (`2026-09-21-care-systems-sync.md`, 10:10): "Plus gives insights and limited backup coverage. It does not make the defective WN7 reliable. Do not call it a 'fix'…"
- Confirm your own read of these before using.

### 14. Micah and Dev, Sep 18 — Plus confusion with consequences — `finding` (Plus thread)
**Source:** `meetings/2026-09-18-shift-feedback.md`, 10:09 and 10:34.
- Micah: couldn't remember "subscription or just a discount"; said "We might have an offer"; customer asked if it would stop the disconnects; went on hold to ask a Lead. "That is the time on the call nobody sees when they say 'just use the script.'"
- Dev: order complete, Plus pending, ended call; customer called back; "the second Guide had to figure out what we had promised."
- [Claude] Customers share the misconception. Harper's Sep 16 call (Plus not attached) is the closest to "forgot."
- [GPT] Merged label: **"Plus offer clarity and execution."** Mechanism (plausible, not proven widespread): doesn't understand offer → can't explain → hold to ask Lead → longer call. "Instructions available vs. equipped to use them."

### 15. CLEAR — adapt, don't copy — `foundation` `hypothesis`
**Source:** `care-conversation-guide.md`; Mateo Sep 16 11:18.
- [You] Copy-pasting CLEAR won't work; adaptation where it fits, since Guides and Leads already know it.
- Source: CLEAR is "a conversational guide, not a script to recite in order… does not identify product-specific eligibility, remedies, or systems." Quality: "many Guides can name CLEAR but do not consistently move from acknowledgment to the right action." Refresher completion "is not evidence."
- [GPT] Label: "Contextual application of existing CLEAR framework." Reinforce through realistic WN7 examples and targeted practice. Don't force every WN7 requirement into a CLEAR step.
- Parked [GPT, not adopted]: eligibility/replacement/Plus under Explain and Act; Recap ↔ Marisol's callback concern.

### 16. Nola, Sep 18 — a small checklist in front of her — `finding`
**Source:** `meetings/2026-09-18-shift-feedback.md`, 10:38.
> "I like that CLEAR says to recap, but on this issue I need a small checklist in front of me. I want to read the confirmation number and the shipping expectation, then say whether Plus is active or when we will follow up. I do not need another 40-slide course."
- [Claude] Not in conflict with Mateo: a checklist *in front of* the Guide vs. one *read aloud*. Related: Guide S., Sep 8 (item 34).

### 17. Priya, Sep 18 — four problems — `finding`
**Source:** `meetings/2026-09-18-shift-feedback.md`, 10:44.
> "I hear a search problem, an eligibility problem, a conversation problem, and a completion problem. We have not told Leads what to coach, and we have not made the same article available to every shift. I will take the Beacon and access issues to Operations. Please do not copy this discussion into a general script without checking the approved offer."
- Facilitator: "self-reports and examples, not a prevalence estimate… Care Quality should compare with sampled calls."
- [Claude] The parts the narrative dropped carry weight: no coaching direction to Leads; access gap; Priya routes some issues to Operations herself.

### 18. The week after `BH-4419` went live — `finding`
**Sources:** `meetings/qa-team-notes.md` Sep 21 calibration and Sep 22 manager pulse; `meetings/care-observation-notes.md` Sep 20 and Sep 22.
- Some Guides used the article and still missed the Plus credit or the recap. Article doesn't show where the eligibility result appears in Orbit. Customer phrases ("internet keeps blinking," "wifi cuts out") returned older articles. A Guide asked why the title says "intermittent."
- Malik: keep an "article discoverability" tag — "It is not all a training failure."
- Lead pulse (12 replies of 18 General Care Leads): 7 shared article, 4 ran or planned a huddle, 3 used a call example; harder to track than a Sana module. Requests: one-page coaching cue, one strong and one weak excerpt, a clear answer for pending Plus, a way to tell whether the Guide used the serial screen. Site 2 Lead: "Give me an example of what 'good' sounds like, then the specific checks."
- Guide K. (Sep 20): "They are mad because they have been through the steps with two different people. Show me how to tell them what changes on this call." Guide T.: fine with five minutes "if it is really five minutes and includes the screen I need."
- [GPT] Label: "Post-publication Beacon effectiveness and remaining performance barriers" — discoverability, usability, terminology, execution, adoption.
- [Claude] The counts may overlap — separate activity counts, not a funnel.

### 19. Huddle as an opening point — `design idea` [You]
[You] A huddle where Leads get clear on signals to watch for and pass the situation to Guides; Guides leave with *something* (undefined).
- Evidence for: Imani's 9-minute huddle (Sep 17); Mateo's examples; Leads' requests for cue and excerpts; CLEAR's huddle history.
- Constraints: coverage (a shift missed it), ~10 minutes of Lead time, no after-shift time, tracking difficulty, phone capacity.
- [You] Several constraints actually show Leads need equipping first. [Claude] Others (coverage, time, capacity) remain real limits.
- [GPT] Label: "Lead-led alignment huddle + in-call performance support." GPT filled the "something" as an in-call reference. The huddle may be the delivery mechanism, not the intervention. Risk: repeating incomplete instructions.

### 20. Elias, Sep 30 — "what would be different on a call" — `evaluation` (pinned)
**Source:** `meetings/qa-team-notes.md`, Sep 30 leadership review preparation.
- Elias asked Learning to say what would be different on a call if the recommendation worked; a completion count would not answer it. "We can learn whether a response is promising. We should not pretend a small operational pilot identifies a single causal ingredient."
- **Dana's margin comment:** "Good. Make it usable next week. I need a recommendation I can discuss with Priya, Mateo, Renee, and Elias, including what each would need to own."
- [GPT] Label: "Success criteria — What changes on the next call?" Completion metric vs. performance metric.
- **Design test:** *If this works, what will a Guide actually do differently?*

### 21. Start from what Leads need — `process` `hypothesis` [You]
[You] Working out what Leads need to coach will also define what Guides need.
- [GPT] Relabeled "Emerging design hypothesis — Lead-first discovery and alignment"; two levels (Leads: look for / reinforce / correct / escalate; Guides: recognize / decide / communicate / complete). [Claude] kept your framing as primary: an analysis approach, not a design commitment.
- Pushback [GPT and Claude]: cross-check against what Guides said directly (Guide S., Nola, Guide T., Guide K., Micah).

### 24. Jul 20 archive search — parallel from a routine file — `finding`
**Source:** `meetings/2026-07-20-archive-search-notes.md`.
- Older SB-11 articles outrank the new guide; they're still correct for the first hardware revision, so deleting them would create another problem. Fix: banner on old, clearer title on new. **Next step: "Search will be checked using both the product code and the common customer phrase."**
- [You] Not 1:1, but echoes the Beacon trouble.
- [GPT] Label: "Knowledge-base discoverability and contextual accuracy." Fix aimed at the information environment, not retraining. Knowledge Operations already handles this class of problem.
- [Claude] `BH-2240` remains correct for ineligible/non-defect cases too. Northstar's routine process already tests customer phrases.

### 25. Sana already has checklists — `finding`
**Source:** `meetings/2026-08-05-sana-orientation-notes.md` + Aug 6 follow-up.
- [Claude] Correction to the first read: it's a **new-hire onboarding checklist** owned by Learning Operations that tracks completion — not an in-call checklist. Shows Sana can host checklists and track completion; Guide T. (Sep 20) sees Sana as separate from the call.

### 26. Sana track for Leads — `design idea` (shortlisted) [You]
[You] Leads complete something short in Sana to get aligned before support reaches Guides — readiness, not box-ticking, and Lead time isn't in the Guide off-phone calculation.
- [GPT] "Sana-based Lead readiness, followed by Guide-facing support." Preparation (reviewed?) → readiness (can identify what to coach?) → impact (Guides doing it on calls — needs call evidence). Design Lead and Guide support around the same behaviors in parallel; Lead track deploys first.
- Checks [Claude]: Lead time is limited; whether Leads count toward coverage is not stated in the packet (label as assumption); Leads said huddles were *harder to track than* a Sana module — a comparison, not a request; "Beacon for in-call" is an assumption given item 18.
- Tempered by item 56 (Priya: smallest manager behavior; not a manager course).

### 27. Leila, Aug 31 — serial verification first — `finding` (hard limit)
**Source:** `meetings/2026-08-31-product-weekly.md`, 09:03.
> "We need serial verification before we tell anyone they qualify for a hardware action."
- Same line: many WN7 contacts coded "internet slow" or "setup" because Guides had no separate code → **data-quality warning** for Orbit trends.
- [Claude, corrected by GPT] Leaders stated the rule consistently from Aug 31; whether Guides understood it equally well is not established.

### 28. Elias, Aug 31 — which serials, what to verify, what to say — `finding`
**Source:** `meetings/2026-08-31-product-weekly.md`, 09:10.
> "…Generic troubleshooting makes sense on an ordinary router call, but it is making these customers repeat steps they already tried. If Product decides on a replacement path, tell us exactly which serials, what the Guide verifies, and what to say before the customer gives up. The existing Beacon article still sends them through restart and placement checks."
- [GPT] Leila sets the boundary; Elias names what makes it workable. Thread: requirements identified early vs. put into practice later.

### 29. Nina, Aug 31 — bundle code to hub serial — `finding`
**Source:** `meetings/2026-08-31-product-weekly.md`, 09:13 (speaker is Nina Hale).
> "…do not use model alone. An unaffected WN7 does not qualify… A few retailers bundled the WN7 as WNM-7. The bundle code needs to map to the hub serial."
- [GPT] Label: "Retail bundle aliases and serial mapping." Chain: customer's identifier → correct hub → its serial → verified eligibility.
- Instruction exists (bulletin: WN7 hub or WNM-7 bundle, ask for hub serial; `WNM-7` is a search term). Whether Orbit maps bundle → serial automatically: not established. Check how WNM-7 calls appear in the Orbit data (`DATA_DICTIONARY.md`).

### 30. Amara, Sep 2 — two paths — `finding`
**Source:** `meetings/product-comms-notes.md`, Sep 2.
> "We should not make a customer perform diagnosis for us. If Care can check the serial and the observed pattern aligns, use the recovery path. If it does not align or is ineligible, Care should have the ordinary support path available. We need both to be true."
- [GPT] Label: "Two-path decision model." Success includes everyone else getting appropriate support. Practice should include qualifying and non-qualifying cases. A reference must answer "what do I do when recovery isn't appropriate?"
- [Claude] Documented in `BH-4419` ("continue normal diagnosis for `Not eligible` or another cause"). Same Sep 2 entry: Nina said customer language could go into search terms "after the path was ready" — still open on the Sep 24 board.

### 31. Guide M., Sep 5 — why the restart happens — `finding`
**Source:** `meetings/care-observation-notes.md`, Sep 5.
> "If a customer says the whole house went down and then it came back, I do not know if that is their modem, the weather, or the WN7. I ask them to reboot because I need somewhere to start. If I skip it and it is a normal connection issue, I get asked why I did not use the basic steps."
- [You] "Just skip the restart if it seems like WN7" isn't the answer; forcing it universally isn't either.
- [Claude] The stated problem is *repeated* restarts, especially after verified eligibility (`connected-home-products.md`: don't "repeatedly ask a verified eligible customer to retry generic troubleshooting").
- [GPT] Label: "Diagnostic uncertainty and accountability pressure." Question: what evidence justifies moving past basic troubleshooting, and will Leads back that decision?
- Corrections [GPT, accepted]: (1) a restart need not precede the serial check — sources favor checking the serial early (Sep 16, Sep 17, Mateo "ask for the serial once"); (2) Guide M. describes *perceived* review pressure, not proof the scoring penalizes exceptions.
- Related: Priya (same entry) "Do not characterize this as refusal or lack of effort"; Theo (Aug 31) a restart "may coincide with recovery."

### 32. Sep 6 — two communication jobs — `finding`
**Source:** `meetings/product-comms-notes.md`, Sep 6.
- Jules: "We have two communication jobs. The first is helping a customer who has already reached Care understand the next step. The second is a proactive notice to affected households."
- Dana: "Care needs the first job in usable language. We cannot wait for the final outbound message to help someone on the phone, but we also cannot have every Guide create their own version."
- Wording limits from the same entry: "recall" removed; "limited number" to Legal; Plus "keep you connected" marked inaccurate; "replacement program" internal only.
- [GPT] Decision support (which path?) vs. conversation support (how to explain it?). Possible source for the learner-facing sample.

### 33. Sep 6 Quality form review — `evaluation`
**Source:** `meetings/qa-team-notes.md`, Sep 6.
- Elias: "followed process" can conceal two very different conversations. Sampling can't establish a full rate; a focused sample is to "see patterns and improve the response, not to create a precise performance ranking."
- Sienna: "We sometimes code empathy high when a Guide has stayed warm for 20 minutes… I want to listen for a concrete acknowledgment and a useful pivot. I do not need a perfect sentence."
- Malik: "We should not make the new fields a compliance trap. A Guide with an ineligible unit may do normal troubleshooting well. We need the sample notes to say what pattern was present and what the serial result was."

### 34. Guides R. and S., Sep 8 — "what I click and what I say" — `finding` (starred)
**Source:** `meetings/care-observation-notes.md`, Sep 8 Team Lead office hours.
- Guide R.: "I can say, 'That sounds frustrating,' all day. The hard part is when they say they already did the unplugging… I would rather have a few words that get me to the next action."
- Guide S.: "Please do not make a video with actors talking about empathy. I will watch it if I have to, but I need to know what I click and what I say when the customer asks whether we are replacing it."
- Same entry: Imani's strongest Guides "hear the impact, then they get the one detail that moves the case"; newer Guides fear a short acknowledgment "will sound cold"; "too much information by chat," no one named to publish a single source of truth; 17 of 29 invited Leads attended.
- [GPT] Click (navigate, verify, act) vs. say (explain, set expectations). **Design test:** *Can a Guide use this to determine the next action and explain it accurately while a customer is waiting?*
- [Claude] Guide S. rejects actors-on-empathy, not video as a format; strong evidence about content, weaker about format.

### 35. Position: a video alone won't do it — `position` [You]
[You] "A video alone won't do it. Still not ruling it out as an additional support resource."
- [GPT] Separate the need Dana identified from the solution she suggested.
- Support [Claude]: in-call needs (item 34); non-training causes (items 9, 18, 24); completion ≠ effect (item 20); Dana's own email asks for "your best take on what Learning can put in supervisors' hands quickly." Respect her real constraints: speed, supervisors, early next week.

### 36. Imani — purpose of a question; the "why" principle — `finding` `position`
**Source:** `meetings/care-observation-notes.md`, Sep 8.
- [You] Supports behavior change, not a 1-2-3 procedure. **Principle [You]: whatever the format, Guides need to understand the "why" behind each step.**
- [GPT] Strong Guides ask more purposeful questions, not just fewer. Practice: decide what information is needed next and why. Support: make the purpose of each check visible.
- Correction [GPT, accepted]: Claude split the call into judgment-early / checklist-late; judgment runs throughout. Checklists support judgment in every phase.
- Evaluation [GPT]: did the Guide get the information needed to make and explain the right decision without unnecessary repetition?

### 37. Ben Cruz's recognition cue, Sep 10 — `foundation`
**Source:** `meetings/qa-team-notes.md`, Sep 10 Team Lead preparation call.
- Cue: "whole home, brief drop, returns on its own, then model and serial." Imani: listen for the impact first. "The group did not approve exact wording for callers."
- [GPT] Label: "Stakeholder-generated recognition cue; pair with impact-first listening; wording not approved for customer use." Recognition ≠ eligibility; cue ≠ script; suggested ≠ approved. Don't let it become the whole solution.
- [Claude] Leads were still asking for a one-page cue on Sep 22.

### 38. Sofia, Sep 10 — a huddle needs a stable answer — `dependency`
**Source:** `meetings/qa-team-notes.md`, Sep 10 (closing note).
> "A huddle is useful when the answer is stable. I do not want to rehearse a recovery offer until we can show people the actual article and Orbit steps. Otherwise I am teaching confidence without a tool."
- [You] Doesn't rule out a huddle; shows what makes it useful.
- [GPT] "Implementation dependency — Stabilize the workflow before coaching it." "A huddle can reinforce a working process; it cannot substitute for one."
- Status [Claude]: article met (Sep 21, hard to find); Orbit steps not met (Sep 22 screenshot gap; Sep 24 board still "Decide whether…").
- Same entry, tracker: "Of 18 General Care Team Leads, 15 had completed the generic CLEAR refresher… The tracker did not measure whether a Lead had observed a WN7 call or practiced a coaching conversation."

### 39. Specialist wording, Sep 12 — `foundation` (starred)
**Source:** `meetings/product-comms-notes.md`, Sep 12 (Nina's observation).
> "We found an issue with some units, and I can check whether yours is included." Then replacement as the action Northstar can take; Plus as a separate goodwill credit.
- [GPT] Label: "Positive performance example — Calibrated language, eligibility verification, remedy vs. goodwill." Principle: say what you know, explain what you're checking, don't promise what isn't verified. Possible exercise: why is this better than announcing a replacement?
- [Claude] That principle is CLEAR's own Explain step. Consistent with Sep 16 model call, Leila Sep 23, bulletin "Do not say every WN7 is affected." Observed practice, not approved script.

### 40. Harper Lee, Sep 12 — not legal copy — `finding`
**Source:** `meetings/product-comms-notes.md`, Sep 12.
> "The temporary guide has the steps, but some people read every qualifier to the customer. I do not want a Guide to sound like legal copy. The customer needs the practical answer, then the detail that matters to their case."
- [GPT] Label: "Communication judgment — Translate accurate guidance into relevant customer-facing language." Internal guidance (complete) vs. customer-facing words (relevant).
- [Claude] A written guide alone produced the read-aloud problem; a job aid may need to separate *what the Guide checks* from *what the Guide says*. Inference (not in source): many wording cautions may push Guides to over-hedge.
- Open question: is any customer disclosure *required*? Sources show prohibitions, not required statements.

### 41. Sep 13 Specialist calibration — `finding` (positive evidence)
**Source:** `meetings/qa-team-notes.md`, Sep 13.
- Nine calls: 5 early serial check → recovery; 2 account/address complications; 1 replacement without Plus; 1 ineligible → standard support. Strong calls "did not sound identical"; in both, no repeated restarts after a verified eligible result.
- [You] Connective tissue: serial eligibility confirmed → proceed.
- **Harper:** "I have people asking me for a script. I keep saying it is a sequence, not a speech. The sequence matters because the customer needs both transactions and a recap. The words can change with the customer."
- [GPT] "Consistent decision-making, flexible communication." [Claude] Full sequence: verify serial → confirm path → stop redundant troubleshooting → complete both transactions → recap.
- Elias caveat: selected calls, transfers; don't compare directly with General Care.

### 42. Sep 15 General Care calibration — `evaluation`
**Source:** `meetings/care-observation-notes.md`, Sep 15.
- Reviewers split ("followed process" vs. "missed escalation") on a Guide who suspected the incident but had no visible recovery process; no WN7 recognition field. 6 of 18 selected calls coded `setup`/`internet slow` despite multi-device drops.
- [You] Be explicit about eligibility in more than one way: the Guide records it and confirms it with the customer.
- [GPT] "QA alignment — Recognition, verification, and appropriate action need distinct observable criteria." Suspected ≠ verified.
- Ben (same entry): "I can coach to that if I have something I can hear… A Guide can get a decent score while making the customer restart a verified eligible unit again."

### 43. Malik, Sep 15 — behavior vs. availability — `evaluation` (starred)
> "We need to separate behavior from availability. Before the path exists, it is unfair to score a Guide down for failing to complete an offer. Once the path is live, the important questions will be: did they recognize the pattern, check eligibility, complete both transactions, and explain what happens next?"
- [GPT] "Evaluation foundation — Four observable behaviors, conditional on operational readiness." Train and evaluate against the same standard.
- [Claude] Add "stop redundant troubleshooting" (Elias) and the ordinary-support path (Malik, Sep 6). The rise in handle time before Sep 21 happened when General Care had no path — affects how the problem is described to Dana.
- [GPT, accepted] Sep 21 is not a line after which everyone is accountable; search, familiarity, permissions, pending-Plus gaps persist.

### 44. Elias, Sep 16, 11:22 — `evaluation`
> "Quality's form needs a field for recognition and a field for complete recovery. 'Used empathy' is too vague. We need to know whether the Guide verified eligibility, stopped the redundant restart loop, and closed both transactions. I will propose a short temporary sampling rubric this week."

### 45. Lead-anchored approach — `position` [You] (strengthened)
[You] Guides can't carry out a policy their leadership hasn't directed them on; Leads give feedback and can't without knowing what to look for; feedback must be consistent across centers; starting from Leads builds the structure for what to bring to Guides and what Leads reinforce. "First" isn't quite the word.
- [Claude] Strongest evidence: the release already relied on Leads without equipping them (Sep 28: "Product Operations expected Team Leads to pass along the update through their usual channels"; no alert, no briefing, no record of which shifts discussed it). Plus Priya Sep 18, Ben Sep 15, uneven sites and shifts, no single source of truth.
- [GPT] Reframe: building the conditions for consistent Guide performance; Leads are part of the performance system. Three layers (GPT's structure, not adopted): **Foundation** (operational alignment) → **Reinforcement** (Lead calibration) → **Execution** (Guide enablement). Not a gate — Guide support develops in parallel. Alignment ≠ uniformity.
- [GPT] framing: "The goal isn't to get every Guide to complete the same training. It's to make sure every Guide operates under the same expectations, receives consistent reinforcement, and has the tools to make the right decision." Also: "Before expecting consistent Guide performance, establish consistent expectations among the people responsible for supporting and evaluating it."
- [Claude] The three layers map to Dana's "what each would need to own."
- Limits: Leads can pass on only what's settled (item 38); coaching doesn't cover the live call (item 34); QA must use the same standard (items 42, 52); Lead time and Dana's timeline.
- Sized by item 56.

### 46. Renee, Sep 19 — complete recovery vs. queue impact — `evaluation` (starred)
**Source:** `meetings/qa-team-notes.md`, Sep 19 (note-taker's summary of Renee's position, not her exact words).
> "She asked that a test avoid measuring only attendance or only handle time. The relevant operational question is whether a change improves a complete customer recovery without unacceptable queue impact."
- [GPT] "Evaluation principle — Complete recovery balanced against operational capacity." Don't invent a number for "unacceptable" — Workforce defines it.
- Same entry: a small staggered test is schedulable outside the busiest period "if the group size and duration were specific"; Lead spans and admin load are uneven; Workforce can protect time for a short pilot but not promise a standing reduction in manager workload.
- Imani (Sep 18): eligible, ineligible, failed-credit calls "sounded nothing alike after the first minute. Our huddle example happened to be the easy one."

### 47. The Orbit eligibility tool — live, not yet usable — `dependency`
Timeline [Claude]: Aug 31 planned ("recovery tool") → Sep 9 demonstrated ("eligible or not eligible"; meeting "did not decide whether the screen should be included in a Beacon image or whether all Guides had the same existing familiarity") → Sep 10 exists, instructions to be published → Sep 20 article can link to it → Sep 21 `BH-4419` links to the panel → Sep 22 a Guide with limited recent Orbit experience can't tell which value is the result → Sep 24 bulletin names "Orbit's `WN7 eligibility` panel"; board still "Decide whether to provide an Orbit screen reference."
- [GPT] "Operational dependency — Orbit eligibility-result identification and findability." "The tool being live is not the same as the tool being usable." Owners: Product Ops/Knowledge Ops (screen reference), Learning (meaning and action), Leads/QA (correct use).
- [You] LC-63 shows Care articles can carry images. [Claude] Feasible; a Beacon image of the Orbit screen was considered Sep 9. [GPT] Feasible ≠ approved; reason it stayed open unknown.
- Learner-facing limit: name the `WN7 eligibility` panel; don't invent click paths.
- Sep 24: reviewers couldn't tell whether a Guide lacked Orbit **permissions** or didn't know the screen — confirm access.
- [GPT, accepted] Varying names for the tool are not themselves evidence of a source-of-truth failure.

### 48. Quality's five temporary fields, Sep 20 — `foundation` `evaluation`
**Source:** `meetings/product-comms-notes.md`, Sep 20: serial verified, eligibility response followed, replacement action complete, Plus credit action complete, recap.
- [GPT] "Design and evaluation foundation." One standard for Guides, Leads, QA. Needs conditional scoring. Core plus targeted observation. "Help Northstar operationalize criteria its own Quality team identified."
- Superseded by item 52.

### 49. `BH-4419` release note and launch-day comments, Sep 21 — `foundation` (starred quote)
**Source:** `meetings/2026-09-21-care-systems-sync.md`.
- Release note: serial first; links to Orbit result and to the separate replacement and Plus transactions; "not a replacement for normal troubleshooting on an ineligible hub."
- [You] Base material — basically "it," with tweaks; the job is getting Guides and Leads on the same page.
- **Priya, 09:33:** "That is a roundup, and we have no shift plan or coaching cue. I have 18 Leads and three centers. Two have planned huddles; I do not know what the others will do. A targeted short note may work as a bridge, but we need a way to see who can actually handle a call."
- Elias, 09:18: four-Guide test, one landed on the old page via `internet slow`; "Please do not count the release as proof that every Guide knows the path."
- Tweaks the evidence calls for: customer-language search terms; "intermittent" title; Orbit screen reference; pending-Plus guidance; ineligible example.
- [GPT] Chain: verified operational guidance → consistent Lead expectations → usable Guide support → observed call performance. "Less new content than better activation."
- Corrections: [GPT] Northstar has the core policy and transaction information, not "all the right content." [Claude] the search terms do *not* include customer language.

### 50. Sep 24 — targeted listening and focused Quality check — `finding` `foundation`
**Sources:** `meetings/care-observation-notes.md` and `meetings/qa-team-notes.md`, Sep 24.
- Five General Care calls: (1) Plus didn't apply → Guide "would stay with the handoff, opened the approved follow-up, and explained that the case remained open until the credit was resolved. The caller said that was clear" — **model for pending/failed Plus**; (2) eight minutes of generic troubleshooting before finding the article; Plus described as "backup internet while the replacement is on the way" — flagged incomplete; (3) recognized the pattern but couldn't locate the serial result — permissions or screen unknown; transferred; (4) ineligible WN7, different symptom, normal troubleshooting, clear recap — Priya: "the case we must keep in the practice set so people do not turn a product name into a promise."
- **Imani:** "There are at least two jobs here. Guides need a concise way to recognize and explain the recovery path. Leads need a tiny cue for what to listen for, plus enough protected time to use it. If we only send a link, I will get uneven uptake. If we build a large course, the incident will change before we finish."
- Amina: "Please do not count a huddle attendance list as the outcome… Give us a small check that looks like the call." Ben: "I can coach from a real call better than a generic reminder."
- A Quality reviewer: "the job aid could remind Guides to capture the confirmation number, transaction status, and follow-up" — first appearance of "job aid" in the case.

### 51. Sienna, Sep 21 — find, use, close the loop — `finding` (core problem statement, starred)
**Source:** `meetings/qa-team-notes.md`, Sep 21.
> "The article release changed what was possible, but it did not make the behavior automatic. We are seeing a difference between finding the content, using it in the right moment, and closing the loop."
- [GPT] "Core problem statement — Content availability ≠ consistent execution ≠ complete recovery." **Design test:** *Which of these gaps does this component actually close?* Not one resource per stage.
- [GPT, accepted] Stages aren't purely Learning problems; each has a Learning part and an operational part.
- [GPT] central argument: "Northstar doesn't primarily need another explanation of the WN7 recovery policy. It needs to turn an existing recovery process into reliable, observable performance across three centers." [Claude] Plus is the exception that still needs explaining (Sep 24 misdescription).

### 52. Quality's six draft focused fields, Sep 24 — `foundation` (core performance standard, draft)
**Source:** `meetings/qa-team-notes.md`, Sep 24.
> recognition of the pattern, serial eligibility checked, appropriate path selected, replacement transaction complete when eligible, Plus credit complete or follow-up opened, and clear recap.
- [You] The core procedure; the job is creating conditions for Guides to do it smoothly and for Guides and Leads to align on it.
- Resolves earlier gaps: recognition added; "appropriate path selected" covers the ordinary path; conditional scoring built in.
- Priya asked whether it could support coaching "without becoming a new performance score"; Elias: first use is "targeted feedback and learning from exceptions" → [GPT] **developmental pilot, not a compliance metric**.
- [GPT] maps to Sienna's stages; Guides practice with the article open, Leads calibrate on eligible/ineligible/incomplete examples, Quality separates Guide error from system failure.
- Not explicit in the six: stopping the redundant restart loop; conversation quality beyond "clear recap." [Claude] "Locate the guidance" in GPT's mapping is GPT's addition. **Still a draft** — confirm adoption.

### 53. Continuity across contacts — `finding` `design idea`
- Instances: Dev's callback (Sep 18, second Guide "had to figure out what we had promised"); customer called four times with incomplete notes (Sep 20); serial in a prior note, unsure whether to re-ask (Sep 22); sparse notes raised by managers (Sep 24).
- [GPT] Quality's fields judge *this* call; recovery can span several. Recap and notes draw on the same facts (confirmation number, each transaction's status, follow-up and next owner). Not a seventh QA field — no documentation standard approved. "Closing the loop doesn't always mean closing the case."
- [Claude] Notes spare the customer repetition; they don't replace verification (Nina, Sep 9: the serial check remains necessary).

### 54. Imani's practice experiment, Sep 18 — `foundation`
**Source:** `meetings/qa-team-notes.md`, Sep 18.
- Two de-identified Specialist snippets (restart loop vs. serial check); each participant wrote "a one-sentence transition from listening to action"; Imani asked "what action the sentence would unlock"; most improved on the second try. "One Guide said she would rather have a small prompt on screen than memorize a sentence." Unattributed: "I understand the call flow. I am still nervous about the free year because I do not want to say it is active if the system is pending."
- [GPT] Evidence for brief practice plus in-call support.

### 55. Amina, Sep 16 — "a clip and a cue" — `finding`
**Source:** `meetings/qa-team-notes.md`, Sep 16.
> "When I coach, I need a before and after. What did the customer say, what did the Guide do, and what should they try next time? I can do that in five minutes if I have a clip and a cue. I cannot create a new quality program while I am covering absences."
- Priya (same entry): the link alone wouldn't tell her what a Guide would do while a frustrated customer waited; nor would an LMS completion report.
- Elias offers "a small set of de-identified call clips" on Oct 1.

### 56. Priya, Sep 19 — the smallest manager behavior — `finding` (sizes item 45)
**Source:** `meetings/qa-team-notes.md`, Sep 19.
> "We should ask for the smallest manager behavior that makes the learning stick. A cue plus one call listen may be enough for a test. If it is not enough, we will learn that. I do not want to launch a manager course as a substitute for giving them the right information."

### 57. Two Lead responses, Sep 22 — `finding`
**Source:** `meetings/qa-team-notes.md`, Sep 22.
- Remote team: "We have new hires who know CLEAR from onboarding and experienced people who know the products. The risk is assuming either group can combine those things on a live incident call. If Learning pilots something, sample both groups."
- Site 1: "I am concerned we will make the serial check another long compliance step. The customer first needs to feel that we understood what dropped. Then get the data. The order matters."

### 58. Sep 18 shift feedback — ineligible practice; Ben's huddle — `finding`
**Source:** `meetings/2026-09-18-shift-feedback.md`, 10:21 and 10:27.
- Rina: "A practice case with an ineligible unit would help, because the easy example always has a happy ending."
- Ben: a ten-minute huddle with two Specialist clips worked ("People got the point faster…"), "But I could not tell them which Beacon article to use. I wrote the temporary specialist page name on a whiteboard, and it is not visible to everyone. My other shift did not get the huddle."
- Imani 10:15: "People can tell you all five CLEAR steps in a quiz. The issue is the pivot from listening to acting."

### 59. Pending Plus, still unanswered in practice, Sep 22 — `dependency`
**Source:** `meetings/care-observation-notes.md`, Sep 22.
- Guide: "I just need to know what to say if the replacement works and the Plus step says pending." Lead H.: "Please document the case and use the follow-up process if a transaction does not complete. We will get a coaching note when one is ready."

### 60. A channel for search fixes already exists, Sep 21 — `finding`
**Source:** `2026-09-21-care-weekly-update.md`.
> "Please submit examples of customer search phrases that do not return the expected Beacon article through the normal content feedback form."

### 61. Ben Cruz, Sep 5 — "WN7" vs "WN-7" — `finding`
**Source:** `meetings/care-observation-notes.md`, Sep 5. A Guide asked whether "WN7" is the same as "WN-7" and searched both ways; the generic article appeared first.

### 62. From the routine files — `finding`
- LC-63 (Jul 27–28): images in Care articles ("photos in guides").
- Glossary ownership (Aug 20–21): Knowledge Operations drafting an ownership table for terms Care and Product define separately.
- Every routine follow-up: "The current published process remains in place until the owner confirms the update" — a ready model for ownership of the WN7 fixes.

### 63. Oct 1 CX check-in — `finding` (closes item 3)
**Source:** `meetings/2026-10-01-cx-check-in.md`.
- Elias 16:16: early serial check + accurate explanation + both steps → strong feedback and shorter calls (sampled, not randomized; Specialist cases may differ); General Care's first week "still shows mixed handling"; "I would test a response before saying we know it will scale."
- **Dana 16:21:** "I was thinking of a very short refresher because I cannot pull 900 hourly Guides off phones for a long course while the queue is this high. I still need something practical for Team Leads next week."
- Renee 16:25: can protect small groups outside the peak window; a broad 20-minute assignment across all shifts "would mean more unanswered calls, and I need that cost visible."
- **Marisol 16:29:** "five minutes is not a ceiling… It may even take practice. I need a reason to believe it will work before we take hundreds of hourly Guides off the phones. A completion rate would not tell me that. I care about fewer repeat calls and a recovery customers believe, along with handle time."
- Dana 16:34: "I do not want an elaborate program that arrives in November." Brings the recommendation to Priya and Mateo on Monday.
- Jules 16:38: notices still in review; if sent, call mix and volume may change.
- Action notes: Renee models coverage once the proposal has a group size and time; Elias can provide de-identified clips; no format or duration approved.
- [GPT] Next step: a one-page intervention architecture (audiences, observable behaviors, dependencies, materials, evaluation) before designing anything.

---

## Decisions after discovery

### 64. Workbook pass before setting priorities — `process`
[Claude] flagged the two workbooks as the biggest remaining gap; [GPT] agreed; [You] approved. Results in `WORKBOOKS.md`: WN7-product mix explains the AHT rise (~39% of answered GC contacts, a product-code proxy); 44% of eligible calls with a recorded serial check still ended in generic troubleshooting (70 of 159); complete recovery ~11 min vs ~20 generic (not causal); center differences not shown; "900 Guides" unreconciled.

### 65. Core targets locked — `position` [You]
Locked Nov 5, 2026, after two review rounds (`GAPS.md`):
1. **End-to-end Guide performance:** recognize → verify → decide → execute → explain and document. Includes eligible, ineligible, and pending-Plus scenarios.
2. **Lead calibration and diagnostic coaching:** common expectations; when a call breaks down, find out whether the cause was understanding, tool access, or decision-making before prescribing coaching.
3. **In-call performance support:** concise, actionable guidance that complements the existing Beacon article rather than duplicating it.
4. **Cross-functional operational readiness:** dependencies, responsible owners, approval requirements, and what Learning drafts vs. what partners must resolve.
5. **Small, capacity-conscious intervention pilot:** tests the *intervention* (Lead calibration + Guide practice + in-call support), not just Guide performance. Includes new and experienced Guides; states group size and minutes per person for Workforce approval; examines observed behaviors, complete recovery, repeat contacts, customer feedback, AHT, and queue impact.

**Preserved distinctions [GPT]:**
- These are locked **design targets**, not locked deliverables or formats. The learner-facing sample (Guide reference, Lead cue, scenario, or a combination) is still open.
- The 70 checked-but-troubleshot calls are an **observed outcome**, not 70 proven decision failures. Misinterpretation / tool access / deliberate choice are diagnostic hypotheses, not a verified breakdown.
- Implementation details and unresolved dependencies remain open.

- Attribution: targets proposed by [GPT] from [Claude]'s gap draft, refined by [GPT] so the pilot tests the intervention, not just Guides; Lead-anchored rollout and "why" principle are yours; decision to lock is yours.
- Priority vs. sequence: eligibility-to-action is the top problem; Lead calibration is the first rollout step.

### 66. What do Leads actually know about the WN7? — `open question` `position` [You]
[You] We've been treating Lead readiness as getting Leads on the same page (a cue, a shared standard). But nothing shows how well Leads themselves recognize the WN7 or understand the recovery. Being aligned isn't the same as knowing the material. **Decision: clarify what Leads need to *know* about the WN7, separately from what they need to coach.**

- [GPT, not adopted — idea noted only] Three dimensions of Lead readiness: (1) WN7 knowledge — recognize the pattern, WN7/WNM-7 vs. eligibility, what Plus is and isn't, the policy's limits; (2) operational competence — Beacon, Orbit, reading the result, choosing the path, pending Plus, walking a Guide through a case; (3) coaching calibration — recognize a good call, locate a breakdown, tell knowledge gaps from tool or process problems. Then reinforcement. Proposed a short scenario-based readiness check before calibrating.
- What the packet shows about Lead knowledge [Claude] — **mixed, no baseline**:
  - Some Leads show strong WN7 knowledge: Sofia (label tip, pattern vs. slow streaming, Sep 13), Imani (impact-first, Sep 8–18), Ben (recognition cue, Sep 10).
  - At least one Lead was unsure early: Amina, Sep 11 — "Can we tell them the credit is a year of Plus, or is it a discount? Also, do we order the hub and then somebody else applies the credit? I want to avoid Leads inventing a handoff." (Before General Care had a path.)
  - Guides go to Leads for answers (Micah on hold to ask a Lead, Sep 18; Guide J., Sep 11), so Lead knowledge gaps pass straight to calls.
  - Lead H. couldn't answer pending Plus (Sep 22) — but no one could; that's a dependency, not a Lead gap.
  - Sep 28: two Leads said Guides first learned about `BH-4419` from a reviewer — suggests some Leads hadn't passed it on, possibly hadn't engaged with it.
  - Tracker (Sep 10): 15 of 18 completed the generic CLEAR refresher; nothing measured WN7 knowledge or practice.
  - Counterpoint: Leads themselves mostly asked for a cue, clips, and a pending-Plus answer (Sep 22, Sep 24) — not WN7 training. Leads may not see a knowledge gap, or may not have one; the packet can't tell which.
- Effect on architecture: the Lead calibration kit (material A) assumes Leads know the WN7 well enough to coach it. That assumption is unverified. Open design question.
- [You] Observation: Leads' requests throughout were "give me cues, what to pass to my Guides, what to watch for" — not "what I need to know." Possibly because Leads aren't on the phones the way Guides are.
  - [Claude] Pattern holds: Sep 22 pulse, Amina (Sep 16, Sep 24), Ben (Sep 15), Imani (Sep 24) all ask for coaching tools. Even Amina's Sep 11 knowledge question is framed as what to *tell* Guides.
  - "Not on the phones" is unconfirmed — the packet never says whether Leads take calls (open under item 26). Other explanations fit too: role framing (coaches ask for coaching tools); assuming knowledge comes from the article; asking to be taught admits a gap; many may already know it.
  - Implication either way: **what Leads asked for may not be all they need** — the same stated-vs-observed gap seen with Guides. Supports checking Lead WN7 knowledge rather than assuming it.
- [GPT, revised suggestion — not adopted] Leads' requests cluster as *what to communicate, what to recognize, what to reinforce* — performance translation, not process learning. Don't lead with a WN7 knowledge assessment (solves an unestablished problem). Use one realistic-case calibration activity; answers reveal understanding; address gaps if they appear. WN7 knowledge is a prerequisite to verify, not a deficit to assume. One Lead session, not two, unless evidence demands it. Leads still need enough operational understanding because Guides consult them mid-call.
  - [Claude] Fits material A without adding a component.
- **Your working answer [You], Nov 6 — "What Leads know":**
  - *(Experienced Leads, not all Leads)* identifying the problem.
  - That resources and tools exist — not necessarily the when and how behind them, the smaller distinctions, or reliably where to find them.
  - Evidence [Claude]: problem recognition — Imani (Sep 5, 08:39), Ben (Sep 5 end-of-shift), Sofia (Sep 13, Sep 19 chat reply); uneven by shift — Priya's three check-ins (Sep 16), 17 of 29 at office hours (Sep 8); tool location — Ben "could not tell them which Beacon article to use" (Sep 18, 10:27), Guides first heard of `BH-4419` from a reviewer (Sep 28); when/how and distinctions — every-caller serial question (Sep 10), Amina on Plus and handoffs (Sep 11), pending Plus (Sep 22). Optional qualifier: awareness that the tools exist is itself uneven.
  - Reading [Claude]: less a WN7 knowledge gap than a gap in what reached Leads and how consistently. Points the 3-minute refresher toward "the verified current state" rather than teaching the WN7. If adopted: someone who can answer on the spot must be in the session (Quality, plus a Specialist who ran the pilot, e.g., Harper or Mateo), or a surfaced gap has no one to fill it.

### 67. Organizer structure — parked for later — `design idea` (GPT, not adopted; saved at your request)
[You] Asked to keep this for later; nothing added to the organizer yet. Organizer = thinking tool, not a deliverable decision.
[GPT] Simple flowchart, three connected layers:
1. **What success looks like** — observable Guide behaviors + customer outcomes.
2. **Team Lead enablement** — *Readiness:* know the process, communicate, recognize, calibrate. *Reinforcement:* observe, diagnose, coach, follow up.
3. **Guide performance** — Recognize → Verify → Decide → Act → Explain/document.
- Separate margin for dependencies, unanswered questions, and evidence, so they aren't mistaken for things Learning has to build.
- No formats (video, job aid, huddle) until each part's job is established.
- Current organizer artifact: https://claude.ai/artifact/PjX54QGFHTMMhPyxMpNbxy (stop 01 "Lead alignment" only).

### 68. Lead one-pager as the takeaway from the Lead alignment meeting — `position` [You] (first format decision)
[You] Leads leave the alignment meeting with a one-page resource. **For Leads only.** Structure (yours): **Here's the situation → What you need to know → How you can help your Guides.** You're also adding a "What Leads need to do afterward" section to the organizer.
- [GPT] Make it a Lead field guide, not another WN7 policy summary: what Guides need to know (failure pattern, eligibility limits, recovery actions, Plus); what good looks like; what to coach (diagnostic questions: misunderstanding vs. tool vs. execution); what to escalate (Orbit access, pending Plus, policy questions). Usable before a huddle, during a Guide escalation on hold, or while reviewing a call. Practical, light on instruction.
- [GPT] Distinct jobs: **meeting** builds shared understanding, resolves confusion, calibrates expectations; **one-pager** preserves that alignment and supports reinforcement. Keep any Guide-facing reference separate — don't make one page serve both audiences.
- [GPT, adopted by you] Add "What Leads need to do afterward" — where readiness turns into reinforcement.
- [Claude] Fits draft material A (ARCHITECTURE.md). Note the parked rule from item 67 ("no formats until each part's job is established"): this one's job is now defined, so the decision is consistent with it. Watch for overlap with any Guide-facing reference (material C) so the two don't become competing sources of truth (item 10 risk); the one-pager can point to the Guide reference rather than restate it. Leads are learners in the alignment meeting, so this one-pager could itself satisfy the brief's "words a learner would see or hear" requirement — though a Guide-facing piece would show the frontline words more directly.

### 69. Team Lead working meeting: 20 minutes — `position` [You]
[You] Approved **20 minutes** for the Team Lead working meeting (down from GPT's first proposal of 25). Planning assumption, subject to Workforce approval. **Time split not decided.**
- Order agreed in discussion: situation → case discussion → alignment → close (cases before alignment so misunderstandings surface before the standard is set).
- Candidate splits (neither adopted):
  - [GPT] 4 situation · 8 cases + understanding check · 5 alignment · 3 takeaway, expectations, next steps. Protect the case minutes.
  - [Claude] 3 · 10 · 5 · 2 — keeps ~3 min per case (eligible, ineligible, pending Plus); the one-pager carries the refresher detail.
- [Claude] Conditions either way: Quality plus a Specialist who ran the pilot (e.g., Harper or Mateo) in the room to answer blockers live; blockers raised go onto Dana's owner list.
- Evidence on Lead time: one Lead could spare ten minutes (Sep 16); Priya's "smallest manager behavior" (Sep 19); Imani's huddles ran 9–10 min; Renee can protect short pilot time (Sep 19, Oct 1).
- **Update — split decided [You], Nov 6:** **3 · 8 · 6 · 3** (situation and WN7 refresher · case discussion and understanding check · align on Guide expectations and Lead coaching · takeaway, responsibilities, next steps). Proposed by [GPT]; the extra alignment minute is where the case discussion becomes a shared coaching standard.
  - **Rule adopted [GPT, decided by you]:** the refresher stops at three minutes. Anything needing deeper explanation is raised during the cases or assigned for follow-up.
  - [Claude] Still open: which cases fit in 8 minutes — all three (eligible, ineligible, pending Plus) at under 3 minutes each, or two plus one on the one-pager.
- **Update — split revised [You], Nov 6:** **3 · 7 · 7 · 3** (case discussion 7, alignment 7), replacing 3 · 8 · 6 · 3. Refresher hard-stop rule unchanged.

### 70. Working order for architecture; questions parked — `process` [You]
[You] Order for the architecture work: **1. What success looks like → 2. Team Lead alignment → everything else falls into place after.** Architecture critique (`ARCHITECTURE.md`) is next on your list; it hasn't been done yet. [GPT] agreed: hold formats, pilot size, and timelines until those two are settled.
- Already decided inside Lead alignment (don't conflict with the order): R1 Lead one-pager (item 68); R2 20-minute meeting, 3·7·7·3 (item 69).
- **Parked until after the critique:**
  - Does the Lead meeting include all 18 General Care Leads or only pilot Leads? ([Claude] noted a middle option: align all 18 Leads, pilot with 2–4 teams.)
  - Small groups: 3 clusters of Leads, each with a Specialist? ([Claude] notes: works for 7-minute cases; needs a shared answer sheet so Specialists don't give three answers; Mateo's sign-off; Specialist Team Leads like Harper may fit better; mix centers in each group.)
  - Which cases fit the 7-minute block.
  - Pilot size and the two-week timeline.

### 71. Shared Lead coordination thread — `position` [You]
[You] Part of the "moving forward" close of the Lead meeting: a **shared Lead coordination thread** for questions, blockers, coaching observations, and verified updates.
- Evidence it answers [Claude]: Sep 8 — "too much information by chat," a rumor, a workaround, and a draft email copied into separate channels; the group agreed a temporary note should be the source of truth "but did not identify who would publish it" (item 34). Sep 21 — Priya didn't know what most of her 18 Leads would do (item 49). Sep 22 — Leads found coaching activity hard to track across shifts (item 18).
- Risk [Claude]: another chat channel could repeat the Sep 8 problem unless *verified updates* are visibly separate from discussion and someone named posts them. Blockers raised here should feed Dana's owner list.
- Open: who owns and verifies the thread (Priya? Learning? Quality?); where it lives; how verified updates are marked.
- **Proposal held (not decided) [Claude], Nov 6 — thread ownership and verification:** one owner runs the thread; facts come from the people who own them.
  - **Owner:** Priya or a Lead she designates (manages the 18 GC Leads; took Beacon and access issues to Operations herself, Sep 18). Her time is the risk; a delegate may be more realistic.
  - **Verified updates:** posted by the owner, tagged with the source — e.g., "Verified: Product Ops, Oct 7." Sources by topic: offer, eligibility, Plus → Product Ops (Nina) / account systems; Orbit screen and permissions → Care Systems (Cam Hall); coaching standard → Quality (Elias); Beacon search and article → Knowledge Ops / content editor.
  - **Learning:** sets it up, turns recurring questions into one-pager updates, routes blockers to Dana's owner list. Not the verifier.
- **Distinctions brought over with the decision [GPT], Nov 6:**
  - **One shared thread for all Leads**, not one per small group — avoids splitting the understanding. Flow: small-group discussion → shared alignment → one ongoing thread.
  - **Who's in it:** the Specialists from the meeting, Quality, and a designated owner who routes unresolved questions.
  - **Scope discipline:** not a running conversation everyone must monitor — questions, blockers, useful coaching observations, confirmed updates only.
  - **Division of labor:** meeting = establish alignment · one-pager = preserve it · thread = maintain it.
  - **Beacon remains the official source of procedural guidance**; the thread doesn't replace it.
  - [Claude] Dependency: "the Specialists from the meeting" assumes the small-group format, which is still parked (item 70). The one-thread decision holds either way.

### 72. Short serial-number / Orbit tool video for Guides — `position` [You] (resource; refinement to come)
[You] Separate from the Lead meeting: a **2–3 minute serial-number tool video** for Guides, sent as a **resource, not a "complete this training" assignment** (email or similar).
- [GPT] Fits the evidence better than a broad WN7 video. Focus: *when to check* (recognize the pattern without assuming eligibility) · *what to look for* (the right Orbit panel and the actual result) · *what happens next* (Eligible → recovery; not eligible → ordinary support; point to `BH-4419`). Optional; Leads point Guides to it when relevant. Cautions: needs an approved screen reference and confirmed permissions first — a video can't fix access; don't make it the only place Guides learn to read the result — a screenshot or visual cue in Beacon is faster mid-call. Gives Dana a version of the short video she asked for without claiming video alone fixes recovery. GPT would mark it a candidate, not a commitment.
- Evidence [Claude]: 44% of eligible calls with a serial check still ended in generic troubleshooting (`WORKBOOKS.md`); a Guide couldn't tell which Orbit value was the result (Sep 22); one couldn't locate the result at all (Sep 24); Guide T.: fine with a short piece "if it is really five minutes and includes the screen I need" (Sep 20); Guide S.: "what I click and what I say" (Sep 8). Northstar has a Learning Media team that produces captioned videos (routine pair, Aug 24–25).
- Risks [Claude]: **blocked on item 47** (Orbit screen reference undecided Sep 24; permissions unconfirmed) — the screen can't be shown until approved. Email alone repeats the Sep 21 roundup problem (sent but not reliably seen, Sep 28); Leads pointing Guides to it via the thread (R3) is the stronger route.
- **Refinement, Nov 6:**
  - **Status [GPT, kept by you]:** decided, **conditional on the Orbit screen and General Care access being verified.**
  - **Correction [GPT, accepted]:** the 44% figure supports investigating the eligibility-to-action breakdown; it doesn't show that 44% of Guides need a tool video. The direct evidence for R4 is the two observed Guide difficulties (Sep 22, Sep 24) and Guide T.'s request (Sep 20).
  - **Delivery [You + GPT]:** email isn't success on its own. [You] Leads mention it in their huddles, alongside the email. [GPT] Leads introduce it, keep it on hand for coaching, and point Guides to it when the difficulty shows up.
  - **Complementary, not duplicate [GPT]:** R1 Lead one-pager helps Leads answer and coach consistently; R4 shows Guides how to read the eligibility tool. Neither restates `BH-4419`.
  - **Open, for later [GPT]:** does the video live inside or alongside `BH-4419` rather than as a standalone link?
- **Link to R2 [You], Nov 6:** the "moving forward" close of the Lead meeting includes asking Leads to introduce the R4 video in their next huddle.

### 73. Two cases in the Lead meeting — `position` [You]
[You] The Lead meeting's 7-minute case block uses **two cases**. Which two is still to be confirmed.
- Direction discussed (not decided): one call that shows the standard and one that shows a breakdown, so Leads practice diagnosing before coaching. [GPT] Move Priya's ineligible case (Sep 24) to Guide practice or the takeaway; label any reconstructed case as reconstructed.
- Candidates, all documented in `meetings/care-observation-notes.md`, Sep 24 joint listening (no reconstruction needed) [Claude]:
  - **Standard:** eligible, Plus credit didn't apply; Guide stayed with the handoff, opened follow-up, explained the case stays open; caller said it was clear.
  - **Breakdown (strong fit):** recognized the pattern but couldn't locate the serial result; transferred; reviewer couldn't tell whether it was Orbit permissions or not knowing the screen — the diagnostic question is built in.
  - **Breakdown (alternative):** eight minutes of generic troubleshooting before the article; both actions done; Plus described as "backup internet while the replacement is on the way."
  - **Ineligible WN7, different symptom:** done right; Priya: "the case we must keep in the practice set so people do not turn a product name into a promise."

### 74. Call-excerpt example bank — `design idea` [You] (proposed, likely; shape not set)
[You] Idea: add call excerpts with different cues to the Lead takeaway. Settled on **describing the bank** in the materials rather than writing out excerpts.
- [GPT] Split: 2–3 concise coaching cues on the one-pager (R1); a separate **example bank** of 3–5 real, de-identified excerpts Leads can pull for coaching or huddles. Cover failure modes, not complaint types: missed recognition · checked but didn't act · incomplete recovery · overpromising · strong execution. Pair each with what happened, the coaching cue, and what to try next time.
- [Claude] The packet has no call transcripts, only descriptions of calls. In the case, excerpts come from Quality's de-identified clips (Elias offered them on Oct 1), so the proposal names Quality as the source. In the interview materials the bank is described with placeholders, not presented as real calls (brief: "label the assumption"). The two Lead-meeting cases (item 73) can be the bank's first entries. Documented material is thin for "checked but didn't act" and "overpromising"; the QA workbook's reviewer notes may hold examples. Imani's caution: don't let the easy example dominate.
- **Status correction [You], Nov 6:** proposed, not decided. Likely to happen, but the shape is open — you're considering a **cheat sheet** format as a better fit for excerpts than a bank. "Describe, don't populate" for the interview materials still stands if it goes ahead.
- **Settled [You], Nov 6:** the excerpts go on a separate **coaching cheat sheet**. Leads leave with two one-page resources: the one-pager (R1, "what do I need to know?") and the cheat sheet (R5, "what do I listen for, and how do I coach it?").
  - [GPT] Cheat sheet: 3–5 short excerpts, each with *Listen for* · *What happened* · *Coach toward*. Focused on observable behavior; Beacon stays the authority for procedures, so the two documents can't conflict. Use one excerpt in the meeting, send Leads away with the rest. Leads asked for examples and cues, so this isn't extra material invented by Learning.
  - **Sourcing assumption (to label in the materials) [You + GPT]:** Quality provides approved, de-identified call excerpts. Quality offering clips doesn't guarantee recordings can be extracted and shared, so if they can't, Learning drafts illustrative scenarios grounded in documented call patterns — manually or with AI to speed drafting and variation. Quality and Specialist Care validate each before use against three criteria: **evidence fidelity** (reflects an observed breakdown, not a new one) · **operational accuracy** (eligibility, Plus, next actions match approved guidance) · **coaching usefulness** (a recognizable cue and a specific behavior to coach). Reconstructed scenarios are labeled, never presented as real calls.
  - **Correction [GPT, accepted]:** the two Lead-meeting cases (item 73) can appear on the cheat sheet, but only verified recordings or transcripts get labeled as real call excerpts. (They come from meeting-note descriptions, not recordings.)

### 75. Resource ownership, maintenance, and the AI signal — `position` [You]
[You] Approved Nov 6.
- **Ownership for R1 and R5 [GPT, adopted]:** a **content owner** (TBD; Quality partnered with Specialist Care is a candidate) for accuracy, updates, and retiring examples; an **approval authority** for procedural or Plus guidance (needn't be the owner); **review triggers**: changes to `BH-4419`, Orbit, Plus handling, or a recurring coaching issue. Both resources carry an owner and a last-reviewed date.
- [GPT] Ownership solves accountability, not maintenance: the owner needs to learn when guidance changes. The Lead thread (R3) can surface issues, but Beacon changes should trigger review through an official process, not a chat message.
- **Change notification [You, idea; GPT shaped]:** a Beacon change-notification process alerting the resource owner ("BH-4419 changed — review R1 and R5"). Roles: Knowledge Management / Beacon admin configures it; the resource owner reviews; the policy owner approves operational changes. Start manual; automate once it's confirmed how Beacon publishes changes (unknown in the packet — notifications, subscriptions, or API not documented). **Not part of the intervention for Dana**; included only as a short sustainability note: *"Assign a resource owner and establish a change-notification process tied to Beacon updates; explore automated alerts if supported."*
- **AI in the plan [You + GPT]:** don't force it. At most one credible future-state AI idea in the proposal (resource maintenance — flagging inconsistencies between Beacon and R1/R5 for the owner), plus the AI-assisted scenario fallback above. AI-assisted call analysis noted as higher impact but heavier on privacy and interpretation; not proposed. The interviewer note is where AI judgment is shown: what it helped with, what was verified, where its conclusions were rejected.
- **Hold [You], Nov 6 — scenario-development fallback:** the AI-assisted scenario wording isn't final. You'll specify what feeds it (which documented call patterns and sources) and the criteria, so the materials don't just say "use AI." The three validation criteria above are GPT's draft until then.
- **Held source list for the scenario fallback [You asked to keep], Nov 6** — documented call patterns to draw from when defining inputs:
  - Missed recognition: Sep 5 (Imani: two drop calls coded "setup," Guide re-ran restarts — `care-observation-notes.md`); Sep 28 (Elias: restart steps before the serial check — `threads/2026-09-28-care-release-followup.md`).
  - Couldn't locate the result / cause unclear: Sep 24 joint listening (`care-observation-notes.md`).
  - Incomplete recovery: Dev, Sep 18 10:34 (`2026-09-18-shift-feedback.md`); Harper, Sep 16 11:09 (`2026-09-16-qa-listening.md`); Sep 21 post-Beacon calibration (`qa-team-notes.md`).
  - Plus misdescribed: Sep 24, "backup internet while the replacement is on the way" (`care-observation-notes.md`); Guide L., Sep 13; Micah, Sep 18 10:09.
  - Ineligible, handled right: Sep 24 (Priya: "keep in the practice set"); Rina, Sep 18 10:21.
  - Strong execution: Specialist wording, Sep 12 (`product-comms-notes.md`); workday call, Sep 16 11:04; pending-Plus follow-up, Sep 24.
  - Possible extra source: QA workbook reviewer notes (`Quality_and_feedback.xlsx`, QA reviews) for "checked but didn't act" and overpromising.
- **Tweak [You + GPT], Nov 6 — notification is a workflow, not AI:** the Beacon change notification is framed as an ordinary maintenance workflow; basic change detection may be enough. AI is only an optional later enhancement if comparing revised guidance against several resources becomes a real problem. **The scenario-development fallback is the plan's one clear AI use; no second one manufactured.** [GPT] The two show different judgment: AI speeds content creation under evidence and human validation; plain automation handles maintenance, with the owner deciding what changes.

### 76. Guide Call Path; Lead cheat sheet renamed Lead Coaching Cues; resource design rules — `position` [You]
[You] Decided Nov 6:
- **Guide Call Path (R6):** a simple step overview Guides glance at during a call to stay on track, know where to go (Beacon, the Orbit serial tool), and cover blind spots like Plus. Deliberately simple so it doesn't replicate Beacon. Named "Call Path" rather than a second cheat sheet to show its different job.
- **R5 renamed "Lead Coaching Cues."** Leads spot the breakdown and coach; Guides stay on track and complete the recovery.
- [GPT] Draft steps (not final): Recognize → Verify (`BH-4419` + Orbit serial tool; don't assume eligibility) → Decide → Complete (incl. Plus credit or approved follow-up) → Explain & document. Plus gets a distinct visual reminder. No eligibility rules, detailed procedures, or unapproved Plus wording — those stay in Beacon. Open for the Guide phase: separate document or embedded in Beacon.
- **Design rules [GPT, adopted]:** one authority (Beacon owns procedures and policy; everything else points there) · one job per resource · one obvious access point per audience. Launch materials (meeting, video) introduce; ongoing references (Call Path, Coaching Cues) are what people return to.
- **Package pushback [GPT]:** one more resource only if it fills a distinct, evidenced gap. Next gains likely come from practice, Lead reinforcement, and removing operational blockers, not another document. The design reads as a performance-support system rather than a training campaign.
- [Claude] Notes for the Guide phase: (1) where the Call Path *lives* decides whether it adds a source of truth — at the top of `BH-4419` or as the Orbit desktop notice Cam described (Sep 19) beats a PDF in email; (2) "Verify" shouldn't add a search step — link straight to the Orbit panel, given the Sep 22 search failures; (3) include the ordinary-support branch and "stop the restart loop once eligible," not only the recovery branch; (4) **locked target 1 includes Guide practice (eligible, ineligible, pending); no practice opportunity for Guides is in the package yet** — the Call Path and video support, but don't give practice; (5) the Call Path is the clearest "words a learner would see" for the brief.
- **GPT's response to Claude's pushback, Nov 6 (your adoption not yet stated):**
  - **Practice is a missing *intervention*, not a missing resource [GPT; Claude accepts the reframe].** A short facilitated Guide huddle with Imani's clips and a couple of decision prompts covers the practice target; Guides use the Call Path *during* practice, not just receive it. Gives a way to check application, not just recognition.
  - **Location over format:** embed the Call Path near the workflow, but don't commit to an Orbit desktop notice until it's confirmed what Cam's notice can support.
  - **Direct Orbit access [GPT accepts Claude's correction]:** the Call Path links straight to the tools, with Beacon linked as the procedural authority; Guides shouldn't navigate through Beacon to reach Orbit.
  - **Both branches:** about half of WN7-product calls were ineligible in the data; a recovery-only path reinforces the wrong mental model.
  - **Learner-facing sample:** the Call Path is a strong attachment for Dana.
  - **Addition [GPT]:** keep a **pending / unclear** state — pending Plus, uncertain eligibility, or no tool access needs an escalation route rather than a forced eligible/ineligible choice.
  - **Next design focus [GPT]:** Guide practice, once Lead alignment is settled.

### 77. Plus FAQ inside Beacon (proposal for the Content Editor) — `position` [You] (partner-owned resource)
[You] Propose that the Content Editor create **question-first Plus guidance inside Beacon** — searchable under "Plus" — so a Guide with a Plus question mid-call finds the answer without reading another guide. Format: FAQ inside Beacon, not a separate document. The Guide Call Path (R6) flags Plus at the relevant step and links here.
- [GPT] Distinct jobs: Call Path = "where am I, what next?"; Plus FAQ = "something went wrong at this step; I need a specific answer." Candidate questions: credit didn't apply after replacement · Plus shows pending, what to say · who owns follow-up and what to document · when to escalate. Pushback: test that "Plus," "pending credit," etc. actually surface it; where the answer depends on Orbit or transaction state, use a small decision table inside the FAQ rather than prose. Content Editor doesn't invent answers — the Plus process owner approves. Framing for the interview: observed problem → design decision → why → dependency; separate proposed design from verified outcome.
- [Claude] Additions:
  - Add **"What is Plus, and does it fix the drops?"** — the recurring misconception (Guide L. Sep 13; Micah's customer Sep 18; Sep 24 "backup internet while the replacement is on the way"). Already-approved answer: Nina, Sep 21 (`2026-09-21-care-systems-sync.md`, 10:10).
  - Answers that already exist: failed transaction → case stays open for follow-up (Sep 9 account systems note; Sep 24 model call); documentation → "Finance needs the case ID tied to both events" (Samir, Sep 10, 15:11). **Only "pending" is still blocked** — the FAQ can go up without it and add it on approval.
  - Search test already exists at Northstar: Jul 20 routine fix checked "the product code and the common customer phrase" (item 24); content feedback form (item 60).
  - "Plus process owner" unnamed — candidates: Product Ops (Nina, wording), account systems (transactions, pending), Finance (Samir, documentation).
  - Keep scope to Plus in the WN7 recovery; Plus is a general $149/yr product (Ben's Sep 5 billing call), so a general FAQ would sprawl.
- Theme for the interviewer note [GPT + Claude]: sometimes the better intervention is improving access to accurate information, not training — echoes Malik, "It is not all a training failure" (Sep 21).
- **Refinements, Nov 6:**
  - **Correction [GPT, accepted]:** don't assume the four answered questions can publish while "pending" is unresolved. Publish approved sections separately only if the missing answer is clearly flagged and an approved escalation path exists; otherwise wait for a coherent minimum viable FAQ. Existing source statements still need editorial and operational review for this customer-facing context — "the answer exists" isn't "approved for publication."
  - **One approver [GPT]:** several contributors (Product Ops, account systems, Finance) are fine; the Content Editor coordinates and one designated approver signs off on publication.
  - **Learning's role ends at the handoff [You, agreed by GPT]:** Learning identifies the gap, proposes the intervention, and sets up the handoff. Content, approval sequence, and the pending answer belong to the owners. Knowing where Learning's responsibility stops is part of the design judgment.
  - **For Dana [GPT]:** What (question-first Plus guidance in Beacon) · Why (fast, accurate answers during WN7 recovery) · Who (Content Editor drafts; Product Ops, account systems, Finance advise and approve) · Dependency (pending-status guidance confirmed before publication) · Validation (test findability and accuracy with Northstar's existing search process).

### 78. Lead meeting: two Beacon mentions, two jobs — `position` [You]
[You] Kept both Beacon mentions in the Lead meeting and gave each a purpose instead of cutting one:
- **Establish understanding — "Mention the Beacon article, search troubles"** = context: guidance exists, but finding and using it has been hard.
- **Establish alignment — zoom-in** = application: Leads leave knowing exactly where `BH-4419` and the Orbit serial tool are and when Guides use each. [GPT wording, adopted in substance] *"Confirm where to find BH-4419 and the Orbit serial tool; clarify when Guides should use each."*
- **Timing [GPT, agreed]:** the zoom-in happens inside the case debrief, not as a separate demo — no second walkthrough in a 20-minute agenda.
- [Claude] Limits: until the Orbit screen reference and permissions are confirmed (item 47), the zoom-in can name the `WN7 eligibility` panel but not show screens. The organizer's "small groups with a specialist" line is still a parked question (item 70).

### 79. Lead meeting back to 25 minutes; Guide design stance — `position` [You]
[You] Nov 6:
- **Lead meeting: 25 minutes** (supersedes the 20-minute decision in item 69). Proposed working session, subject to Workforce scheduling approval. Agenda **3 · 10 · 9 · 3** [GPT split, adopted]: situation brief / WN7 refresh 3 · case discussion / understanding check 10 · align on Guide behaviors and coaching 9 · takeaways / next steps 3. Extra time goes to discussion, not presentation. Refresher hard stop still applies.
- **Design stance:** Guides don't need re-teaching or a big training; they need to be properly equipped — know where to look and what to say to carry it out. That comes from the Leads, who also monitor it afterward. **Design as if no Guide already knows how to execute, even if some do** — which is why their tools are in-the-moment tools.
  - [GPT] "Not no training — less instruction, more performance support and reinforcement." Call sample shows some Guides can't execute but not why; short practice and diagnostic coaching still matter. Guide Call Path (R6) becomes the centerpiece of Guide support: Recognize → Verify → Decide → Complete → Explain & document, with Orbit/Beacon links at the decision points, including unclear eligibility and pending Plus. Call Path navigates the approved process; it isn't a competing source of policy. Lead session sets up coaching; short Guide practice introduces the workflow; in-the-moment tools carry it into calls.
- [Claude] Notes: the 25 minutes sits above the strongest Lead-time evidence (one Lead could spare ten minutes, Sep 16; Priya's "smallest manager behavior," Sep 19) — the case for it is that it's one session that replaces fragmented coaching later; name that trade-off for Renee (about 7.5 Lead-hours for 18 Leads, plus Specialist time). With 10 minutes, two cases at ~5 minutes each fits well (item 73). "Design for a Guide who doesn't know" matches the data: 56% of eligible GC calls after Sep 21 still ended in generic troubleshooting. For practice, keep Ben's caution in view: "The people who need this most may not volunteer for practice" (Sep 16).
- **Split revised [You], Nov 6:** **3 · 9 · 10 · 3** — case discussion 9, alignment 10 (replaces GPT's 3 · 10 · 9 · 3). Organizer agenda updated to match.
  - **How it runs [You + GPT]:** the 9 and 10 minutes work as **one ~19-minute working session**, bookended by a 3-minute setup and a 3-minute close; the split is for planning, not two separate activities for Leads. Transition between them [GPT]: *What happened and why?* → *What should Guides do, and how should Leads respond?* — so the two parts don't repeat each other. A calibration session, not a presentation with activities.

### 80. Lead meeting cases locked — `position` [You]
[You] Locked Nov 6 (supersedes the open list in item 73):
- **Case A — strong recovery with a Plus complication** (documented Sep 24 call). Purpose: what good end-to-end execution and ownership look like, including the difference between completing the replacement and handling the piece that didn't finish.
- **Case B — serial checked, but generic troubleshooting continues** (composite of the call-sample pattern, 70 of 159). Purpose: diagnose before coaching. A recorded serial check doesn't prove the Guide saw or understood the result. **Case B ends with what the Lead asks or checks next**, not just a list of causes.
- Why not a second Plus case: Plus is already covered in the refresher, Case A, the coaching discussion, and the proposed Beacon FAQ (R7); a second Plus case would give up the diagnostic practice.
- Design principle [You]: *equip Guides to execute correctly in the moment, while Leads reinforce the standard and diagnose barriers over time.*
- Design notes, prompts, takeaways, the Lead's next checks, and confirmations needed: `LEAD_CASES.md` [Claude]. Notes, not finished facilitator materials.
- [Claude] Flags: Case A's source says the credit "had not applied" — not "failed" or "pending"; whether those are different states is for account systems to confirm. Case B is a composite of an aggregate pattern; no single documented call shows it, so it's presented as an Orbit call record using real data fields, and labeled.
- **Refinements [GPT, accepted], Nov 6:** (1) softened Case A takeaway to "don't sacrifice a complete recovery just to shorten the call" — not "longer beats a callback," which implied longer is better and that completion prevents callbacks; (2) Quality's six fields labeled as Quality's **draft** proposal wherever they appear, so the meeting doesn't quietly introduce a new process requirement. Case selection and conceptual design settled; `LEAD_CASES.md` stays design notes, not a facilitator guide.
- **Organizer update [You + GPT], Nov 6:** under *Establish alignment*, replaced "Recap/discuss cues" and "Keep an eye out for…" with **Agree on coaching cues** — a five-row table (WN7 recognition · serial verification · recovery decision · complete recovery · customer explanation and documentation), each with what Leads should investigate and an illustrative example, plus a footnote (illustrative, not verified quotes; system records don't show what the Guide saw; proposed coaching aids, not QA fields) and a *Lead response* line. The cues come out of the Case A/B discussion, not a separate activity. Seed for the later Lead Coaching Cues resource (R5). Removed the duplicate shared-thread line in *Moving Forward*; owner stays TBD.
- **Cues table revised [You], Nov 6:** examples tightened to documented Northstar wording and call patterns ("Everything dropped," "My whole house went offline"; Orbit check recorded; eligible result + generic troubleshooting; order completed + Plus unresolved; notes didn't show whether order or credit started), investigate column shortened to one question per cue, footnote shortened. "More recognition phrases" list dropped.
- **Takeaway section revised [You], Nov 6:** "Takeaway resources for Leads" now names both resources with their jobs — **Lead one-pager = operational reference** (WN7 summary and reminders; Guide recovery sequence; where BH-4419 and the Orbit tool are and when to use each; Lead responsibilities, follow-up, escalation channels) and **Lead Coaching Cues = coaching reference** (strong/weak call examples; observable cues; diagnostic questions; coaching vs. escalation). Footnote: approved de-identified excerpts where available, otherwise labeled illustrative scenarios validated by Quality/Specialist Care. RESOURCES R1 and R5 updated.

### 81. Small-group structure settled; Lead alignment page settled — `position` [You]
[You] Nov 6: the Lead meeting includes **Specialist-supported small-group case discussion, followed by shared alignment on Guide expectations and coaching responses** — part of the continuous 19-minute case-and-alignment block, not an extra activity. Resolves the small-groups question parked in item 70. **Specialist availability is a staffing dependency** (Specialist Care sign-off), not a confirmed commitment. Number of groups and whether all 18 Leads attend remain open (item 70).
- Lead alignment organizer page considered settled; next focus: **Equip Guides**.

### 82. Lead alignment settled at the design level — `position` [You + GPT]
Nov 6. Evidence (what Leads know and need) → intervention (25-minute session, two cases) → outcome (shared recovery expectations, diagnostic coaching) → support (Lead one-pager + Lead Coaching Cues) → reinforcement (call reviews, huddles, Lead thread). The session calibrates how Leads support Guides; it doesn't teach Leads everything about WN7. Stop polishing the organizer; remaining unknowns are implementation dependencies.
- **Carry forward — don't forget [You]:** **Lead thread owner is TBD.** Before the proposal is final, name who monitors the thread and routes unresolved questions, or the channel has no accountability [GPT]. Held proposal (item 71): Priya or a Lead she designates; verified updates relayed with a source tag; Learning curates, doesn't verify.
- **Applied [GPT suggestion, adopted by you]:** removed "Review Case(s)" from *Establish understanding*; the two cases now sit under the 9-minute agenda segment, since they bridge into alignment.
- Implementation dependencies (not design blockers): Specialist availability · approved clips · Orbit screen and General Care access · pending-Plus wording.
- Next: **02 — Equip Guides.**

### 83. Equip Guides: Cues and Proper Sequence kept separate — `position` [You]
Nov 6. Under *What Guides need* in the organizer: **Cues — recognize when to act** (Ben's recognition cue, Sep 10; Imani's impact-first refinement; recognition triggers verification, not an assumption of eligibility) and **Proper Sequence — know what to do next** (Recognize → Verify → Decide → Complete → Explain & Document; supported by the proposed Guide Call Path, R6; covers eligible, ineligible, unclear, and unresolved Plus). Kept separate as distinct performance needs; both may appear together in the Call Path later. Working design notes — neither cue nor sequence is approved Northstar procedure. Guide actions and Guide resources not expanded yet.

### 84. Guide practice huddle (intervention) with a one-slide sequence aid — `position` [You]
Nov 6. Closes the Guide practice gap flagged in item 76.
- **Roles [Claude framing, adopted]:** Guide practice huddle = the intervention · one sequence slide = its supporting aid · Guide Call Path (R6) = in-call performance support. The slide bridges Lead alignment and Guide execution; Leads bring it to huddles, so Guides don't have to find it.
- **Design additions adopted (Claude, with GPT's trims):**
  1. Show the three branches — eligible → recovery · not eligible → standard support · unclear → verify or escalate — so the slide doesn't teach "WN7 = replacement."
  2. Pair the slide with a short scenario that **forces a decision, not just recognition**. Primary: an **ineligible WN7** case (recognizing the pattern ≠ eligibility). Pending Plus as a follow-up prompt if time allows. (Evidence: Imani's practice format Sep 18; Rina Sep 18; Priya Sep 24.)
  3. A very short Plus reminder at "Complete"; the Call Path carries the detail.
  4. Ben's cue shown as an internal recognition prompt for Guides, not wording to say to customers.
- **Keep the slide lean [GPT]:** Ben's cue, impact reminder, five steps, three branches, and a short Plus line is near the one-screen limit; trim before adding. Teaching visual only — not a second Call Path, no procedures to maintain. Fits Sofia: "Please make the cue fit on one screen" (Sep 19).
- **Interview sample question — parked [You]:** GPT argues the Call Path is the stronger primary learner-facing sample (decision support, branching, workflow integration); Claude suggested the slide. You'll decide after submitting the package (Sunday) while prepping for the Wednesday interview.

### 85. Live safety net during rollout — Specialists in the Lead thread — `design idea` [You] (proposed; pending your confirmation)
Nov 6. Your intent: a short-term "live safety net while Guides get acclimated."
- Path explored: Specialist shadowing small groups → designated Specialist escalation → Guide-facing Specialist chat buddy. [Claude] Routed it through Leads instead: Specialist Care is the tightest capacity in the packet (Mateo Sep 10, Sep 19; Specialist abandonment ~3% → 24%, occupancy ~85%), and a Guide–Specialist side chat risks the Sep 8 "too much information by chat" problem.
- **Shape [GPT refinements]:** Guide uses the Call Path → asks their Lead → Lead posts in the shared Lead thread (R3), where a **small rotating pool of Specialists**, sized to Specialist Care's bandwidth, clarifies from approved guidance **during the first rollout days**. Existing escalation stays in place for urgent or formal issues; the thread isn't a guaranteed real-time service. No promised response times or dedicated Specialist.
- **Exit condition [GPT]:** at the end of the pilot, review what questions came up, which were resolved, which need operational fixes; then decide whether normal Lead coaching and escalation are enough. Not a permanent operating model.
- **Learning loop:** the thread owner monitors unanswered questions, tags recurring blockers (Orbit reading, permissions, Plus), and routes them to coaching, the Call Path, or the dependency owners.
- **Can't fix:** pending-Plus answers (no approved guidance yet) and permissions (Care Systems).
- **Placement:** pilot / rollout support, not Equip Guides.
- **Proposal wording [GPT]:** "During the initial rollout, a small, rotating group of Specialists may participate in the shared Lead thread, subject to Specialist Care capacity. This provides Leads with additional clarification while Guides become familiar with the recovery process. Recurring questions and blockers inform coaching and resource improvements; urgent issues continue through established escalation channels."
- [Claude] Bundle with item 81 as **one Specialist Care request** on Dana's owner list (meeting small groups + thread pool). Raises urgency on naming the thread owner (item 82).
- **Ownership decision [You], Nov 6:** bundle both Specialist Care requests under **Mateo** in the ownership map — one sign-off conversation, two commitments he can approve, modify, or decline independently: (1) Specialists in the 25-minute Lead session; (2) rotating Specialists in the Lead thread during initial rollout. **If capacity supports only one, prioritize the Lead session** — it builds lasting Lead capability; thread coverage is a temporary net. **Lead thread owner (TBD)** carried forward as an explicit ownership decision (monitor unanswered questions, route recurring blockers). Item 85 stays **proposed** until rollout planning confirms how it fits the pilot.
- **Equip Guides structure [You + GPT], Nov 6:** removed *What Guides know* from the organizer — the Lead page needed a baseline to shape calibration; for Guides, the support has to work whether a Guide is experienced, unsure, or new to WN7. Page now runs **What Guides need → Guide actions → Guide resources**. [GPT] Prior knowledge still matters in the **pilot**: check whether Guides at different levels can use the support, rather than assuming everyone starts at the same level. Sofia's entry trimmed to one line ending "requires procedural verification before inclusion in customer-facing guidance."

### 86. Complementary Lead and Guide actions after the meeting — `position` [You]
Nov 7. **Leads (Moving Forward):** monitor and coach Guide execution during existing call reviews — look for observable recognition, verification, path choice, completion or follow-up, explanation and documentation; diagnose breakdowns, coach, escalate tool or process blockers. **Guides (Guide actions):** apply the Call Path on live WN7 contacts using approved guidance, asking a Lead when needed.
- [GPT] Leads verify *observed* execution in the calls they review, not proficiency across ~600 Guides — don't promise competency validation from a handful of reviews.
- [GPT] Feedback loop for the rollout section: Guide practice → live application → Lead observation → coaching or escalation → intervention refinement.
- Organizer now has stops 03 *Rollout & Reinforcement* and 04 *Ownership* (yours).

### 87. Individual digital scenario replaces the proposed micro-huddle — `position` [You + GPT; Claude critique]
Nov 7. Revises item 84.
- **Scope [You]:** the digital scenario replaces only the separately proposed 3–5 minute micro-huddle. The **team huddle stays**, as the start of Lead–Guide alignment and dialogue, and the **sequence slide stays in it**. [Claude] I first framed this as replacing the whole huddle drill and suggested dropping the slide; you corrected that.
- **Shape [GPT]:** Guide enters a decision in text, compares it to a model answer; standalone page; video optional in the same message. Lead action changes from "share the video in huddle" to introducing and reinforcing the practice; Guide action adds completing it and bringing one decision to a follow-up.
- **Tightening [Claude]:** assign during scheduled work time rather than leaving it voluntary (Ben, Sep 16); budget the time with Workforce (Renee); 1:1s aren't documented, so say "next coaching conversation" or label it an assumption; keep the ineligible scenario as primary so no unapproved Plus wording is needed.
- **Locked flow [You + GPT], Nov 7:** team huddle + slide (introduce the WN7 workflow, open dialogue, launch practice) → individual scenario in or through Sana (assigned work time, free-text decisions, approved model responses) → live Call Path application → Lead coaching + call review.
- **Sana: assignment ≠ hosting [GPT, adopted]:** Sana is the assignment and access point. Learning Operations confirms whether the free-text, reveal-and-compare exercise runs natively in Sana or is linked from it. No new infrastructure unless needed.
- **Completion tracking [GPT, adopted]:** no scoring doesn't mean no tracking. Sana may record opened or finished. That's an operational measure, not evidence of competence; written responses stay private and ungraded.
- **Not a gate [GPT, adopted]:** Guides apply approved guidance on live calls right away; the coaching conversation reinforces it afterward.
- **Readiness checks, not approvals in hand:** Sana delivery capability (Learning Operations); practice-time scheduling (Workforce).
- **Organizer updated:** the Lead action "Tell leads to share about the video resource in huddle" became "Introduce and reinforce Guide practice"; Guide actions now list completing the practice, live Call Path application (unchanged), and bringing one decision or uncertainty to the next coaching conversation, plus a footnote with the readiness checks. Slide kept in the team huddle.
- Updated RESOURCES.md R8.
- **Guide actions expanded [You], Nov 7:** seven actions — (1) attend the team huddle* · (2) locate and review the Call Path · (3) complete the practice scenario* · (4) confirm the live support route* · (5) escalate unresolved issues · (6) apply the Call Path on live contacts · (7) follow-up coaching. **Pending Approval / Readiness** (kept separate on purpose): (8) Orbit serial-tool video · (9) Plus FAQ in Beacon. **Rollout Dependencies:** Sana delivery (Learning Operations); practice time (Workforce); Lead availability for live support and a fallback route (Care leadership + Workforce); micro-huddle removed, team huddle and slide kept. *Asterisks mark the actions tied to those dependencies.
- **Refinements [You + GPT], Nov 7:** Ben's recognition cue date checked independently: **Sep 10 is correct** (`qa-team-notes.md`, Sep 10 Team Lead preparation call); Sep 16 applies only to his voluntary-practice quote. Scenario marked *(proposed)*, still needing development and content validation. Video marked *(optional)*; rollout doesn't depend on it. Plus FAQ marked *(pending approval)*, with a separate **required** readiness item: an authoritative Plus support route regardless of FAQ status. **#4 vs #5 [You]:** #4 sets up the live support route (the Lead "live safety net," item 85); #5 uses it when a problem comes up. Your edits kept: asterisks on #1 and #4 removed, micro-huddle line dropped from dependencies. Guide actions **provisionally locked**.
- **Next — Guide Resources [GPT]:** map only to the needs and actions already defined (Call Path, huddle slide, digital scenario, Beacon Plus FAQ, conditional Orbit video). The live support route is an operational arrangement, not a resource. No new resources to fill the section.
- **Ownership gap → organizer stop 04:** who maintains the scenario and the Call Path when Beacon procedures change (TBD).
- **Customer Communication consolidated [You + GPT], Nov 7:** under *What Guides need*, the "a few words…" quote, the possible customer line, the acknowledge/explain/set-expectations bullet, and "I need to know what I click and what I say..." with Sofia's prompt are now one need: **Customer Communication — Know what to say and how to move the call forward.** Caveats kept: the customer line requires approval; Sofia's label check requires procedural verification. [GPT] Sofia's suggestion is a verification technique rather than wording, but it belongs here because the section covers how Guides move the customer through the conversation, not only scripts.
- **Guide Resources mapped; Equip Guides provisionally locked [You + GPT], Nov 7:** the Guide Call Path is the central resource; the others introduce it, practice it, or give deeper authoritative guidance. Call Path (proposed): in-call decision and execution support · team huddle slide: introduce and visualize the sequence · digital practice scenario (proposed): rehearse decisions and customer language · Beacon Plus FAQ (pending approval): authoritative Plus answers · Orbit video (optional): demonstrate serial-tool navigation. The live support route is an operational arrangement, not a resource. Working-note phrases dropped from Guide actions #4 and #5 so each stands on its own. [GPT] Can't slip without blocking rollout: Plus guidance route, Lead support route, approved Call Path, scheduled practice time. The video can slip. Next: **03 — Rollout & Reinforcement.**

### 88. Rollout success criteria set before the rollout sequence — `position` [You]
Nov 7. Top of organizer stop 03 *Rollout & Reinforcement*: **Rollout Success** statement (reviewed WN7 calls show more consistent recognition, verification, recovery decisions and documented follow-up than the pre-rollout baseline; customer outcomes show promising improvement; service capacity stays manageable). **Stakeholder Evidence:** Malik, Quality reviewer, Sep 15 Care Quality calibration (`care-observation-notes.md`): "Once the path is live, the important questions will be: did they recognize the pattern, check eligibility, complete both transactions, and explain what happens next?" (verbatim; the final sentence of a longer comment that opens "We need to separate behavior from availability"). **Observable Execution Rubric:** six dimensions (Recognition, Verification, Decision, Recovery, Communication, Documentation), plus evaluation guidance: apply only where relevant; same criteria before and during the pilot; observed behavior ≠ system-recorded events; investigate missing evidence; a proposed rubric, not a replacement for the QA scorecard.
- **Scope [You]:** this defines what success looks like, not yet how rollout is scheduled or measured. No phases, sampling or owners yet. **No numerical targets or scoring thresholds anywhere in the proposal, by design.**
- **Renamed [You + GPT], Nov 7:** "Observable Execution Rubric" became **Observable Indicators of Successful Execution**, because "rubric" implies scoring or formal evaluation and neither is proposed. The five guidance bullets were replaced by one note: "These indicators guide review of relevant behaviors in baseline and pilot calls. Apply them according to the circumstances of each call, distinguish observed behavior from system records, and investigate gaps before drawing conclusions." That also drops the "not a replacement for the QA scorecard" disclaimer. Coordinating with Quality on how the indicators are used is still needed; it's logged as an open question in organizer stop 04 (Ownership), not in the success statement.

### 89. Success is defined before the rollout plan, and the plan is tested against it — `position` [You]
Nov 7. Organizer stop 03 opens with the success definition (item 88) on purpose, before any rollout sequence is drafted.
- **Your logic:** defining success explicitly sets the tone for the rollout plan. "By the end we should be able to look and say yes, if things go according to plan, this will happen."
- **What that means for 03:** every rollout element that follows (sequence, pilot, reinforcement, review) should trace back to at least one part of the success definition: Guide execution (the six observable indicators), customer outcomes, or operational capacity. An element that doesn't serve one of them needs a reason to be there.
- **Structure on the page:** *Rollout Success* (subhead: "Defining success across Guide execution, customer outcomes, and operational capacity") → *Stakeholder Evidence* (Malik, Sep 15) → *Observable Indicators of Successful Execution* (subhead: "Defining the behaviors Leads and Quality look for when reviewing WN7 calls"), with one usage note.
- **Boundaries kept (item 88):** no numerical targets or scoring thresholds anywhere in the proposal; phases, sampling and owners come later in 03; Quality coordination on using the indicators is an open question in 04 Ownership.

### 90. Rollout framework: five evidence-gated phases — `position` [You]
Nov 7. Added to organizer stop 03 under the success definition (items 88–89), which is unchanged.
- **Organizing principle [You]:** designed backward from the success criteria. Each phase answers: does it make the desired Guide behavior possible, support its execution, or provide evidence that it's happening? Phases advance on evidence, not on a schedule.
- **Phases:** 1 Prepare (operational readiness) → 2 Pilot (introduce and practice) → 3 Observe & Adjust (evaluate execution, find breakdowns) → 4 Expand (scale on evidence and capacity) → 5 Sustain (maintain execution and reinforcement).
- **Same four fields per phase:** Purpose · Key activities · Evidence / outputs · Decision point (proceed / adjust / pause; Sustain uses maintain / revisit / retire).
- **Existing decisions carried in:** team huddle and slide remain; the scenario replaces only the micro-huddle; practice during scheduled time (Workforce); Sana pending Learning Operations; video optional; Plus guidance or escalation route is a prerequisite; Guide → Lead primary, Specialists only as capacity allows; scenario completion is an operational measure, not proficiency; pilot and expansion account for queue and Specialist strain.
- **Labeled open [Claude, in drafting]:** who makes the proceed/pause call; which customer-outcome and capacity signals to check; expansion increments and whether all 18 Leads attend the Lead meeting before or alongside expansion; Lead thread owner; maintenance owner (04). *(Revised by item 91.)*
- **Scope:** working framework, not the finished plan. No dates, numeric targets, staffing commitments or sample sizes. Next: work through it phase by phase, then turn it into the polished rollout plan for the proposal ZIP.

### 91. Rollout framework consistency pass — `position` [You]
Nov 7. A clarity pass on stop 03, not a redesign. Success statement, Malik quote, six indicators, five phases and the four fields are unchanged.
- **Prepare gate corrected:** Proceed now requires every dependency already named in Key activities: approved Call Path and authoritative Plus guidance or escalation route · validated Orbit eligibility workflow and General Care access · confirmed scenario delivery/access through Sana or an approved link · Lead alignment and a functioning Guide → Lead support/fallback route · Workforce-approved pilot group and scheduled practice time. The Orbit video stays optional. Pause if any required item is unconfirmed; required items aren't bypassed.
- **Pilot vs. Observe & Adjust:** the Pilot gate checks delivery and usability (is the intervention reaching Guides; are its components usable). Observe & Adjust evaluates whether execution is improving. Huddle attendance and scenario completion are delivery measures, not evidence of proficiency.
- **Observe & Adjust evaluation:** comparability note added (comparable call selection, applicable eligibility branches, the same six indicators, explicit treatment of missing evidence). The unspecified signals became a **proposed measurement set**, pending Quality/Workforce confirmation: complete and incomplete recovery · repeat contacts, where measurable · average handle time · wait time and abandonment · Lead and Specialist support load. Observed changes don't by themselves establish causation. Limited or mixed improvement generally means Adjust and observe again; Pause is reserved for serious operational strain, inaccurate or unusable guidance, unresolved critical access or support problems, or other conditions that make continued rollout inappropriate.
- **Expand, Lead readiness (proposed sequencing, pending confirmation):** each Lead is aligned before their Guides enter the rollout. This doesn't require all 18 Leads before the initial pilot. It replaces the earlier open question.
- **Removed:** my example of who might hold go/no-go authority, so it reads only as an open decision.
- **Still open (not settled):** pilot size and composition · review sampling and cadence · numeric success thresholds (none in the proposal, by design) · expansion increments · final go/no-go authority · Lead thread owner · resource maintenance owner · staffing and Specialist commitments · confirmation of the proposed measures (Quality, Workforce) · Sana delivery (Learning Operations) · Orbit workflow and access (Care Systems) · approved Plus guidance or escalation route.

### 92. Seven rollout decisions integrated into stops 03 and 04 — `position` [You]
Nov 7. A targeted integration pass. Success statement, Malik quote, six indicators, the Guide intervention, the delivery-vs-proficiency distinction, required readiness items and the optional video are all unchanged.
1. **Pilot scope (proposed):** 2–3 Lead teams with a representative mix of Guides, not volunteers or only high performers. Workforce sets the final Guide count, team selection and scheduling. Not a staffing commitment.
2. **Evaluation and baseline:** Quality leads; Leads contribute coaching observations and gap diagnosis; Workforce provides capacity data. Baseline: 204 eligible General Care calls, Sep 21–30 (`WORKBOOKS.md`): 76 complete (37%), 13 incomplete (6%), 115 generic troubleshooting (56%). These are pre-rollout findings, not six-indicator scores; Quality revisits the underlying calls where possible.
3. **Expansion gate (qualitative):** meaningful improvement in observable execution, critical workflow blockers resolved, capacity manageable; customer outcomes show promising directional evidence, without requiring every metric to improve right away. Limited or mixed evidence means Adjust, not suspension.
4. **Decision authority (proposed):** Care leadership owns proceed / adjust / pause, informed by Quality, Workforce, Learning and Specialist Care (partner table in 04).
5. **Expansion:** successive Lead-team waves; Workforce approves size and timing of each; each Lead aligned before their Guides enter; not all 18 before the pilot; refinements carried forward; same evidence gate each wave.
6. **Thread Admin (proposed):** Care leadership designates a temporary Admin; Priya proposed, pending confirmation *(superseded by item 93: no individual named)*. Coordinates, routes, tracks, circulates verified answers; doesn't own every resolution. Lead coordination only; Specialists conditional on capacity; not a permanent channel.
7. **Sustainment:** Learning maintains the learning materials; Quality monitors gaps; Care Systems validates Orbit; Specialist Care / policy owners validate procedures and Plus; Care leadership and Leads reinforce; Beacon authoritative. Learning doesn't independently approve policy.
- **Resolved by this item:** thread owner (now a proposed Admin), go/no-go authority, pilot composition, expansion increments (Workforce approves per wave), Call Path/scenario maintenance owner, and how Leads and Quality share the evaluation. The two earlier open questions in stop 04 are replaced by the ownership map.
- **Flagged, not changed [Claude]:** (a) the packet names Priya Bell as Manager of General Care, not a Team Lead, so "designates a Lead as Admin" and "Priya is the candidate" don't match; 04 says "a temporary thread Admin" for now. (b) Stop 01 *Moving Forward* still reads "thread-owned by (TBD)". (c) Item 75 named Quality with Specialist Care as the candidate content owner for the Lead one-pager and Coaching Cues (R1, R5); item 92 gives Learning the "associated learning materials" — which applies to R1/R5 isn't settled. (d) The six indicators' "What reviewers look for" header and 04 both name Leads and Quality as reviewers, while Quality now leads the evaluation; consistent, but Leads' role in formal review vs. coaching observation may need one line in the final plan.
- RESOURCES.md R3 and ownership map updated.

### 93. Rollout refinements and thread Admin correction — `position` [You + GPT]
Nov 7. Refinements, not structural changes.
1. **Baseline sequencing:** a fully reconstructed six-indicator baseline isn't a launch prerequisite. Quality sets the comparison approach before launch and completes the needed baseline review before interpreting pilot results (Prepare and Observe & Adjust updated; Proceed gate unchanged).
2. **Observation window:** Guides need sufficient opportunity to handle actual WN7 calls before Quality evaluates execution. No duration set. The Pilot gate now requires it, so scenario completion can't lead straight to performance conclusions.
3. **Three evidence layers:** Guide execution (six indicators) · customer recovery outcomes (complete and incomplete recovery; repeat contacts, where measurable), which show whether individual customers got the right resolution · operational signals (AHT; wait time and abandonment; Lead and Specialist support load), which show capacity but not resolution. The expansion gate now refers to customer *recovery* outcomes.
4. **Sampling and cadence:** deliberately not specified in this proposal; approach, accountability and decision logic are enough at this stage. No longer listed as an open decision.
5. **Thread Admin [You]:** Priya dropped (she's Manager of General Care, not a Lead). Care leadership designates a participating Lead as temporary Admin, with the specific person confirmed during Prepare. No individual named in the proposal; the role and responsibilities are what matter.
- Next: verify the ownership model in stop 04, then translate the organizer into the proposal deliverables.

### 94. Ownership-design pass closed — `position` [You]
Nov 7. Approved as proposed design choices; no new commitments.
1. **Lead one-pager and Coaching Cues:** Learning owns production and maintenance; Quality and Specialist Care validate relevant operational content. Resolves item 75's open content owner.
2. **Live Guide support:** Care leadership owns the arrangement; Leads provide first-line support; Workforce validates coverage; Specialist Care confirms escalation availability, subject to capacity. The established fallback route stays.
3. **Sana delivery:** Learning Operations owns confirmation of assignment, access and delivery, native or via an approved link.
4. **Lead working meeting:** Learning facilitates; Care leadership ensures participating Leads can attend; Specialist Care supports only with approval.
5. **Specialist capacity:** Mateo approves separately (a) Specialists in the Lead working meeting and (b) temporary shared-thread support. Neither implies the other.
6. **Expansion authority:** Care leadership decides whether evidence supports expansion; Workforce approves each wave's composition, timing, scheduled practice coverage and operational feasibility. Both are required. Workforce's row in the partner table updated from "advises" to "approves" to match.
- **01:** thread TBD replaced: "a participating Lead designated by Care leadership serves as temporary thread Admin during rollout."
- **03 Pilot observation:** Quality can observe and review live WN7 calls as soon as they occur; sufficient live-call exposure and comparable evidence are needed before performance conclusions or an expansion recommendation, not before observation starts. Continue gate no longer waits on call volume; the Observe & Adjust Proceed gate now references it. Delivery measures still never stand in for demonstrated execution.
- 03 Expand and Sustain lines aligned (dual approval; Learning updates Lead resources too).
- Ownership-design pass closed. Next: the proposal deliverables (not started).

### 95. Organizer locked as the working design baseline — `position` [You + GPT]
Nov 7. Stops 01–04 (organizer v621) are the design baseline for the deliverables. Further changes come through the deliverables, not by reopening the organizer.
- **Strengths noted [GPT]:** clear decision authority (Care leadership owns progression; Workforce controls whether each wave is operationally feasible); credible evaluation (the 204-call baseline is kept separate from the six behavioral indicators, and observation starts with live calls, not training completion); realistic constraints (no invented targets, guaranteed Specialist coverage or automatic expansion).
- **Carry into deliverables (organizer not reopened):** complete recovery is a documented outcome, not proof that the customer had a lasting resolution; repeat contacts help test that, where measurable.
- **Sequence:** one deliverable at a time, with review between each. (1) **Rollout plan**, built on stop 03 but more executive-facing: five phases, major actions, accountable partners, evidence, decision gates; detailed dependencies stay in the organizer. (2) Then check the Lead resources, Guide Call Path and proposal presentation against that plan.
- Status: nothing built yet.

### 96. ARCHITECTURE.md retired — `position` [You]
Nov 7. The draft intervention architecture has been superseded by the locked organizer baseline (item 95), RESOURCES.md, and items 64–95. Removed from the repo; it's still in git history (last present in commit 01cb0a2). Earlier references to it in this log are kept as history.
