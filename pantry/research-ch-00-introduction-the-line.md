# Research: Chapter 0 — Introduction: The Line
## Claude Code for Teachers: A Practitioner's Guide

**Chapter one-line:** There is a line between what Claude executes and what only you can do. This book teaches you to draw it — by building real things, then teaching students to draw it themselves.

**Research date:** 2026-05-21

---

## 1. Primary Sources

### Foundational papers and texts

- **Dewey, John. *Experience and Education*. Macmillan, 1938.** "Reflective practice" — the teacher learns by teaching. The interleaved structure (teacher build + classroom activity per chapter) is Dewey applied to AI-assisted classroom builds.
- **Computer Science Teachers Association. *The 2025 CS Teacher Landscape Report* (fall 2024 survey, published 2025).** 2,882 PK-12 CS teachers. 74% have 10+ years classroom experience, only 26% have 10+ years CS teaching; 96% participated in PD, ~47% did fewer than 11 hours. landscape.csteachers.org. The reader portrait sits on this data.
- **Anthropic. "Anthropic Education Report: How educators use Claude." anthropic.com/news/anthropic-education-report-how-educators-use-claude, 2025.** Teachers save 5.9 hours/week with AI. **Key finding for this book: educators are already building custom tools, not just generating lesson plans** — validating the teacher-as-builder thesis. Also: 48.9% of grading-related use is automation-heavy despite faculty rating grading as AI's least effective application.
- **Challen, Geoffrey. "A Day With Claude: Using and Teaching Coding Agents." Illinois CS faculty retreat presentation, January 15, 2026. geoffreychallen.com/talks/2026-01-15-a-day-with-claude-using-and-teaching-coding-agents.** The closest practitioner account. Key insight quoted in TIKTOC: *"the challenge in CS teaching is no longer turning specifications into code — AI is good at that — but rather getting ideas out of students' brains and into specifications that coding agents can work with."* This is the /v0 gate discovered independently. Specification-writing IS CS education.
- **Shulman, Lee S. "Those Who Understand: Knowledge Growth in Teaching." *Educational Researcher* 15, no. 2 (1986): 4–14.** PCK. The book exists separately from the students book because teaching the discipline requires different knowledge than doing it. Full treatment in Ch 13.

### Key empirical cases

- **Seth's eighteen-months-later moment (TIKTOC opening).** Seth, eighteen months after the students book. Not explaining homework/quiz gap anymore — describing the first time he built something real with Claude Code and understood why the discipline matters from the inside. Author should preserve specifics.
- **Geoffrey Challen's CS 124 adaptation.** Challen's course adapted around AI coding agents: students with 8–9 weeks of programming experience building Android apps. The book's pedagogy of teacher-as-builder is validated by Challen's parallel CS-instructor-as-builder pattern.
- **The "teacher uses Claude for lesson plans" baseline.** The reader's starting point. The book's job is to move them from content-generation use to build-conducting use.

---

## 2. The Core Concept — State of the Field

### What is settled

- **K-12 CS teachers are time-pressured and under-prepared for AI-assisted build work.** CSTA 2025 data confirms.
- **Teacher-as-builder produces deeper learning than teacher-as-consumer.** Established in education research (Resnick, Papert, Kafai) and now in AI-specific contexts (Anthropic Education Report).
- **Specification-writing is the new CS literacy.** Challen's argument, now widely cited.
- **Reflective practice deepens both teaching and craft.** Dewey, Schön. The interleaved structure is a structural commitment.

### What is disputed

- **Whether teachers can become builders without significant developer skill.** TIKTOC's position: yes, with the conducting discipline (specification writing + verification, not deep coding). The book is the operational test.
- **Whether Claude Code is the right tool for K-12 teachers vs. a simpler interface.** TIKTOC takes a position: the framework applies to any agentic tool; Claude Code is the current implementation. Defensible aging-risk mitigation.

### What has changed recently (last 5 years)

- The Anthropic Education Report's data (2024–2025) and Challen's January 2026 talk are the new empirical anchors. The book is the first practitioner handbook for K-12 CS teachers to address Claude Code conducting specifically.
- Claude Code's agentic features (Skills, Hooks, Subagents) are 2024–2026 additions that did not exist when the field was first imagining agentic coding tools. The book's framework engages with these features as they are now, not as they were imagined.

---

## 3. Application Domain Examples

(Domain coverage map: Ch 0 introduces the three builds.)

- **Class website (Act One).** First build. Low-stakes; the teacher can rebuild if it breaks; the discipline is what's at stake, not the artifact.
- **Grading tool (Act Two).** Higher stakes — touching student work. The dangerous middle hits: AI-generated feedback that's technically correct and pedagogically wrong. ESL/AAVE bias compounds the risk.
- **Interactive classroom simulation (Act Three).** Highest stakes — running in front of 30 students. The Brutalist three-file system (CLAUDE.md / DESIGN.md / PROJECT.md) governs.

---

## 4. The Book's Thesis Connection

Ch 0 establishes the thesis: the teacher-as-builder and the teacher-as-instructor are the same discipline applied twice. The chapter must:

