# Research: Chapter 2 — CLAUDE.md: Your Coding Constitution
## Claude Code for Teachers: A Practitioner's Guide

**Chapter one-line:** CLAUDE.md is the file Claude reads at the start of every session. It is the difference between a Claude that knows your project and a Claude that guesses.

**Research date:** 2026-05-21

---

## 1. Primary Sources

### Foundational papers and texts

- **Anthropic. Claude Code documentation — CLAUDE.md reference (code.claude.com/docs).** Canonical. Documents hierarchical discovery, /init, /memory, the 200-line guidance. Cite URL.
- **Knuth, Donald E. "Literate Programming." *The Computer Journal* 27, no. 2 (1984): 97–111.** CLAUDE.md as literate programming for AI collaboration.
- **Brooks, Frederick P. *The Mythical Man-Month*, ch. 6 ("Passing the Word"). Addison-Wesley, 1995.** Documentary Hypothesis — documents as substrate.
- **OpenAI. AGENTS.md documentation (developers.openai.com/codex/guides/agents-md).** The Codex equivalent. Cross-reference for the broader AI-context-file ecosystem; not the book's tool, but cite for context.
- **DESIGN.md ecosystem references (designmd.app, getdesign.md, github.com/VoltAgent/awesome-design-md).** The broader 2025–2026 design-system-as-AI-readable-spec movement. Useful for Ch 10 (three-file system) but ground here in Ch 2's general framing.

### Key empirical cases

- **The teacher's first CLAUDE.md (TIKTOC).** Five entries, under 200 lines, checked into git. Author should produce a real example for a class website project.
- **The "/init revealed something I didn't tell it" pattern.** Recurring teacher experience. /init introspects the codebase and surfaces structure the teacher wasn't tracking. The chapter's emotional anchor.
- **OpenAI's own AGENTS.md (github.com/openai/codex/blob/main/AGENTS.md).** Useful as the "what production looks like" reference, even though this book is Claude Code. Shows the genre at scale.

---

## 2. The Core Concept — State of the Field

### What is settled

- **CLAUDE.md is loaded automatically.** Anthropic's documentation is explicit. Hierarchical discovery: project-root → .claude/CLAUDE.md → user ~/.claude/CLAUDE.md → managed policy locations.
- **The 200-line guideline.** Empirically validated: bloated CLAUDE.md degrades Claude's instruction-following.
- **CLAUDE.md ≠ Skills ≠ Hooks.** Anthropic's own documentation distinguishes: CLAUDE.md is always-on; Skills are on-demand; Hooks are deterministic enforcement. The chapter's three-way distinction (full treatment in Ch 6, Ch 7) is built on this.

### What is disputed

- **Whether all CLAUDE.md content should be version-controlled.** Pro: project conventions become versioned. Con: lessons-learned and personal-style entries may not belong in team git. Recommendation: yes for the main file, with a `[private]` section in user ~/.claude/CLAUDE.md.
- **The right size of CLAUDE.md.** 200 lines is the working consensus; some teams push to 500; others stay under 100. The chapter's recommendation matches the consensus.
- **CLAUDE.md vs. Skills boundary.** Some content fits both. The book's heuristic: if it must be present in every session, CLAUDE.md; if it's only needed for a specific workflow, Skill.

### What has changed recently (last 5 years)

- The 2024–2026 wave of AI-context files (CLAUDE.md, AGENTS.md, SKILL.md, DESIGN.md ecosystems) reflects industry recognition that automatic injection beats per-prompt context. The chapter is in this lineage.
- The /init command (auto-generation of starter CLAUDE.md from codebase introspection) is a 2024–2025 feature. The chapter teaches refining /init output, not writing CLAUDE.md from scratch.
- Skills, Hooks, Subagents (2024–2026 Claude Code features) change what belongs in CLAUDE.md. The chapter must address this proactively.

---

## 3. Application Domain Examples

(Domain coverage map: Ch 2 sits in class website project.)

A class website CLAUDE.md, five entries:

1. **Stack and build:** "Static HTML/CSS/JS. No build step. Files live in `src/`; deployed via `npm run deploy` (calls `rsync` to the school server)."
2. **Code style:** "Vanilla CSS (no Tailwind, no preprocessor). Plain JS with ES modules. No bundler. Use semantic HTML5 elements; no div-soup."
3. **Test/verification:** "After any HTML change, run `npm run lint-html` (checks links, accessibility). After any CSS change, manual visual check on mobile breakpoint."
4. **Architectural decisions:** "Each page is a self-contained file. Shared components are template literals injected at build, not iframes. No JS framework."
5. **Environment quirks:** "School server uses outdated mod_rewrite — no fancy URL rewriting. All paths end in .html explicitly. Never use trailing slashes for canonical URLs."

The chapter must show the *writing* of CLAUDE.md, not just the listing. /init generates a starter; the teacher refines.

---

## 4. The Book's Thesis Connection

Ch 2 is where the discipline becomes durable. CLAUDE.md persists across sessions; the gate (foreshadowed in Ch 3, fully treated in Ch 4) is per-command.

