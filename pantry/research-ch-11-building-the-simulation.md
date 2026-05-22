# Research: Chapter 11 — Building the Simulation: Conducting at Full Complexity
## Claude Code for Teachers: A Practitioner's Guide

**Chapter one-line:** The three files are in place. The build begins. Every step has a specification, a handoff condition, and a labeled supervisory capacity. This is what conducting looks like at full complexity.

**Research date:** 2026-05-21

---

## 1. Primary Sources

### Foundational papers and texts

**TIKTOC names Schön here. Schön is also used at Ch 14 — double-booking. Recommendation: keep Schön at Ch 11 (reflection-in-action is more central here than Ch 14's reflection-on-action), swap Ch 14 to a different figure. Alternate for this chapter if rebalancing demands: Wanda Orlikowski.**

Sources for Ch 11 (independent of Wayback choice):

- **Schön, Donald A. *The Reflective Practitioner*. Basic Books, 1983.** Reflection-in-action — practitioner who thinks about what they are doing while doing it. Supervisory-capacity labels in the build log are reflection-in-action made operational.
- **Deming, W. Edwards. *Out of the Crisis*. MIT Press, 1986.** PDCA at command granularity. (Already used at Ch 4; cross-reference.)
- **Beyer, Betsy et al. *Site Reliability Engineering*. O'Reilly, 2016.** Runbook practice; iterative discipline.
- **Anthropic. Claude Code best practices (code.claude.com/docs).** Explore → Plan → Implement → Commit applied to simulation development.

### Key empirical cases

- **Seth's simulation build (TIKTOC).** Real prompts, real Claude outputs. The chapter's spine. Author + Seth produce.
- **The "browser screenshot iteration" pattern.** TIKTOC: define target state, give Claude a way to screenshot and compare, iterate until match. Feedback-loop produces dramatically better visual output than single-pass. Anchor case.
- **The Writer/Reviewer for simulation interaction design.** Subagent (Ch 9) reviews interaction from a student's perspective. Concrete worked example.
- **The "scope creep" moment.** Claude suggests "while I'm here" improvements; teacher logs in PROJECT.md Layer 2, doesn't execute.

---

## 2. The Core Concept — State of the Field

### What is settled

- **Iterative builds with verification produce better results** than single-shot generation. Anthropic-documented.
- **Per-step approval reduces compounding error** in agentic builds.
- **Three-file system protects against drift.** Established in 2024–2026 practitioner literature.

### What is disputed

- **Whether the per-step gate slows builds unacceptably.** Anthropic RCT data suggests engagement patterns match or slightly improve total time.
- **Whether autopilot is acceptable for simulation builds.** Book argues against pure autopilot. The discipline that builds capability is the per-step review.
- **State-reset verification.** Some argue automated tests sufficient; book argues manual verification before classroom deployment.

### What has changed recently (last 5 years)

- 2026 Claude Code's plan mode + Ctrl+G plan editing makes per-step gate operational.
- Screenshot-and-iterate is a 2025–2026 pattern; Claude Code can take screenshots via MCP tools.
- Hooks-in-skills and subagents-with-frontmatter are 2026 additions.

---

## 3. Application Domain Examples

(Domain coverage map: Ch 11 sits in interactive simulation.)

For the sorting-algorithm simulation (TIKTOC's working example pending OQ-1 resolution), Phase 1 build:

- **Step 1: HTML scaffold.** Specification names file structure, semantic elements, no styling. Handoff condition: HTML validates; structure matches DESIGN.md interaction-vocabulary requirements.
- **Step 2: CSS with the six DESIGN.md variables.** Specification names exactly which variables and which selectors use them. Handoff condition: visual matches DESIGN.md description (screenshot vs. reference).
- **Step 3: JS simulation logic for bubble sort.** Specification names the function signatures, the data structure, the step-control interface. Handoff condition: produces correct output on three test inputs; produces O(n²) comparisons on already-sorted input.
- **Step 4: Step controls and keyboard handling.** Specification names exactly which keys do what. Handoff condition: works on three test paths (forward step, backward step, reset).
- **Step 5: Mobile responsiveness check.** Specification names the breakpoint and the expected layout change. Handoff condition: Chrome devtools mobile preset renders correctly.

One rejection and revision: Step 3's first version uses `setTimeout` for animation; doesn't match the step-controls in Step 4. /rewind to Step 3 checkpoint; respecify with explicit step-by-step (no auto-advance) requirement; re-run.

One scope-creep moment: Claude suggests adding insertion-sort visualization "while I'm here." Logged in PROJECT.md Layer 2 as future. Not executed.

---

## 4. The Book's Thesis Connection

Ch 11 is the framework in motion at full complexity. The teacher has all tools; the build uses every one.

The chapter's contribution:
1. **Framework in motion.** Every framework piece appears.
2. **Three-file system in action.** CLAUDE.md governs technical; DESIGN.md governs visual; PROJECT.md tracks state.
3. **The simulation works.** End of Ch 11: working simulation ready for classroom deployment (Ch 12).

Student-supplied capacity: at every step, the teacher's decision about whether the output serves the simulation's pedagogical purpose.

---

## 5. The AI Wayback Machine — Candidate Figures

**TIKTOC names: Donald Schön (1930–1997).** Strong fit. But Schön is also at Ch 14 — double-booking.

Candidates:
- **Donald Schön** (1930–1997, USA, philosopher/planner). Named. Reflection-in-action. Substantive fit excellent here.
- **Wanda Orlikowski** (born 1953, USA, MIT Sloan). Technology-in-practice. **Strongest diverse alternate.** Woman, American, ongoing scholar. Same recommendation as the gh-copilot teacher book Ch 11.

Recommendation: **keep Schön here; swap Schön at Ch 14.** Reflection-in-action is more central at Ch 11 (during the build) than Ch 14 (after the build). Ch 14 can take bell hooks or another figure.

---

## 6. Pedagogical Delivery Research

### Prior knowledge required
Full framework + Ch 10 three files.

### Common misconceptions to disarm
- **"With three files, the build should run itself."** No. Per-step gate remains.
- **"I'll skip explain on familiar commands."** No.
- **"Scope creep is fine."** No. Log in PROJECT.md; don't execute.

### Effective instructional sequences
- **Seth's full transcript annotated.** Every step capacity-labeled.
- **The three pivotal moments.** Handoff failure, scope creep, screenshot iteration. Specific.
- **The screenshot-iterate demo.** Concrete: define target, screenshot, compare, iterate.

### Known failure modes
- **Transcript dump.** Narrative + transcript.
- **The simulation as exhibition.** Pedagogical tool the teacher will deploy.
- **Over-claiming framework universality.** Shows it working at full complexity; don't extrapolate.

### What separates understanding from memorization
A reader who *understands* Ch 11 has built Phase 1 of their simulation following the framework, documented every specification and handoff condition, and used /rewind at least once. A reader who memorized Ch 11 can describe steps without producing a working simulation phase.

---

## 7. Representation and Display Research

TIKTOC specifies one figure:

- **`<!-- → [DIAGRAM: The simulation build loop.] -->`** Three files populated → specification → Claude executes → handoff check → [Pass: next step / Fail: /rewind and respecify]. Subagent research branch off main loop. Supervisory-capacity label at each human step. Editorial style.

---

## 8. Open Questions and Research Gaps

- **Seth's specific simulation (TIKTOC OQ-1).** Most acute here.
- **Schön over-use.** Strongly recommend swap at Ch 14, keep at Ch 11.
- **Screenshot-iterate tooling.** Claude Code's screenshot capability via MCP. Author should verify 2026 status.
- **Plan-mode + Code-mode integration for visual builds.** Author should test before drafting.

---

## 9. Sourcing Notes

- **Schön 1983** — Basic Books.
- **Deming 1986** — MIT Press.
- **Beyer et al. 2016** — open access at sre.google.
- **Anthropic Claude Code docs** — code.claude.com.
- **Orlikowski 2000** — open access via AOM archives.
