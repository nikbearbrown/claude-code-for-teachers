# Research: Chapter 10 — The Three-File System: Intent, Constitution, State
## Claude Code for Teachers: A Practitioner's Guide

**Chapter one-line:** Before Claude writes a single line of the simulation, three files define everything. The Intent Layer is human, always. The Technical Constitution governs what Claude never improvises. The Project State tracks what is built and what is pending.

**Research date:** 2026-05-21

---

## 1. Primary Sources

### Foundational papers and texts

- **Mies van der Rohe, Ludwig. "Less is more" (attributed; from multiple lectures and writings 1920s–1960s).** Architectural philosophy: the structural frame defines what is built without determining every detail. The three-file system as architectural design. **Note: this attribution is more aphoristic than precisely sourced; the chapter should use Mies as an evocative reference, not as a primary citation.**
- **Mies van der Rohe lecture transcripts and the *Mies van der Rohe Centennial Exhibition* catalog (MoMA, 1986).** Better-sourced material on Mies's design philosophy. Use for citations.
- **Alexander, Christopher. *A Pattern Language*. Oxford, 1977.** Patterns as nested constraints — the system that constrains what's built within a clear boundary.
- **Bear Brown, Nik. *Brutalist Design System*. brutalist.art.** The book's central operational reference for the three-file system. **Author's own work; the chapter should be transparent about this.**
- **DESIGN.md ecosystem references.** designmd.app, getdesign.md, github.com/VoltAgent/awesome-design-md. The broader 2025–2026 ecosystem; brutalist three-file is one entrant.
- **LeWitt, Sol. "Sentences on Conceptual Art" (1969).** The author who holds the intent and writes the instruction is the author. Foundational for the Intent Layer concept.

### Key empirical cases

- **The teacher's "build me a sorting simulator" failure (TIKTOC opening).** Types one-line prompt. Claude builds something. Works. Color scheme not the teacher's. Interaction model not what the teacher had in mind. Pedagogical scaffolding missing. The teacher didn't draw the line before Claude started.
- **The teacher's first three files (TIKTOC).** CLAUDE.md, DESIGN.md, PROJECT.md, all populated before Claude sees the project. Author should produce real examples.
- **The 45-minute scope test.** TIKTOC's apply-level exercise: if the three files take more than 45 minutes, the scope is too large. Concrete forcing function.

---

## 2. The Core Concept — State of the Field

### What is settled

- **AI-context files improve generated output quality.** Established broadly in 2024–2026 practitioner literature.
- **Separating intent, constitution, and state reduces drift.** Established in software architecture (Alexander) and design (LeWitt, Mies).
- **Brutalist three-file system is one operational choice among several in the 2025–2026 ecosystem.** designmd.app catalogs 454 design systems; the book teaches the Brutalist version.

### What is disputed

- **Whether three files is right vs. fewer or more.** Some practitioners use two (CLAUDE.md + DESIGN.md without PROJECT.md). Others use four+ (adding SKILL.md as a fourth file). The book commits to three; defensible.
- **Whether the Intent Layer should be entirely off-limits to Claude.** TIKTOC's position: yes, "never overwritten by Claude." Some practitioners argue Claude should be able to *suggest* Intent revisions for human review. The book's stronger position prevents drift; defensible.
- **The 200-line limit for each file.** CLAUDE.md limit (200 lines) is documented; DESIGN.md and PROJECT.md aren't bound similarly. The book extends the guidance; reasonable.

### What has changed recently (last 5 years)

- The 2024–2026 DESIGN.md ecosystem (designmd.app, awesome-design-md) is institutional support for the chapter's argument.
- 2026 Claude Code features (Skills with frontmatter, Subagents with frontmatter) interact with the three-file system in ways that didn't exist in 2024. Brief sidebar.

---

## 3. Application Domain Examples

(Domain coverage map: Ch 10 sits in interactive simulation.)

