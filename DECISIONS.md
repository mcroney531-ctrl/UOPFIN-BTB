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
1. One end-to-end Guide recovery behavior, practiced with eligible, ineligible, and pending cases.
2. A common Lead coaching and observation standard.
3. An in-call reference that helps Guides act without memorizing a speech.
4. Operational fixes assigned to their actual owners.
5. A small, capacity-conscious pilot evaluated on complete recovery and call behavior.
- Attribution: targets proposed by [GPT] from [Claude]'s gap draft; Lead-anchored rollout and "why" principle are yours; decision to lock is yours.
- Priority vs. sequence: eligibility-to-action is the top problem; Lead calibration is the first rollout step.
