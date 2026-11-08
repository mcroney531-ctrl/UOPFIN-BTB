# Handoff: picking up the Northstar package in a new session

For a fresh Claude Code session (or another account) taking over mid-project. Read this first, then `STATUS.md`.

## 1. Setup checklist
- **Repos (both on branch `ccr-312323a1-9vzgbn`):**
  - `mcroney531-ctrl/TN-UOP-FIN`: the deliverables, in `deliverables/`, plus `tools/`. Its default branch is a different, near-empty one; check out `ccr-312323a1-9vzgbn`. The browser test suites expect it at `/home/user/TN-UOP-FIN` (a symlink works).
  - `mcroney531-ctrl/UOPFIN-BTB`: this repo, holding the reasoning, decision log and status.
  - The new account needs GitHub access to both.
- **Case packet:** not in either repo, on purpose (interview material; this repo may be public). Upload the original case-packet zip to the new session and extract it outside the repos. Every quote and figure is checked against `sources/` in that packet.
- **Not reachable from another account:** the Working Organizer artifact and the Claude previews of the deliverables are private to the original account. `STATUS.md` summarizes the organizer's current saved state (v621, four stops, all locked). Every locked design is also fully expressed in the deliverables and in `DECISIONS.md`.
- **Tools:** PDFs rebuild with `node TN-UOP-FIN/tools/build-pdfs.js [filter]`. It prints the room left above each page footer, and a negative number means overflow. Shared print CSS lives in `tools/*.css`. Browser test suites are in `tools/tests/`; they use absolute paths under `/home/user/` and Playwright's preinstalled Chromium.

## 2. Where things stand (Nov 8)
- **Locked:** Interviewer Note + Design Decision Log (`interviewer/wn7-behind-the-design.*`, `interviewer/wn7-design-decision-log.*`, item 142; interviewer-only folder) · Dana pre-read email (`email/wn7-dana-pre-read-email.md`, item 136; not sent) · Huddle Sequence Slide (`wn7-huddle-slide.html` + `.pdf`, item 130) · Resource Overview (`wn7-resource-overview.html` + `assets/ro-*.jpg`, item 128; links all eight files, including the slide) · Rollout Plan Overview (`wn7-rollout-overview.html`, item 126) · Ownership Map Overview (`wn7-ownership-map.html`, item 124) · Rollout plan PDF · Lead meeting plan · Lead Quick Reference · Coaching Cues · Guide Call Path (HTML + PDF) · Make the Call practice scenario (redesigned, items 156–157).
- **Final review process (item 145):** Round 1 (wording, accuracy, terminology, small additions) for every document, then Round 2 (structure, hierarchy, layout, visuals) for every document; then packaging. Apply only the edits the user sends for each round; preserve everything else and diff-check. **Round 1 is complete** (items 145–150). **Round 2 (item 151):** one shared visual system applied to a user-specified set of documents (the user sends a list and screenshots; GPT and the user define the system; Claude implements from one consolidated prompt). Make the Call is excluded and gets its own design pass. System applied to the five in-scope resources (item 153) via `tools/ns-system/apply.py` (re-run after edits, then rebuild PDFs); before-copies in `archive/round2-before/`; **all five locked (item 155)**. **Make the Call's own design pass is locked (item 156)**; the approved file is in `TN-UOP-FIN/deliverables/` (item 157; before-copy in `archive/round2-before/`). Remaining: packaging when the user calls it.
- **Wrap-up plan (item 144), in order:**
  1. **Content review** (user + GPT) of the Interviewer Note, Decision Log and AI Extensions. The Note and Log are content-locked provisionally (item 142); AI Extensions is ready for final review (item 143).
  2. **Visual review** of the actual PDFs: typography, spacing, hierarchy, page breaks.
  3. **Final corrections:** the user sends one consolidated punch list. Apply only those items; don't reopen locked work wholesale.
  4. **Lock and package — ON HOLD until steps 1–3 are done.** Build Dana's three folders (01 — Start Here · 02 — Detailed Planning · 03 — Learning Resources, item 131) plus a separate interviewer folder (Note, Log, AI Extensions). Update and retest every relative link and the `assets/` paths, then check the ZIP contents.
  5. Optional visual polish, last.
