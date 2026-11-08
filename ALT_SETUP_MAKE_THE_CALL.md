# Setup prompt: Make the Call visual pass (alt account)

Paste this into a new Claude Code session that has both repos attached.

---

We're continuing the Northstar WN7 take-home project. Two repos, both on branch `ccr-312323a1-9vzgbn`:
- `mcroney531-ctrl/TN-UOP-FIN`: deliverables (`deliverables/`), tools (`tools/`), interviewer docs (`interviewer/`)
- `mcroney531-ctrl/UOPFIN-BTB`: decision log (`DECISIONS.md`, last item 155), `STATUS.md`, `HANDOFF.md`

Read `UOPFIN-BTB/HANDOFF.md` first, then `STATUS.md`.

**Task: the visual design pass for "Make the Call: Digital Practice"** (`TN-UOP-FIN/deliverables/wn7-practice-scenario.html`). It was deliberately left out of Round 2 (item 151). Every other learning resource is locked with the Round 2 Northstar visual system (items 153–155).

**How we'll work:**
1. I'll attach the current `wn7-practice-scenario.html` (also in the repo) so you can see it.
2. When ready, I'll bring implementation instructions and one or more reference visuals from my GPT design session. Don't start visual changes until those arrive; just get oriented.
3. You implement, I review, then we lock.

**Rules:**
- Visual and presentation changes only. Keep every word, the three-moment flow (Recognize & verify · Decide · Explain & document), the model responses, the "why this matters" text, the fictionalization framing, the Moment 3 two-field requirement, the no-scoring/no-storage behavior, the offline and no-JavaScript fallbacks, and keyboard/screen-reader support.
- Match the Round 2 Northstar system where it fits: the shared layer is `TN-UOP-FIN/tools/ns-system/` (palette navy #0F2E5E, cobalt #2E6BD1, ice #E9F1FB, amber #F8EED6, green #E5F4E9; opaque navy gradient banner with the logo and a divider; restrained line icons; semantic result colors: Eligible green, Not eligible navy, No clear result amber). The logo is `deliverables/assets/northstar-logo-white.png`.
- Save a before-copy in `TN-UOP-FIN/archive/round2-before/` first.
- Run `node tools/tests/practice-scenario.test.js` before and after (93 checks); update the tests only if markup hooks change, never to hide a regression. Check desktop and phone widths.
- Log each step in `UOPFIN-BTB/DECISIONS.md` (next item 156; attribution [You]/[GPT]/[Claude]), update `STATUS.md` and `HANDOFF.md`, and commit with the Co-Authored-By / Claude-Session trailer style used in the history. Push to `ccr-312323a1-9vzgbn`. No pull requests.
- Packaging (the three Dana folders plus the interviewer folder) is handled separately; don't start it unless I ask.
