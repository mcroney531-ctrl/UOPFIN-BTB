# Handoff: picking up the Northstar package in a new session

For a fresh Claude Code session (or another account) taking over mid-project. Read this first, then `STATUS.md`.

## 1. Setup checklist
- **Repos (both on branch `ccr-312323a1-9vzgbn`):**
  - `mcroney531-ctrl/TN-UOP-FIN`: the deliverables, in `deliverables/`, plus `tools/`.
  - `mcroney531-ctrl/UOPFIN-BTB`: this repo, holding the reasoning, decision log and status.
  - The new account needs GitHub access to both.
- **Case packet:** not in either repo, on purpose (interview material; this repo may be public). Upload the original case-packet zip to the new session and extract it outside the repos. Every quote and figure is checked against `sources/` in that packet.
- **Not reachable from another account:** the Working Organizer artifact and the Claude previews of the deliverables are private to the original account. `STATUS.md` summarizes the organizer's current saved state (v621, four stops, all locked). Every locked design is also fully expressed in the deliverables and in `DECISIONS.md`.
- **Tools:** PDFs rebuild with `node TN-UOP-FIN/tools/build-pdfs.js [filter]`. It prints the room left above each page footer, and a negative number means overflow. Shared print CSS lives in `tools/*.css`. Browser test suites are in `tools/tests/`; they use absolute paths under `/home/user/` and Playwright's preinstalled Chromium.

## 2. Where things stand (Nov 7)
- **Locked:** Rollout plan PDF · Lead meeting plan · Lead Quick Reference · Coaching Cues · Guide Call Path (HTML + PDF) · Make the Call practice scenario.
- **In review:** Resource Overview, `deliverables/wn7-resource-overview.html` (items 115–117). Three sections (Lead, Guide, Team Huddle); the two overviews are separate files in the ZIP. Structure approved; screenshots wait for the visual pass; its links assume it sits next to the deliverables in the ZIP.
- **Still to do, in this order:**
  1. Ownership Map Overview (one page).
  2. Rollout Overview (one page).
  3. Huddle Sequence Slide.
  4. Dana's pre-read email.
  5. Interviewer note.
  6. ZIP packaging.
  7. Optional visual polish, last.
- **Deadline pressure:** Dana's email is the time-critical item, and the brief requires it.

## 3. How we work
- **Roles and loop:**
  - The person decides. GPT reviews in a separate chat; its feedback is pasted in as prompts.
  - Claude builds, checks sources, and logs decisions.
  - Each deliverable goes: build a draft → stop for review → targeted fixes → lock.
  - Locked deliverables aren't reopened for cosmetic changes while others are unfinished (item 101).
- **Logging:**
  - Every decision goes into `UOPFIN-BTB/DECISIONS.md` as the next numbered item. The last one is 117.
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
- `UOPFIN-BTB/DECISIONS.md`: the full decision history (items 1–117). Most relevant now: 87–100 (rollout), 92–94 (ownership), 101 (workflow rule), 104–114 (deliverable locks).
- `UOPFIN-BTB/CALL_PATH_AUDIT.md`: the PO-117 source audit and its open gaps.
- `UOPFIN-BTB/RESOURCES.md`, `LEAD_CASES.md`, `WORKBOOKS.md`, `QUOTES.md`: resource decisions, Case A/B, workbook figures, verified quotes.
- `TN-UOP-FIN/deliverables/`: all deliverables and print sources.

## 5. Keeping this current
After every lock, new deliverable or process change, update in the same commit:
- `DECISIONS.md`: the new item.
- `STATUS.md`: the deliverables table and the remaining order of work.
- This file: section 2 (where things stand), plus the last item number in sections 3 and 4.
- Any new tools or tests go in `TN-UOP-FIN/tools/`, not the session scratch space.
