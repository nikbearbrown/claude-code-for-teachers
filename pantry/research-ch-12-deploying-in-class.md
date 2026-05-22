# Research: Chapter 12 — Deploying in Class: From Build to Lesson
## Claude Code for Teachers: A Practitioner's Guide

**Chapter one-line:** The simulation works in your terminal. Now it has to work with 30 students who have never seen it. This chapter is about the gap between "it works" and "it teaches."

**Research date:** 2026-05-21

---

## 1. Primary Sources

### Foundational papers and texts

- **Montessori, Maria. *The Montessori Method*. Frederick A. Stokes, 1912.** Educational materials must be self-correcting — student discovers errors without teacher intervention. The "first 30 seconds test" is Montessori's "control of error" applied.
- **Montessori, Maria. *The Absorbent Mind*. Henry Holt, 1949.** Prepared environments.
- **Norman, Donald A. *The Design of Everyday Things*, rev. ed. Basic Books, 2013.** Affordances and feedback. The simulation's user-facing surface.
- **Anthropic. "Claude Artifacts" documentation.** Fastest path to a shareable URL. Useful for deployment.
- **GitHub Pages documentation.** Free hosting for HTML/CSS/JS. Alternative deployment.

### Key empirical cases

- **The teacher's "student clicks something unexpected" moment (TIKTOC opening).** First classroom deployment; student clicks something; simulation breaks. The chapter trains for this.
- **The first-30-seconds test.** Does a student who knows nothing about the code know what to do without instructions?
- **The cross-class usability test (TIKTOC classroom activity).** Student from another group tries each simulation without explanation. Builder observes. Documents what breaks. Conducts revision build.

---

## 2. The Core Concept — State of the Field

### What is settled

- **Classroom deployment differs from solo deployment.** 30 students, three OS configurations.
- **Graceful failure is a deployment requirement.** Silent failure in front of 30 students is worst-case.
- **Classroom observation reveals what no pre-deploy test catches.** Established teaching practice.

### What is disputed

- **Whether to test on every student machine or representative sample.** Three is practical.
- **Whether to demonstrate the simulation's failure modes to students.** The book argues yes — showing how the simulation was fixed from feedback is itself a lesson in conducting.
- **Claude Artifacts vs. GitHub Pages.** Artifacts: faster, single URL, no build step. Pages: free, public, more customizable. Either works for student deployment.

### What has changed recently (last 5 years)

- Claude Artifacts (2024+) enables sharing without setup; the chapter can recommend it as the fastest classroom-deploy path.
- 2024–2026 push for Chromebooks and BYOD makes cross-platform variance more pronounced.
- Student-AI interaction expectations have matured (2024–2026); students are more willing to engage with imperfect AI-built tools and provide constructive feedback.

---

## 3. Application Domain Examples

(Domain coverage map: Ch 12 sits in simulation deployment.)

- **The first-30-seconds failure.** Student opens simulation; sees a screen with no obvious starting point. The teacher hadn't included a "click here to start" affordance because the teacher knew what to do. Fix: add explicit affordance.
- **The unexpected-click failure.** Student clicks an element that's visually styled like an interactive element but isn't (a label that looks like a button). Simulation produces no feedback. Student stuck. Fix: either remove the visual cue or make the element actually interactive.
- **The mobile-or-Chromebook failure.** Simulation works on the teacher's laptop; on a Chromebook the touch events don't fire correctly. Fix: explicit touch-event handling alongside mouse.

---

## 4. The Book's Thesis Connection

Ch 12 closes the build-to-deployment loop. The simulation works in the teacher's terminal; classroom deployment is a new application of the framework.

The chapter's contribution:
1. **Names the deployment work.** Distinct from build work.
2. **Operationalizes the student-facing verification.** First-30-seconds, failure-states, progression.
3. **Reframes classroom observation as conducting.** The teacher who watches the simulation and conducts a revision build is exercising the framework on the deployment problem.

Student-supplied capacity: classroom observation. Only the teacher can watch.

---

## 5. The AI Wayback Machine — Candidate Figures

**TIKTOC names: Maria Montessori (1870–1952).** Strong fit. Cross-series consistent with gh-copilot teacher Ch 12.

Candidates:
- **Maria Montessori** (1870–1952, Italy, physician/educator). Named. Control of error. Substantive fit excellent. Diversity: woman, Italian — strong contribution.
- **Lev Vygotsky** (1896–1934, Russia, psychologist). ZPD. Less direct fit.
- **Reggio Emilia** (collective; Loris Malaguzzi 1920–1994). Prepared environment. Less individually attributable.

Recommendation: keep Montessori.

---

## 6. Pedagogical Delivery Research

### Prior knowledge required
Ch 11 (simulation built).

### Common misconceptions to disarm
- **"If it works on my machine, it'll work in class."** No.
- **"Pre-deploy testing is overkill."** Three checks, < 15 min.
- **"Failures in class are embarrassing."** Teaching opportunities.
- **"I'll fix it during class."** No. Fix in advance; observe for revisions.

### Effective instructional sequences
- **The three-check verification protocol.** Concrete, time-boxed.
- **Graceful failure examples.** "Click here to retry" vs. silent break.
- **The revision-build cycle.** Watch → note → /rewind framing applied to deployment.
- **Show students the fix.** Apply-level exercise: teacher demonstrates revision as a meta-lesson.

### Known failure modes
- **The chapter as deployment-engineering.** Keep classroom-specific.
- **Over-engineering verification.** Three checks; not seven.
- **The "perfect simulation" trap.** Most simulations need revision after first class. That's the discipline working.

### What separates understanding from memorization
A reader who *understands* Ch 12 has deployed their simulation, run the three-check verification, identified at least one issue, and conducted a revision build. A reader who memorized Ch 12 can recite the three checks without applying.

---

## 7. Representation and Display Research

TIKTOC specifies one figure:

- **`<!-- → [DIAGRAM: The student-facing verification pass.] -->`** Three checks in sequence:
  - Check 1: does a student who knows nothing about the code know what to do in 30 seconds?
  - Check 2: are failure states informative or just broken?
  - Check 3: does the simulation have a path from easy to hard?
  - Binary results; revision-build path on fail.
  - Editorial style.

---

## 8. Open Questions and Research Gaps

- **Chromebook-specific guidance.** Sidebar.
- **Touch-event handling for tablets/phones.** Brief sidebar.
- **District-IT for classroom deploy.** TIKTOC's OQ-3 names a district-IT appendix. Ch 12 references.
- **The "demonstrate the fix" lesson.** Pedagogically strong; sidebar treatment.

---

## 9. Sourcing Notes

- **Montessori 1912 / 1949** — Frederick A. Stokes / Henry Holt.
- **Norman 2013** — rev. ed.
- **Anthropic Claude Artifacts docs** — claude.com.
- **GitHub Pages docs** — pages.github.com.
