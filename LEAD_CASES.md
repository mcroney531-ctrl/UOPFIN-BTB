# Lead meeting cases — design notes

**Status:** cases locked (item 80). These are design notes for the meeting proposal (R2), not finished facilitator materials. Nothing here is committed as an interview deliverable.

**Ground rules for both cases**
- Built only from the case packet. No invented transcripts, tool behavior, permissions, or Plus wording.
- Case A is a documented call. Case B is a composite of an observed data pattern and is labeled as such.
- Where the right answer depends on something Northstar hasn't confirmed, the case says so rather than resolving it.

**How they fit the 25 minutes:** 3 setup · **9 cases** (A ≈ 3–4 min, B ≈ 5–6 min) · **10 alignment** · 3 close. The middle 19 minutes run as one calibration exercise: *What happened and why?* → *What should Guides do, and how should Leads respond?* Quality and a Specialist who ran the pilot are in the room to answer on the spot.

---

## Case A — Strong recovery with a Plus complication

**Job in the meeting:** set the standard for good end-to-end execution, including the difference between completing the replacement and responsibly handling the piece that didn't finish.

**Source (documented call):** `meetings/care-observation-notes.md`, Sep 24, Elias and Priya's joint listening of five General Care calls:
> "One verified an eligible serial, completed the replacement order, then noticed the Plus credit had not applied. She told the customer she would stay with the handoff, opened the approved follow-up, and explained that the case remained open until the credit was resolved. The caller said that was clear. The call was still longer than the specialist examples because the credit system was delayed."

**Present it as:** the observed call, summarized as above (in the case, Quality could supply the de-identified clip — Elias, Oct 1).

**Discussion prompts**
1. The replacement went through. Why isn't the call finished?
2. What did the Guide do about the part that didn't complete? What did she *not* promise?
3. What would the incomplete version of this call have sounded like? *(Anchor: Dev, Sep 18 — order complete, Plus pending, call ended, customer called back.)*
4. This call ran longer than the Specialist examples. Was it still the right call?

**Expected Lead takeaways**
- A complete recovery means **both transactions done, or follow-up opened and explained** — not "replacement submitted." (Matches Quality's draft field: "Plus credit complete or follow-up opened," Sep 24.)
- Ownership of the unresolved piece: open the follow-up, keep the case open, tell the customer what happens next.
- Don't promise an outcome or timing that isn't confirmed.
- Record what's done and what's pending so the next contact can see it (item 53).
- A longer call that closes the loop beats a short one that causes a callback (Harper, Sep 16: "Our dashboard would have looked good if we only watched handle time").

**Coaching cue:** *Did the Guide recognize the unresolved piece and take ownership of it?*

---

## Case B — Serial checked, but generic troubleshooting continues

**Job in the meeting:** practice diagnosing a breakdown before coaching it, instead of assuming a knowledge or motivation problem. The case ends with what the Lead asks or checks next.

**Source:** a **composite**, labeled as such. Built from the call-sample pattern: of 159 eligible General Care contacts with a recorded serial check (Sep 21–30), 70 still ended in generic troubleshooting (`WORKBOOKS.md`). No single documented call in the packet shows this exact sequence, so the case presents a call record, not a transcript.

**Present it as:** a call record using only fields that exist in Orbit's call data:
- Product: WN7 · Reported pattern: intermittent disconnect
- Serial verified: **Yes** · Eligible for recovery: **Yes**
- Conversation path: generic troubleshooting · Disposition: troubleshooting complete
- Replacement arranged: No · Plus attached: No
- Handle time: about 20 minutes (typical for this group in the sample)

**What the record can't tell you:** whether the Guide saw the eligibility result, understood it, could act on it, or chose not to. **A recorded serial check doesn't prove the Guide saw or understood the result.** The case keeps that uncertainty open.

**Discussion prompts**
1. What does this record tell you, and what doesn't it tell you?
2. What are the possible reasons the Guide kept troubleshooting? *(Leads should generate these; the facilitator holds the list below.)*
3. **What would you ask or check first — before deciding how to coach?**
4. How would your coaching differ depending on what you find?

**Possible causes (facilitator's list, each tied to evidence)**
| Cause | Evidence it happens |
|---|---|
| Didn't know the next step | Guide R.: "If I have nothing else I can actually do…" (Sep 8); Micah on hold (Sep 18) |
| Couldn't read the Orbit result | Guide "did not know which value on the screen counted as the result" (Sep 22) |
| Access or process blocker | Reviewer couldn't tell "whether she had the correct Orbit permissions or simply did not know the screen" (Sep 24) |
| Chose to keep troubleshooting | Guide M.: "If I skip it… I get asked why I did not use the basic steps" (Sep 5, perceived pressure) |
| Something else | Customer insisted on troubleshooting; account complications (Sep 13); other — investigate |

**What the Lead asks or checks next (the skill being practiced)**
1. **Check the call itself if a recording exists:** did the Guide mention the result to the customer? *(Separates "saw it" from "didn't.")*
2. **Ask the Guide, without leading:** *"Walk me through what you saw after you entered the serial."* *(Interpretation.)*
3. *"What did you expect the next step to be?"* *(Knowledge of the path.)*
4. *"Were you able to open the replacement order and the credit action?"* — and if not, check with Care Systems whether the Guide has the access. *(Access.)*
5. *"What made you keep troubleshooting?"* *(Deliberate choice, perceived expectations, customer pressure.)*

**Then respond to what you found**
| Finding | Lead response |
|---|---|
| Didn't know the next step | Walk through the Call Path (R6); short practice |
| Couldn't read the result | Point to the Orbit panel / tool video (R4) once approved |
| Access or permission problem | **Don't coach — escalate** through the Lead thread (R3) to Care Systems |
| Felt expected to keep troubleshooting | Clarify the expectation (stop the restart loop once eligible); flag to Quality so scoring matches |
| Other / unclear | Log it in the thread; Quality looks for patterns |

**Expected Lead takeaways**
- The same observed failure can need four different responses; diagnose first.
- Some fixes aren't coaching at all — access and tool problems get escalated.
- Once eligibility is verified, stop the generic troubleshooting (Dana, Sep 10; Elias, Sep 16).

**Coaching cue:** *Did the Guide act on the verified result — and if not, what got in the way?*

---

## Into the 10-minute alignment

Pull from both cases:
- **Guide standard:** recognize → verify → choose the path → complete both actions or open follow-up → explain and document (Quality's six draft fields).
- **Coaching cues:** the two above, plus what to listen for (Ben's cue with Imani's "impact first").
- **Escalation:** what goes to the Lead thread vs. what a Lead handles directly.
- Zoom-in on where `BH-4419` and the Orbit tool are, and when Guides use each (item 78).

---

## Needs confirmation before use

| Question | Who confirms | Affects |
|---|---|---|
| "Had not applied" vs. "pending" vs. "failed" — are these different states, and does each need a different response? | Account systems / Product Ops | Case A takeaways |
| What the approved follow-up is, who owns it, and what the Guide may say about timing | Account systems / Product Ops | Case A |
| Whether a call recording/clip can be shown to Leads | Quality (Elias) | Case A presentation |
| Where the eligibility result appears in Orbit; General Care permissions | Care Systems | Case B checks 2 and 4 |
| Whether the six draft fields are adopted | Quality | Alignment standard |
| Who from Specialist Care attends | Mateo | Facilitation |