- **During review** the user may ask for highlight-and-annotate pages; templates and refresh notes are in `TN-UOP-FIN/tools/review/`. Publish with the `downloads` capability.
- **Rebuild commands:** interviewer docs `python3 interviewer/src/build.py && node tools/build-interviewer-pdfs.js`; AI Extensions `node tools/build-ai-extensions.js`; huddle slide `node tools/build-slide-pdf.js`; print PDFs `node tools/build-pdfs.js`. Tests are in `tools/tests/`.

## 3. How we work
- **Roles and loop:**
  - The person decides. GPT reviews in a separate chat; its feedback is pasted in as prompts.
  - Claude builds, checks sources, and logs decisions.
  - Each deliverable goes: build a draft → stop for review → targeted fixes → lock.
  - Locked deliverables aren't reopened for cosmetic changes while others are unfinished (item 101).
- **Logging:**
  - Every decision goes into `UOPFIN-BTB/DECISIONS.md` as the next numbered item. The last one is 157.
  - Attribution is kept separate: [You], [GPT], [Claude].
  - Drafts are marked `draft`; locks are `position`.
- **Commits:** end every commit message with the Co-Authored-By / Claude-Session lines used throughout the history. Push to `ccr-312323a1-9vzgbn`. No pull requests unless asked.
- **Source rules:**
  - Use only the packet's fictional facts; label assumptions.
  - Never invent Orbit screens or click paths, Plus policy or statuses, customer scripts, escalation channels, dates, numeric targets, or staffing commitments.
  - BH-4419 and its linked Product Operations reference PO-117 (`sources/care-desk-september-bulletin.md`) are authoritative.
  - Verify every quote and date against the packet before using it.
- **Wording conventions:**
  - Completion is "reach, not proficiency."
  - Anything not showing `Applied` is still open; a call can close with owned follow-up while the transaction stays outstanding.
  - Recorded serial check ≠ proof the Guide read the result. Say "70 of 159 eligible calls with a recorded serial check."
  - The baseline is 204 eligible General Care calls (Sep 21–30) from a systematic Orbit call sample, with eligibility classified retrospectively: 76 complete, 13 incomplete, 115 generic troubleshooting.
  - Thread Admin = "a participating Lead designated by Care leadership." Don't name anyone.
  - Plus validation: Account Systems and Product Ops (proposed), with Specialist Care input; final policy authority is unconfirmed.
  - Mateo (Specialist Care) gives two separate approvals: A for the Lead meeting, B for thread support.
  - Expansion needs both Care leadership's decision and Workforce's approval of each wave.
- **Test claims:** describe browser checks as Claude's automated suite, not independently reproduced. Screen-reader testing hasn't been done.
- **Style:** Inter, the navy/white Northstar palette, and the approved logo at `deliverables/assets/northstar-logo-white.png`, which must ship next to the HTML files. The Resource Overview keeps its own existing design. Write plain, natural language; refer to people as they/them unless a source gives pronouns.

## 4. Key files
- `UOPFIN-BTB/STATUS.md`: inventory, organizer reconciliation, and the remaining order of work.
- `UOPFIN-BTB/DECISIONS.md`: the full decision history (items 1–157). Most relevant now: 87–100 (rollout), 92–94 (ownership), 101 (workflow rule), 104–114 (deliverable locks).
- `UOPFIN-BTB/CALL_PATH_AUDIT.md`: the PO-117 source audit and its open gaps.
- `UOPFIN-BTB/RESOURCES.md`, `LEAD_CASES.md`, `WORKBOOKS.md`, `QUOTES.md`: resource decisions, Case A/B, workbook figures, verified quotes.
- `TN-UOP-FIN/deliverables/`: all deliverables and print sources.

## 5. Keeping this current
After every lock, new deliverable or process change, update in the same commit:
- `DECISIONS.md`: the new item.
- `STATUS.md`: the deliverables table and the remaining order of work.
- This file: section 2 (where things stand), plus the last item number in sections 3 and 4.
- Any new tools or tests go in `TN-UOP-FIN/tools/`, not the session scratch space.
