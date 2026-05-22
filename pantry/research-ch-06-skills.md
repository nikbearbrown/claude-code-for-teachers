# Research: Chapter 6 — Skills: Build Once, Use Every Semester
## Claude Code for Teachers: A Practitioner's Guide

**Chapter one-line:** A Skill is a CLAUDE.md file for a specific task — a lesson plan generator, a rubric builder, a grading workflow. Build it once. Invoke it with /skill-name every semester.

**Research date:** 2026-05-21

---

## 1. Primary Sources

### Foundational papers and texts

- **Anthropic. "Claude Code Skills" documentation (code.claude.com/docs).** Canonical. SKILL.md format; .claude/skills/<name>/ location; `/skill-name` invocation; `disable-model-invocation: true` flag; context-cost model (description loads at session start, full content on use). Cite URL.
- **Babbage, Charles. *Passages from the Life of a Philosopher* (1864) and on the Analytical Engine.** Subroutines: stored operations re-executable without re-specification. The Skill is a Babbage subroutine.
- **Knuth, Donald E. *The Art of Computer Programming*, Vol. 1: Fundamental Algorithms. Addison-Wesley, 1968.** Procedure abstraction. Skills are procedures the teacher can invoke by name.
- **Reusman ("ofox.ai"). "Claude Code: Hooks, Subagents, and Skills — Complete Guide" (2026, ofox.ai/blog/claude-code-hooks-subagents-skills-complete-guide-2026/).** Practitioner-side overview. Useful for examples that aren't in Anthropic's official docs.
- **The Education Agent Skills Library (152 evidence-based teaching skills across 19 learning-science domains, MCP tools).** TIKTOC references this. Author should verify provenance — TIKTOC names it but I haven't found a direct citation.

### Key empirical cases

- **The teacher's first two skills (TIKTOC).** Lesson-plan-generator and grading-workflow. Both invoked, verified, checked into git for next semester. Author should produce real SKILL.md files.
- **The "I wrote the same workflow specification three times" pattern.** TIKTOC opening. Recurring teacher experience that motivates Skills.
- **The Anthropic Education Report's "educators building custom tools" finding.** Skills are the operational form of teacher-as-tool-builder.

---

## 2. The Core Concept — State of the Field

### What is settled

- **Skills exist as a Claude Code feature.** Confirmed Anthropic docs and 2026 practitioner guides.
- **Skills load on demand; CLAUDE.md loads every session.** Anthropic-documented distinction.
- **Context cost matters.** Skill descriptions add small cost at session start; full content costs only when invoked. The model documented by Anthropic.
- **disable-model-invocation: true** is a real flag that hides a skill from auto-invocation. Useful for skills with side effects.

### What is disputed

- **CLAUDE.md vs. Skill boundary.** Some content fits both. Heuristic: every-session content → CLAUDE.md; workflow-specific → Skill.
- **Whether to share skills across projects.** Symlinks vs. duplication. Author recommends symlinks for team contexts; duplication for personal projects.
- **The right size for a Skill.** Some practitioners argue large SKILL.md is fine because it loads only on invocation; others argue brevity per usability. Recommendation: under 200 lines (same as CLAUDE.md guidance).

### What has changed recently (last 5 years)

- Skills are a 2024–2025 Claude Code feature; the format and behavior have stabilized in 2026.
- The 2026 generation supports hooks-in-skills (frontmatter-defined hooks scoped to skill activation) — newer feature, may be worth a sidebar mention. Confirmed in 2026 practitioner docs.
- The Education Agent Skills Library (if real) is a 2025–2026 community effort. Author should verify current status.

---

## 3. Application Domain Examples

(Domain coverage map: Ch 6 sits in grading tool.)

The teacher's grading-workflow skill, SKILL.md format:

```markdown
---
name: grading-workflow
description: Process a batch of student submissions; flag patterns; never generate final grades
disable-model-invocation: false
---

## Workflow
1. Read submissions from `submissions/<assignment>/` (one directory per student).
2. For each submission, check presence of required sections (rubric in `rubric.md`).
3. Run pattern detection across all submissions: missing docstrings, common misconceptions, code-style outliers.
4. Output a per-student flagging report (NOT graded feedback) to `grading/flags/<student>.md`.
5. Output a cohort pattern report to `grading/patterns.md`.

## Never
- Generate a final letter or numeric grade.
- Write feedback that addresses the student directly.
- Modify files in `submissions/`.

## Verification
- After running, count: should produce one flag report per student + one pattern report.
- The cohort pattern report should name at least three patterns, not just count occurrences.
```

The teacher invokes with `/grading-workflow` and Claude follows. The skill is checked into git. Next semester: invoke again; the workflow is the same.

The lesson-plan-generator skill follows similar structure for a different workflow.

---

## 4. The Book's Thesis Connection

Ch 6 is the chapter where the discipline becomes *reusable*. CLAUDE.md (Ch 2) and the gate + handoff conditions (Ch 3–4) are foundational; Skills are how the teacher captures the workflow for next semester.

