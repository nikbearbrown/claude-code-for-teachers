# Research: Chapter 5 — The Five Supervisory Capacities
## Claude Code for Teachers: A Practitioner's Guide

**Chapter one-line:** These are the five things you do that Claude cannot. Name them. Exercise them explicitly. Never delegate them.

**Research date:** 2026-05-21

---

## 1. Primary Sources

### Foundational papers and texts

- **Wiener, Norbert. *The Human Use of Human Beings: Cybernetics and Society*. Houghton Mifflin, 1950 (rev. 1954).** Feedback loops as the mechanism by which a system maintains its goal. The five capacities are the feedback mechanisms that keep a Claude Code build aligned with teacher intent.
- **Engelbart, Douglas C. "Augmenting Human Intellect." Stanford Research Institute, 1962.** Augmentation framework. The chapter is Engelbart applied to AI-assisted classroom builds.
- **Norman, Donald A. *The Design of Everyday Things*, rev. ed. Basic Books, 2013.** Gulfs of execution and evaluation. PF closes execution; PA + IJ close evaluation.
- **Klein, Gary. *Sources of Power: How People Make Decisions*. MIT Press, 1998.** Recognition-primed decision. PA is RPD applied to Claude output.
- **Anthropic RCT (canonical citation across the series).** High-scoring patterns. The five capacities are a finer-grained version.

### Key empirical cases

- **Seth's "almost shipped it" moment (TIKTOC opening).** Grading-tool output looks fine, produces feedback, fast. Seth almost ships. PA catches what verification doesn't. Author should preserve.
- **The five-capacity post-mortem of a Claude Code grading-tool failure.** Decomposed by which capacity was absent. Author + Seth produce.
- **The "feedback is technically accurate, would I say this?" pattern.** Anchor case for PA in grading context.

---

## 2. The Core Concept — State of the Field

### What is settled

- **Human-machine task division has 60+ years of literature.** Fitts (1951), Sheridan (1992), current human-factors taxonomies.
- **Pattern recognition and judgment are different operations.** Klein, Kahneman.
- **Named distinctions deploy more reliably than generic "judgment."** Vocabulary studies in expert pedagogy.

### What is disputed

- **Five as the right number.** Same as student books — operational choice.
- **Stability under tool improvement.** TIKTOC's Contested Claims: "currently requires human judgment." Hold lightly.
- **Distinguishability.** Some readers will conflate PA with IJ.

### What has changed recently (last 5 years)

- Anthropic RCT (2026) validates engagement-pattern framework.
- Claude Code's autonomous execution makes capacity exercise MORE important — the agent will continue unless the human intervenes.

---

## 3. Application Domain Examples

(Domain coverage map: Ch 5 sits in grading tool.)

For each capacity, plain teacher language in grading context:

- **[PA] Plausibility Auditing.** "This feedback is technically accurate. But would I say this to this student? Does it match the rubric in the way the rubric intends?" Claude produces fluent output calibrated for accuracy, not pedagogical appropriateness.
- **[PF] Problem Formulation.** "Am I building a tool that generates feedback, or a tool that flags patterns across submissions so I can write feedback myself?" If frame is wrong, output is wrong, elegantly.
- **[TO] Tool Orchestration.** "Do I give Claude the whole rubric or just criteria for this assignment? Skills (Ch 6) or CLAUDE.md (Ch 2)? Subagent for research (Ch 9)?"
- **[IJ] Interpretive Judgment.** "This feedback is correct, but this student has been struggling all semester. The feedback needs a different tone."
- **[EI] Executive Integration.** "Three prompts ago we agreed the tool would never generate a final grade. This output is generating grades. Stop."

---

## 4. The Book's Thesis Connection

Ch 5 makes the supervisory work nameable in the grading context. Act Two's stakes are higher — student work is at risk. The capacities matter more here than in Act One.

The chapter's contribution:
1. **Decomposition.** Five practicable operations.
2. **Diagnostic vocabulary.** Post-mortems become "PA was absent at step 3" rather than "I should have been more careful."
3. **Stability.** Tool-agnostic.

Student-supplied capacity: all five require teacher knowledge the model lacks.

---

## 5. The AI Wayback Machine — Candidate Figures

**TIKTOC names: Norbert Wiener (1894–1964).** Strong fit. Cross-series consistent with the gh-copilot teacher book Ch 5 (also Wiener).

Candidates:
- **Wiener** — named. Cybernetics. Diversity: white male American.
- **Lucy Suchman** (born 1951, USA, anthropologist). *Plans and Situated Actions*. **Strongest diverse alternate.** Woman, American.
- **Engelbart** (TIKTOC standard for "five capacities" in student books; avoid double-booking).

Recommendation: keep Wiener.

---

## 6. Pedagogical Delivery Research

### Prior knowledge required
Act One framework + Ch 1–4 internalized. The teacher is starting the higher-stakes grading-tool build.

### Common misconceptions to disarm
- **"Five things on every prompt."** Each capacity fires at a different moment.
- **"Conscious performance every time."** They fuse into single conducting practice.
- **"PA = paranoia."** Vigilance, not anxiety.

### Effective instructional sequences
- **Define each in grading-specific language.** Generic definitions land less well.
- **Trace a grading-tool build through all five.**
- **Diagnostic exercise.** Given a failed build, name absent capacity.

### Known failure modes
- **The chapter as glossary.** Lead with action.
- **Over-specification.** Usefully fuzzy.
- **PA-as-paranoia.** Distinguish.

### What separates understanding from memorization
A reader who *understands* Ch 5 can read an unfamiliar Claude transcript and label which capacity is exercised at each step. A reader who memorized Ch 5 recites five names.

---

## 7. Representation and Display Research

TIKTOC specifies two figures:

- **`<!-- → [DIAGRAM: Five supervisory capacities — labeled five-column layout.] -->`** Standard format.
- **`<!-- → [TABLE: Five supervisory capacities — label, name, what it catches, example failure when absent.] -->`** Standard table.

No additional displays required.

---

## 8. Open Questions and Research Gaps

- **Grading-context specifics.** Author + Seth or teacher contributor must produce 1–2 worked-example moments per capacity.
- **Cross-book consistency.** Student book Ch 5 and this book Ch 5 both teach five capacities. Cross-references should be explicit.
- **Capacity-fluency development.** Open empirical question.

---

## 9. Sourcing Notes

- **Wiener 1954** — Houghton Mifflin.
- **Engelbart 1962** — open access dougengelbart.org.
- **Norman 2013** — rev. ed.
- **Klein 1998** — trade.
- **Anthropic RCT 2026** — anthropic.com/research/AI-assistance-coding-skills.