For a sorting-algorithm simulation, the three files:

**CLAUDE.md (Technical Constitution):**
- Stack: vanilla HTML/CSS/JS; no framework; single-file deployable.
- File structure: `index.html`, `simulation.css`, `simulation.js`; no other top-level files.
- Naming: kebab-case for IDs; camelCase for JS functions.
- Never touch without instruction: any file outside the simulation directory; the class website's shared CSS.
- Verification: opens cleanly in Chromium without console errors; works on mobile breakpoint.

**DESIGN.md (Visual Constitution):**
- Color system (six variables max — no others):
  - `--background: #f5f5f0` (warm white)
  - `--ink: #1a1a1a` (near-black)
  - `--accent: #c97a3a` (terracotta — for the element being compared)
  - `--target: #3a7ac9` (blue — for the element being placed)
  - `--rule: #999999` (medium gray — for axis lines)
  - `--highlight: #f0d843` (amber — for the sorted region)
- Typography: monospace for numeric values, sans-serif for labels. No serif. No script.
- Interaction vocabulary: single click to step forward; long click to step backward; keyboard arrows for fine control. **Never:** drag-and-drop, hover-only states, hidden controls.
- Accessibility: keyboard-navigable; screen-reader-friendly with descriptive labels; minimum 16px font.

**PROJECT.md (Project State):**

Layer 1 — Intent (human, never overwritten):
- What this simulation is: an interactive visualization of bubble sort showing why it's O(n²).
- What the student should understand after using it: that comparison-based sorts have a tradeoff between simplicity and efficiency; that small changes (one early swap) can have cascading effects.
- What questions it answers: "How does bubble sort work?"; "Why is it slow?"; "What happens when the input is already sorted?"
- What questions it refuses to answer: "Which sort is best?" (too context-dependent); "Why is quicksort faster?" (different simulation).
- Tone: matter-of-fact, slightly playful; no jargon; no condescension.

Layer 2 — Technical State (AI layer):
- What is built: HTML scaffold; CSS variables defined.
- What is pending: JS simulation logic; step controls; keyboard handling.
- Generation log: [will populate during build].
- Open technical questions: how to handle large input sizes without performance degradation.

---

## 4. The Book's Thesis Connection

Ch 10 opens Act Three by making the design work explicit before any generation begins. The chapter's claim: most simulation failures are intent failures that surfaced as technical or aesthetic problems downstream.

The chapter's contribution:
1. **Names the design work.** Distinct from prompt-writing.
2. **Three files = three concerns separated.** Technical, visual, intent. Each protected from the others.
3. **The Brutalist governing principle.** Maximally informed, minimally autonomous, by design.
4. **45-minute scope test.** If you can't write the three files in 45 minutes, the simulation is too large for a first build.

Student-supplied capacity: the Intent Layer is irreducibly the teacher's. Only the teacher knows what their students need to understand.

---

## 5. The AI Wayback Machine — Candidate Figures

**TIKTOC names: Mies van der Rohe (1886–1969).** Substantive fit moderate.

Candidates:
- **Mies van der Rohe** (1886–1969, Germany/USA, architect). Named. "Less is more"; structural frame. Diversity: white male German-American — adds non-USA. **Substantive fit is more aphoristic than precise.**
- **Eileen Gray** (1878–1976, Ireland/France, architect/designer). Total design — every element planned from materials to interaction. **Strongest diverse alternate.** Woman, Irish-French.
- **Lina Bo Bardi** (1914–1992, Italy/Brazil, architect). Functional design with explicit social purpose. Diversity: Italian-Brazilian.
- **Sol LeWitt** (1928–2007, USA, conceptual artist). The author who holds the intent. Direct fit for the Intent Layer concept. White male American.

Recommendation: **consider Eileen Gray.** Her total-design approach (E-1027 villa, designed every interior element) maps onto the three-file system more precisely than Mies's aphoristic philosophy. Adds woman + non-USA. Mies remains evocative but Gray fits substantively better.

