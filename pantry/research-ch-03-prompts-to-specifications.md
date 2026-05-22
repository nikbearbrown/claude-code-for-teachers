# Research: Chapter 3 — From Prompts to Specifications: The First Build
## Claude Code for Teachers: A Practitioner's Guide

**Chapter one-line:** "Add a page to my class website" is a request. A specification names the file, the structure, what it must not touch, and what done looks like. The class website is the first build.

**Research date:** 2026-05-21

---

## 1. Primary Sources

### Foundational papers and texts

- **Pólya, George. *How to Solve It*. Princeton University Press, 1945.** Understand → plan → execute → look back. The Explore → Plan → Implement → Commit workflow is Pólya's sequence applied to Claude Code.
- **Brooks, Frederick P. "No Silver Bullet." *IEEE Computer* 20, no. 4 (1987): 10–19.** Essential difficulty: specification.
- **Lovelace, Ada. *Notes on the Analytical Engine* (1843), Note G.** First program: precise specification in dependency order.
- **Liskov, Barbara H. and Jeannette M. Wing. "A Behavioral Notion of Subtyping." *ACM TOPLAS* 16 (1994): 1811–1841.** Contracts.
- **Wirth, Niklaus. "Program Development by Stepwise Refinement." *CACM* 14 (1971): 221–227.** Specification as refinement.
- **Anthropic. Claude Code "Best practices" (code.claude.com/docs).** Anthropic's own published guidance on Explore → Plan → Implement → Commit and prompt structure.
- **Challen, Geoffrey. "A Day With Claude." (Ch 0).** "The challenge is getting your idea out of your own brain into a specification." The chapter's central operational claim.

### Key empirical cases

- **The teacher's first page build (TIKTOC pebble).** Course home page with syllabus structure. One page, one five-element specification, plan mode, approve, implement, verify. Author should produce.
- **Same task, two prompts.** TIKTOC's pattern: weak prompt vs. five-element specification. Same Claude; different outputs.
- **The plan-mode revision moment.** Ctrl+G to edit the plan in the teacher's text editor before approving. Concrete example of conducting at the plan stage.

---

## 2. The Core Concept — State of the Field

### What is settled

- **Specification clarity correlates with output quality.** Broad consensus in prompt-engineering literature; vendor-confirmed (Anthropic, OpenAI guides).
- **Plan mode (read-only until approved) is standard for non-trivial builds.** Anthropic's own guidance.
- **Negative constraints matter.** "Do not touch X" is not implied.
- **Feedback mechanisms in prompts dramatically improve results.** TIKTOC quotes the pattern: "give Claude a way to verify its own work" via tests or bash commands.

### What is disputed

- **The right formality.** XML-tagged structured prompts vs. natural-language paragraphs vs. hybrid. The book recommends a simple five-element format on memorability grounds.
- **Plan-mode-by-default vs. per-task.** TIKTOC implies plan-mode for non-trivial; some practitioners argue plan-mode-always. The book's position is defensible middle.
- **Examples in the prompt.** Useful for complex; overhead for routine.

### What has changed recently (last 5 years)

- The 2024–2026 generation of Claude Code handles structured prompts more reliably than 2023.
- Plan mode (Shift+Tab twice) is a 2024–2025 UI affordance. Ctrl+G to edit plans in text editor is a 2025 feature.
- Industry adoption of plan-mode-by-default for destructive operations (2024–2026).

---

## 3. Application Domain Examples

(Domain coverage map: Ch 3 sits in class website.)

For the class website's first page, the five elements:

1. **Operation:** Create a new file `src/syllabus.html` (not "add a page").
2. **Invariants:** No existing files modified. Existing CSS in `src/styles.css` not changed. The page follows the same head/nav template as `src/index.html`.
3. **Context:** CLAUDE.md sections — stack (vanilla HTML/CSS, no build step), code style (semantic HTML5), test/verification (npm run lint-html).
4. **Output format:** A complete `src/syllabus.html` rendering the course's syllabus structure (units, dates, topics). Linked from `src/index.html` in the nav.
5. **Negative constraint:** No JavaScript (the page is pure HTML/CSS). No new dependencies. No CSS changes.

Same task as one-line prompt ("add a syllabus page to my class website") produces something generic; the specification produces something that fits the project.

---

## 4. The Book's Thesis Connection

Ch 3 is the first deployable artifact. The teacher has CLAUDE.md (Ch 2); now they write specifications and the gate (Ch 4) follows.

The chapter's contribution:
1. **Specification is the bridge between intent and code.**
2. **Five elements operationalize the supervisory work** (foreshadowed; full treatment Ch 5).
3. **The first page works.** End of Ch 3 the teacher has built something deployable.

Student-supplied capacity: every element is information Claude cannot supply.

---

## 5. The AI Wayback Machine — Candidate Figures

**TIKTOC names: George Pólya (1887–1985).** Strong fit. Same recommendation as the gh-copilot teacher book Ch 3.

Candidates:
- **Pólya** — named. *How to Solve It*. Hungarian-American. Adds non-American context.
- **Lovelace** (already candidate elsewhere across the series).
- **Hopper** (Ch 4 candidate in CLI student book; avoid double-booking).

Recommendation: keep Pólya. Cross-series consistency: the gh-copilot teacher book also uses Pólya at Ch 3.

---

## 6. Pedagogical Delivery Research

### Prior knowledge required
Ch 1 (terminal session) + Ch 2 (CLAUDE.md). The teacher can run Claude with CLAUDE.md loaded.

### Common misconceptions to disarm
- **"Specifications are for big builds."** Any operation that can fail silently deserves the format.
- **"I can just edit the generated code."** Sometimes; not when the code isn't visibly wrong.
- **"Plan mode slows me down."** It saves time when the plan reveals an assumption.

### Effective instructional sequences
- **Build the first page live.** Apply-level exercise; reader follows.
- **Show the plan-mode edit moment.** Concrete: Ctrl+G, edit, approve.
- **Before/after pairs.** Multiple worked examples.

### Known failure modes
- **Specification as boilerplate.** Decisions, not form-filling.
- **Over-specification of trivial commands.** In proportion to consequence.

### What separates understanding from memorization
A reader who *understands* Ch 3 has built the first page of their class website using a five-element specification through plan mode. A reader who memorized Ch 3 can recite the five elements without producing a working spec.

---

## 7. Representation and Display Research

TIKTOC specifies two figures:

- **`<!-- → [DIAGRAM: The Explore → Plan → Implement → Commit workflow.] -->`** Four-phase linear sequence. Phase 1 (Explore): plan mode, read-only. Phase 2 (Plan): Ctrl+G to edit. Phase 3 (Implement): switch out of plan mode. Phase 4 (Commit): descriptive message. Editorial style.
- **`<!-- → [TABLE: Prompt vs. specification.] -->`** Five rows; worked example for class website.

No additional displays required.

---

## 8. Open Questions and Research Gaps

- **Dry-run alternatives for HTML/CSS builds.** Not all builds support dry-run cleanly. The chapter should give a verification protocol for static-site builds.
- **Plan-mode UX changes.** Anthropic's UI evolves; verify Ctrl+G and Shift+Tab at press.

---

## 9. Sourcing Notes

- **Pólya 1945** — Princeton.
- **Brooks 1987** — IEEE.
- **Lovelace 1843** — scholarly editions; Note G.
- **Liskov & Wing 1994** — ACM DL.
- **Wirth 1971** — open access *CACM*.
- **Anthropic Claude Code best practices** — code.claude.com/docs.
- **Challen 2026** — geoffreychallen.com.