1. **Validate the reader.** CSTA 2025 confirms: experienced teacher, early in CS journey, time-pressured, under-supported.
2. **Establish the partnership with Seth.** Seth is the practitioner who has done what the teacher is about to do. Not student to manage; co-practitioner.
3. **Foreshadow the three builds.** Each introduces a conducting concept; each is deployable.

Student-supplied capacity (foreshadowed): the teacher's pedagogical judgment, irreducibly. None of the three builds can be conducted without it.

---

## 5. The AI Wayback Machine — Candidate Figures

**TIKTOC names: John Dewey (1859–1952).** Strong fit.

Candidates:
- **John Dewey** (1859–1952, USA, philosopher/educator). Named. *Experience and Education*. Reflective practice. Substantive fit excellent. Diversity: white male American. **Note: TIKTOC also uses Dewey at student book Ch 14 (last chapter) and the gh-copilot teacher book Ch 0.** Cross-series Dewey use is intentional differentiation across audiences.
- **bell hooks** (1952–2021, USA, scholar/educator). *Teaching to Transgress*. **Strongest diverse alternate.** Black woman, American. Could shift to Ch 14 in this book if Schön is swapped out there.
- **Paulo Freire** (1921–1997, Brazil, educator). Banking education. Diversity: Brazilian.

Recommendation: keep Dewey. If diversity rebalancing demands, Ch 14 is a better swap candidate (where Schön is double-booked).

---

## 6. Pedagogical Delivery Research

### Prior knowledge required
Basic terminal use (the reader can cd, ls, run commands if given exact syntax). Claude for lesson plans (Claude.ai familiarity, not Claude Code).

### Common misconceptions to disarm
- **"AI for teachers means faster lesson plans."** This book is about builds, not content generation. The chapter must establish this in the first three paragraphs.
- **"Claude Code is just a better Claude.ai."** No. Agentic system with file access, terminal access, autonomous execution. Different stakes; different discipline.
- **"I need to be a developer to do this."** No. Conducting requires specification + verification, not deep coding. CSTA 2025 confirms most CS teachers have 3–4 years of CS teaching — the book meets readers there.
- **"My students know more than me."** Partially true; not relevant to the book's argument. The teacher who has built knows what the technically-fluent student does not: what the discipline costs when skipped.

### Effective instructional sequences
- **Reflective-practice framing from page one.** The interleaved structure is the book's pedagogical commitment. Ch 0 explains it clearly so the reader sees why each chapter has both halves.
- **Concrete builds, not abstractions.** Name website / grading tool / simulation upfront.
- **CSTA 2025 numbers as validation, not lecture.** Reader knows they're not alone; don't moralize.
- **Dictation shortcut sidebar.** Practical detail for the 30-minute-Monday-night reader.

### Known failure modes
- **The "extra work" frame.** Frame as time-saver and capability-builder, not duty.
- **Over-claiming Seth's authority.** Seth is a co-practitioner; reader has more pedagogical experience.
- **Terminal intimidation.** CSTA 2025 data is reassuring; chapter voice should match.

### What separates understanding from memorization
A reader who *understands* Ch 0 can articulate why the book has both teacher-build and classroom-activity per chapter, and identify the three Acts' builds. A reader who memorized Ch 0 can list "website / grading / simulation" without grasping the interleaved-structure rationale.

---

## 7. Representation and Display Research

TIKTOC specifies one figure:

- **`<!-- → [DIAGRAM: The book's arc as three build tiers on a timeline.] -->`** Worked content:
  - Horizontal three-point timeline.
  - Tier 1: class website (Act One) — introduces gate, CLAUDE.md, specifications, handoff conditions.
  - Tier 2: grading tool (Act Two) — introduces five capacities, Skills, Hooks, Subagents, dangerous middle.
  - Tier 3: interactive simulation (Act Three) — introduces three-file system (Brutalist), classroom deployment, student-facing verification.
  - Editorial style. No color.

No additional displays required.

---

## 8. Open Questions and Research Gaps

- **Simulation domain (TIKTOC OQ-1).** What CS concept does Act Three teach? Sorting? Memory allocation? Recursion? Author + CS teacher advisory must decide before Ch 10 drafting. Foreshadow only in Ch 0.
- **Windows dictation shortcut (OQ-6).** Win+H confirmed; Linux equivalent (xdotool? Speech Note? Vosk?) needs research. Author must confirm before press.
- **Seth's specific opening scene.** TIKTOC frames it as Seth eighteen months after the students book. Author should preserve specific scene — what build, what realization, what changed.
- **Geoffrey Challen citation form.** The talk is the strongest practitioner source. Author should reach out to Challen for permission and consider including a sidebar quote.

---

## 9. Sourcing Notes

- **Dewey 1938** — Kappa Delta Pi reprint (1998) standard.
- **CSTA 2025 Landscape Report** — csteachers.org / landscape.csteachers.org. Verify specific stats against full report.
- **Anthropic Education Report 2025** — anthropic.com.
- **Challen 2026 talk** — geoffreychallen.com/talks/2026-01-15. The book's strongest practitioner anchor.
- **Shulman 1986** — open access via AERA.