The chapter's contribution:
1. **Skills make discipline portable across semesters.** The teacher's lessons-learned in semester 1 become semester 2's starting point.
2. **The boundary against generated content.** Skills can include explicit prohibitions (never generate final grade) that travel with the workflow.
3. **The teacher-as-tool-builder thesis.** Skills are the operational form. The teacher who has built and shared a skill has done something Claude can't — designed the workflow.

Student-supplied capacity: the workflow design. Which patterns to flag, what counts as a missing section, what the cohort report should highlight — all teacher knowledge.

---

## 5. The AI Wayback Machine — Candidate Figures

**TIKTOC names: Charles Babbage (1791–1871).** Strong fit.

Candidates:
- **Charles Babbage** (1791–1871, UK, mathematician). Named. Analytical Engine subroutines. The Skill is a Babbage subroutine. Substantive fit excellent. Diversity: white male British — adds non-USA.
- **Ada Lovelace** (1815–1852, UK, mathematician). Babbage's collaborator; Note G is the first subroutine specification. **Strongest diverse alternate.** Already a candidate in CLI/Codex student books Ch 8; using her here would create cross-series resonance.
- **John Backus** (1924–2007, USA, computer scientist). FORTRAN; turning operations into named, reusable subroutines at compiler level. Same broad diversity profile.

Recommendation: keep Babbage. Lovelace at Ch 6 would create cross-book continuity but Babbage is more specifically about the subroutine concept the chapter operationalizes.

---

## 6. Pedagogical Delivery Research

### Prior knowledge required
Ch 2 (CLAUDE.md) + Ch 5 (capacities). The teacher understands the distinction between persistent context and on-demand workflow.

### Common misconceptions to disarm
- **"Skills are just longer prompts."** No. Skills are stored, reusable, invokable by name.
- **"Everything that's reusable should be a Skill."** No. CLAUDE.md vs. Skill boundary matters.
- **"Skills are for power users."** TIKTOC's Ch 6 makes the case for teacher-relevant skills (lesson plan, rubric, grading workflow, differentiation, feedback). Accessible.

### Effective instructional sequences
- **Build two skills live.** Apply-level exercise. Lesson-plan-generator first (lower stakes), grading-workflow second (with the "never generate final grade" prohibition).
- **Show invocation.** `/skill-name` in the terminal. Concrete.
- **The teacher skill catalog.** TIKTOC's table — six skills the teacher likely needs.

### Known failure modes
- **Skills as homework.** Frame as next-semester time-saver.
- **Over-engineered first skills.** Start small; iterate.
- **The skill that drifts.** Skills must be maintained. Updating after the first use is the discipline.

### What separates understanding from memorization
A reader who *understands* Ch 6 has built a lesson-plan-generator skill and a grading-workflow skill, invoked both, refined both based on first use, and checked both into git. A reader who memorized Ch 6 can describe the SKILL.md format without producing usable skills.

---

## 7. Representation and Display Research

TIKTOC specifies two figures:

- **`<!-- → [DIAGRAM: Skills vs. CLAUDE.md vs. Hooks.] -->`** Worked content:
  - Three columns.
  - CLAUDE.md: loads every session; always-on; advisory.
  - Skills: loads on demand; invoked by /name or auto-judgment; reusable workflow.
  - Hooks: runs on lifecycle events; deterministic; enforcement (Ch 7).

- **`<!-- → [TABLE: Teacher skill catalog.] -->`** Worked content (six rows):

  | Skill | What it does | When to invoke | disable-model-invocation |
  |---|---|---|---|
  | lesson-plan-generator | Produce a draft lesson plan from learning objectives | Planning week | false |
  | rubric-builder | Generate a draft rubric from assignment description | Assignment design | false |
  | grading-workflow | Flag patterns across submissions; produce per-student flags | Grading day | false |
  | differentiation-helper | Suggest differentiation for a lesson plan | Lesson refinement | false |
  | feedback-generator | Draft feedback for a single submission (first draft only) | Grading | true (side effect — explicit invoke only) |
  | exit-ticket | Generate an exit-ticket prompt | End of lesson | false |

No additional displays required.

---

## 8. Open Questions and Research Gaps

- **The Education Agent Skills Library.** TIKTOC references "152 evidence-based teaching skills across 19 learning-science domains, MCP tools." Author should verify provenance and link. If real and current, this is a strong adoption asset.
- **CLAUDE.md vs. Skill heuristic.** Author should give 3–5 concrete examples of content that belongs in one vs. the other.
- **Hooks-in-skills.** 2026 feature: hooks can be defined in skill frontmatter, scoped to skill activation. Brief sidebar mention; full hooks treatment Ch 7.
- **Sharing skills across schools / districts.** Open. The book's primary reader is individual teacher; school/district sharing is future-edition.

---

## 9. Sourcing Notes

- **Anthropic Claude Code Skills docs** — code.claude.com/docs.
- **Babbage 1864** — *Passages from the Life of a Philosopher*; modern Cambridge reprint (1994).
- **Knuth 1968** — Addison-Wesley.
- **Practitioner guides** — ofox.ai, boringbot, trensee 2026. Useful for examples; not for empirical claims.
- **Education Agent Skills Library** — verify before press.
