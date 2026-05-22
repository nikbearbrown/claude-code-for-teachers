# Research: Chapter 4 — Handoff Conditions: The Gate Between Steps
## Claude Code for Teachers: A Practitioner's Guide

**Chapter one-line:** Not "looks good." A specific, testable condition that must be true before the next step begins. This is what separates conducting from approving.

**Research date:** 2026-05-21

---

## 1. Primary Sources

### Foundational papers and texts

- **Deming, W. Edwards. *Out of the Crisis*. MIT Press, 1986.** PDCA. "A bad system will beat a good person every time" — the argument for Ch 7 (Hooks) foreshadowed here.
- **Hoare, C.A.R. "An Axiomatic Basis for Computer Programming." *CACM* 12, no. 10 (1969): 576–580.** Pre/postconditions. A handoff condition is a postcondition.
- **Meyer, Bertrand. "Applying 'Design by Contract.'" *IEEE Computer* 25, no. 10 (1992): 40–51.** Design by contract.
- **Hopper, Grace. "The Education of a Computer." *ACM Symposium*, 1952.** "Done" must be defined before verified.
- **Spear & Bowen. "Decoding the DNA of the Toyota Production System." *HBR*, Sep 1999.** Andon-cord: stop on abnormality.

### Key empirical cases

- **The teacher's "broken link three days later" moment (TIKTOC opening).** Teacher reviews Claude's output, looks correct, approves. Three days later: broken link. The handoff condition the teacher didn't write. Real and recoverable.
- **The /rewind moment.** Esc twice or /rewind to restore previous state. Concrete demonstration of conducting at the failed-handoff moment.
- **The Pixar Toy Story 2 near-deletion (1998).** Animator's `rm` ran from the wrong directory. Pattern-correct, scope-wrong. Strongest precedent for "exit 0 isn't enough."
- **The GitLab 2017 database deletion.** Backup mechanisms exiting 0 nightly while producing empty archives. The killer detail: failed verification disguised as success.

---

## 2. The Core Concept — State of the Field

### What is settled

- **Exit codes are process-completion signals, not correctness signals.** Uncontroversial.
- **Postconditions are not implied by syntactic success.** Established in formal methods.
- **Layered verification reduces error rates.** Established in safety-critical systems.

### What is disputed

- **Whether all build steps need handoff conditions.** In proportion to consequence.
- **Forward correction vs. revert.** TIKTOC: forward correction adds failed attempts to context window. After two failed corrections, /clear and rewrite. Defensible.
- **What "binary, testable" means in HTML/CSS land.** Some handoff conditions are mechanically testable (lint passes); some require visual judgment (renders correctly on mobile). The chapter must distinguish.

### What has changed recently (last 5 years)

- /rewind (Esc twice) is a 2024–2025 Claude Code feature. Pre-/rewind, the discipline required manual git-revert. /rewind makes the revert-and-respecify rule operational.
- /clear and /compact (context management) are 2024–2026 features. The chapter teaches when to use each.

---

## 3. Application Domain Examples

(Domain coverage map: Ch 4 sits in class website.)

For the class website, three handoff conditions:

1. **After adding a page.** Weak: "looks good." Strong: "page renders on mobile (Chrome devtools, iPhone preset). All links on the page resolve. No CSS from prior pages has changed (run `npm run lint-html`, exit 0). The new page is linked from `src/index.html` nav."

2. **After a CSS change.** Weak: "no errors." Strong: "every previously-rendered page still renders identically (visual diff on three representative pages). The change appears only where intended (check by diffing the rendered DOM)."

3. **After a deploy step.** Weak: "rsync exits 0." Strong: "the live site at the class URL serves the current git SHA. The new page is reachable from the nav at the live URL. No 404s in the broken-link check."

The chapter must show the *writing* of handoff conditions, not just the listing.

---

## 4. The Book's Thesis Connection

Ch 4 closes Act One. The teacher has built one deployable page with CLAUDE.md, the gate, specifications, and handoff conditions. Designed classroom activities at each step. Gate 1 met.

The chapter's contribution:
1. **Operationalizes "verify."** Ch 1's gate ended with "verify"; Ch 4 says *how*.
2. **Sets binary acceptance threshold.** Teacher either knows what "done" means or doesn't.
3. **Introduces /rewind.** Concrete Claude Code feature that makes revert-and-respecify operational.

Student-supplied capacity: only the teacher knows what "done" means for *their* page on *their* server for *their* students.

---

## 5. The AI Wayback Machine — Candidate Figures

**TIKTOC names: W. Edwards Deming (1900–1993).** Strong fit.

Candidates:
- **Deming** — named. PDCA. "Bad system beats good person" foreshadows Ch 7 Hooks. Diversity: white male American.
- **Taiichi Ohno** (1912–1990, Japan). Andon-cord. **Strongest diverse alternate.** Cross-series consistent with gh-copilot teacher Ch 4 and CLI student Ch 12 recommendations.
- **Walter Shewhart** (1891–1967, USA). PDCA originator. More academic.

Recommendation: **consider Ohno swap.** Adds Japanese voice; substantive fit equal or better.

---

## 6. Pedagogical Delivery Research

### Prior knowledge required
Ch 1–3 fully assimilated.

### Common misconceptions to disarm
- **"Looks good" is a condition.** No. Feeling, not criterion.
- **"Forward correction is fine."** TIKTOC: /clear after two failed corrections.
- **"/rewind is for failures."** Also for "I want to try a different approach without polluting context."

### Effective instructional sequences
- **Strong vs. weak conditions side by side.** TIKTOC's pattern.
- **The /rewind demo.** Concrete: write a weak condition, encounter failure, /rewind, write stronger condition, re-run.
- **STOP block introduction.** Foreshadows Ch 7 Hooks. Conditions Claude must pause for.

### Known failure modes
- **The chapter as test-writing advocacy.** Handoff conditions are intent verification, not unit tests.
- **Over-formalization.** Written-but-flexible. No DSL.

### What separates understanding from memorization
A reader who *understands* Ch 4 has written handoff conditions for their three website pages and has used /rewind at least once when a condition failed. A reader who memorized Ch 4 can recite "specific, testable, binary" without applying.

---

## 7. Representation and Display Research

TIKTOC specifies two figures:

- **`<!-- → [DIAGRAM: The handoff condition gate.] -->`** Step N → [handoff check: specific, testable, binary] → Pass → Step N+1. Fail path: /rewind to checkpoint, respecify, rerun. Editorial style.
- **`<!-- → [TABLE: Strong vs. weak handoff conditions.] -->`** Five examples for class website context.

No additional displays required.

---

## 8. Open Questions and Research Gaps

- **Gate 1 acceptance criteria.** TIKTOC names. Chapter must end with concrete checklist.
- **STOP block specifics.** Conditions under which Claude pauses for human verification. Brief introduction here; full treatment Ch 7.
- **Visual handoff conditions.** When the condition is "renders correctly on mobile," it's not binary. The chapter should acknowledge: some conditions require human review; for those, the discipline is *which human and when*.

---

## 9. Sourcing Notes

- **Deming 1986** — MIT Press; 2018 reprint.
- **Hoare 1969** — open access *CACM*.
- **Meyer 1992** — IEEE.
- **Hopper 1952** — ACM DL.
- **Pixar Toy Story 2** — Pixar Touch (Price 2008); Oren Jacob interviews.
- **GitLab 2017** — about.gitlab.com/blog/2017/02/01.