The chapter's contribution:
1. **The artifact is the discipline made visible.** Maintained CLAUDE.md is supervisory work made into evidence.
2. **Automatic injection is the feature.** Unlike the gh-copilot CLI book's manual-paste CLI.md, Claude Code's auto-loaded CLAUDE.md means the discipline is upstream (write the file well) rather than per-invocation (remember to paste).
3. **Eventually becomes teaching artifact (Ch 13).** By Act Three, the teacher's CLAUDE.md spans three build tiers and is shareable with students.

Student-supplied capacity: the teacher knows their project's conventions, exclusions, and prior mistakes. CLAUDE.md is the form that knowledge takes.

---

## 5. The AI Wayback Machine — Candidate Figures

**TIKTOC names: Donald Knuth (born 1938).** Strong fit.

Candidates:
- **Donald Knuth** (born 1938, USA, computer scientist). Named. Literate programming. Substantive fit excellent. Diversity: white male American.
- **Margaret Hamilton** (born 1936, USA, software engineer). Apollo flight-software documentation. **Strongest diverse alternate.** Same recommendation as appears in CLI book Ch 6 and Codex book Ch 6 — series-wide Hamilton swap would unify and strengthen the diversity story.
- **Ward Cunningham** (born 1949, USA, programmer). Wiki inventor. Same diversity profile.

Recommendation: **consider Hamilton swap.** Coordinate with CLI and Codex books. Cross-series consistency would amplify the diversity contribution.

---

## 6. Pedagogical Delivery Research

### Prior knowledge required
Ch 1 first session. The teacher has run /init and seen the generated CLAUDE.md.

### Common misconceptions to disarm
- **"CLAUDE.md is for documentation."** It's for *Claude*. Written by humans, read by Claude every session.
- **"More content is better."** No. 200-line guideline. A 50-line CLAUDE.md the teacher maintains beats a 500-line one abandoned.
- **"I'll write CLAUDE.md when the project is bigger."** Now. Even the smallest project benefits.
- **"/init is enough."** /init is the starter. Refinement is the discipline.

### Effective instructional sequences
- **Run /init, then refine in the chapter.** Concrete, immediate, observable.
- **Show before-and-after Claude behavior.** Same prompt with and without the relevant CLAUDE.md entry. The contrast teaches.
- **Lessons-learned by example.** Three entries; date + mistake + fix.

### Known failure modes
- **CLAUDE.md as homework.** Frame as upstream investment.
- **Over-documented CLAUDE.md.** 200-line guideline.
- **Skipping the /memory tour.** /memory browses all CLAUDE.md files loaded. Teacher should know.

### What separates understanding from memorization
A reader who *understands* Ch 2 has written a CLAUDE.md for their class website project (refined from /init), used it across two sessions, and observed at least one specific behavior change. A reader who memorized Ch 2 can recite the five-element format without producing a tailored CLAUDE.md.

---

## 7. Representation and Display Research

TIKTOC specifies two figures:

- **`<!-- → [DIAGRAM: CLAUDE.md in the session context.] -->`** Worked content:
  - Top: session start → CLAUDE.md loaded (hierarchical).
  - Middle: every prompt operates with CLAUDE.md in context.
  - Bottom contrast row: without CLAUDE.md (Claude guesses) vs. with CLAUDE.md (Claude knows).
- **`<!-- → [TABLE: CLAUDE.md include/exclude.] -->`** Worked content:

  | Include | Exclude |
  |---|---|
  | Bash commands Claude can't guess | What Claude can figure out from code |
  | Code style deviations from norm | Standard conventions |
  | Test runners | Constantly changing state |
  | Architectural decisions | Personal notes unrelated to project |
  | Environment quirks | Secrets, credentials |

No additional displays required.

---

## 8. Open Questions and Research Gaps

- **CLAUDE.md vs. Skills boundary.** Ch 6 owns Skills; Ch 2 should establish the boundary clearly. Recommendation: "if it must be present in every session, CLAUDE.md; if it's only needed for a specific workflow, Skill."
- **Auto memory and /memory.** Auto memory accumulates learnings without the teacher writing. The chapter should mention this briefly; Ch 9 owns subagent auto memory.
- **District-managed CLAUDE.md.** Some schools may want district-level CLAUDE.md policies. Brief sidebar; full treatment is out of scope.
- **Hamilton vs. Knuth swap.** Cross-series decision.

---

## 9. Sourcing Notes

- **Anthropic Claude Code docs** — code.claude.com/docs. Stable; verify at press.
- **Knuth 1984** — open access *Computer Journal*.
- **Brooks 1995** — anniversary edition.
- **OpenAI AGENTS.md docs** — developers.openai.com/codex/guides/agents-md.
- **OpenAI Codex repo AGENTS.md** — github.com/openai/codex/blob/main/AGENTS.md.
- **Hamilton sources** if swapping: NASA Apollo archive; McMillan 2015 *Wired* piece.