---

## 6. Pedagogical Delivery Research

### Prior knowledge required
Act One framework + Act Two (Skills, Hooks, Subagents).

### Common misconceptions to disarm
- **"Three files is too much for a small simulation."** No. 45-minute test forces appropriate scope.
- **"DESIGN.md is for designers."** No. Anyone building anything with visual output needs design decisions.
- **"Claude can figure out the Intent Layer."** No. Intent is irreducibly human.
- **"I'll iterate on the files as I build."** No. Write them first; refine later if needed. Iteration during generation is forward correction, which TIKTOC's Ch 4 warns against.

### Effective instructional sequences
- **Write the three files for a teacher's simulation.** Apply-level exercise.
- **The 45-minute test.** Concrete forcing function.
- **Show all three files for a worked example.** TIKTOC's sorting-algorithm simulation is the natural fit.
- **brutalist.art transparency.** The chapter cites the author's own design system. Reader should know.

### Known failure modes
- **The chapter as Brutalist evangelism.** Teach the principles; let readers adopt.
- **brutalist.art as authority.** Author should be honest about authorship.
- **DESIGN.md fetishism.** Six color variables is a constraint, not a religion. The point is the *boundary*, not the specific number.

### What separates understanding from memorization
A reader who *understands* Ch 10 has written three files for their own simulation in under 45 minutes, can identify which file each decision belongs to, and recognizes that the Intent Layer requires their pedagogical judgment. A reader who memorized Ch 10 can recite the three-file structure without producing usable files.

---

## 7. Representation and Display Research

TIKTOC specifies two figures:

- **`<!-- → [DIAGRAM: The three-file system as concentric circles or nested boxes.] -->`** Worked content:
  - Outer: CLAUDE.md (Technical Constitution).
  - Middle: DESIGN.md (Visual Constitution).
  - Inner: PROJECT.md (Project State — Intent Layer is human, always).
  - Editorial style.

- **`<!-- → [TABLE: Three-file system — file name, what it contains, who writes it, when it changes.] -->`** Worked content:

  | File | Contents | Who writes | When it changes |
  |---|---|---|---|
  | CLAUDE.md | Technical constitution — stack, conventions, file structure, what Claude never touches | Teacher (refined from /init) | Tech stack changes |
  | DESIGN.md | Visual constitution — color, typography, interaction vocabulary, accessibility | Teacher | Design system changes |
  | PROJECT.md | Project state — Intent Layer (human) + Technical State (AI) | Teacher writes Layer 1; Claude updates Layer 2 | Per-project; intent rarely, technical-state per session |

---

## 8. Open Questions and Research Gaps

- **brutalist.art transparency.** The chapter cites the author's own design system. Be honest about authorship; position within the broader DESIGN.md ecosystem (designmd.app etc.).
- **Eileen Gray vs. Mies van der Rohe.** Recommended swap; author's call.
- **Simulation domain (TIKTOC OQ-1).** Most acute at Ch 10. Author + CS teacher advisory must lock before drafting. Sorting algorithms is the chapter's working example; the book's actual simulation could be different.
- **Three-file vs. four-file (with SKILL.md).** Some practitioners add SKILL.md as a fourth. The book commits to three; defensible.

---

## 9. Sourcing Notes

- **Mies van der Rohe attribution** — careful with "less is more"; the phrase is widely attributed but precisely sourced citations are few. Use the MoMA centennial catalog (1986) or specific lecture transcripts.
- **Alexander 1977** — Oxford.
- **brutalist.art** — author's own.
- **DESIGN.md ecosystem** — designmd.app, getdesign.md.
- **LeWitt 1969** — open access via 0–9 archives.
- **Eileen Gray sources** if swapping: Adam, *Eileen Gray: Her Life and Her Work* (1987); the Pompidou's *Eileen Gray* exhibition catalog (2013).
