# Research: Chapter 1 — Your First Terminal Session: Claude Code Is Not ChatGPT
## Claude Code for Teachers: A Practitioner's Guide

**Chapter one-line:** Claude Code runs in your terminal, reads your files, runs commands, and works autonomously. That autonomy is the feature — and the reason you need a discipline before you start.

**Research date:** 2026-05-21

---

## 1. Primary Sources

### Foundational papers and texts

- **Anthropic. "Claude Code" documentation (code.claude.com).** Canonical reference. Installation, agentic loop, permission modes, /init, /clear, /rewind, /context. Cite URL.
- **Anthropic. "Claude Code: Hooks, Subagents, Skills" and "Best practices" (code.claude.com/docs).** Same source; useful for the chapter's specific commands.
- **Kay, Alan. "A Personal Computer for Children of All Ages." Xerox PARC, 1972.** "Computer as medium for exploration, not just execution." The questions-before-code rule is Kay's stance applied. The chapter's intellectual ancestor.
- **Brooks, Frederick P. *The Mythical Man-Month*, ch. 6 ("Passing the Word"). Addison-Wesley, 1995.** Context-as-substrate. Useful for the chapter's argument that what the terminal "knows" lives in CLAUDE.md, not in the model.
- **Anthropic RCT (canonical citation in CLI/Codex student books).** Engagement patterns matter. Foreshadowed here; full treatment elsewhere.

### Key empirical cases

- **The teacher's first session (TIKTOC opening).** Opens terminal with Claude Code; Claude reads project directory, proposes structure, starts making files; teacher watches. Different from chatbot. Author should preserve.
- **The "I asked five questions before making any change" pattern.** TIKTOC's "questions before code" rule operationalized. Concrete first-session walkthrough.
- **The /init-generated CLAUDE.md.** First artifact the teacher sees. TIKTOC's exercise. The contrast: what Claude noticed vs. what the teacher hadn't told it.

---

## 2. The Core Concept — State of the Field

### What is settled

- **Claude Code is agentic, not chat.** File access, terminal access, autonomous multi-step execution. Documented by Anthropic.
- **The context window is the primary resource.** Established in LLM literature; Anthropic-confirmed for Claude Code specifically. Performance degrades as it fills.
- **Questions-before-code reduces error rate.** Established practitioner pattern, validated by Challen's "specification is the work" frame.

### What is disputed

- **Whether plan mode should be default for student/teacher builds.** TIKTOC implies yes for most builds; some practitioners argue plan-mode-always is overhead. The book's position is defensible: for first sessions and high-stakes operations, plan mode; for routine, no.
- **Whether installation is a barrier the chapter can really mitigate.** TIKTOC names this as adoption risk #1. The chapter includes complete walkthrough; whether that's enough varies by reader.

### What has changed recently (last 5 years)

- Claude Code introduced (2024–2025) and matured rapidly. The 2026 generation supports plan mode, /rewind, /compact, Skills, Hooks, Subagents — none of which existed in early Claude Code.
- Industry adoption of plan-mode-by-default for destructive operations (2024–2026) supports the chapter's discipline.

---

## 3. Application Domain Examples

(Domain coverage map: Ch 1 sits in class website foundation.)

- **First session: questions about a class website folder.** Teacher asks Claude what it sees. Claude lists files, identifies the framework, notices the existing structure. Teacher reads. No changes.
- **First session: read the /init CLAUDE.md.** Teacher runs /init. Claude generates a starter CLAUDE.md based on the codebase. Teacher reads what Claude noticed.
- **First session: plan mode for adding a page.** Teacher enters plan mode (Shift+Tab twice). Asks Claude to propose adding a new page. Reads the plan. Doesn't approve. Notes assumptions Claude made.

---

## 4. The Book's Thesis Connection

Ch 1 puts hands on the terminal with the discipline already in place. The chapter must:

1. **Establish the agentic-loop reality.** Claude Code is different from Claude.ai. The chapter must make this concrete.
2. **Install context-window awareness.** The single most important resource. Foreshadows Ch 6 (Skills), Ch 7 (Hooks), Ch 9 (Subagents) which all manage context.
3. **Make questions-before-code a habit from minute one.** Not aspirational; default. The first session demonstrates the discipline.

Student-supplied capacity: the teacher's *judgment* about which generated suggestions match their actual project. Claude cannot know.

---

## 5. The AI Wayback Machine — Candidate Figures

**TIKTOC names: Alan Kay (born 1940).** Excellent fit.

Candidates:
- **Alan Kay** (born 1940, USA, computer scientist). Named. Dynabook. Substantive fit excellent — "computer as medium for exploration" is the questions-before-code rule. Diversity: white male American.
- **Adele Goldberg** (born 1945, USA, computer scientist). Co-developer with Kay of Smalltalk. **Strongest diverse alternate.** Woman, American.
- **Seymour Papert** (1928–2016, South African/USA). Already TIKTOC's Bridge candidate; avoid double-booking.

Recommendation: keep Kay. Goldberg works if rebalancing demands.

---

## 6. Pedagogical Delivery Research

### Prior knowledge required
The reader can open a terminal and run `ls`. The chapter takes them from there.

### Common misconceptions to disarm
- **"Claude Code is like Claude.ai."** No.
- **"I'll skip questions-before-code; I know what I want."** No. The first session is for calibration, not execution.
- **"Installation problems mean this book isn't for me."** Friction, not exclusion.

### Effective instructional sequences
- **Installation walkthrough, exact commands.** `npm install -g @anthropic-ai/claude-code`; `claude` in project dir; `/init`. Plus troubleshooting sidebar.
- **First session: questions only.** Concrete; teacher experiences calibration before making changes.
- **Plan-mode demonstration.** Teacher enters plan mode; sees what Claude would do; doesn't approve. Teaches the gate by example.

### Known failure modes
- **Installation chapter as gatekeeper.** Over-resource installation help.
- **First-session demo that fails.** Test the chapter's commands against current Claude Code before press.
- **"My school IT won't allow this."** Real problem; reference Appendix on access (OQ-3).

### What separates understanding from memorization
A reader who *understands* Ch 1 has run their first Claude Code session, asked five questions before making any changes, and read the /init-generated CLAUDE.md. A reader who memorized Ch 1 can recite "questions before code" without having done it.

---

## 7. Representation and Display Research

TIKTOC specifies one figure:

- **`<!-- → [DIAGRAM: The agentic loop.] -->`** Worked content:
  - Three-phase cycle: Gather context → Take action → Verify results → [repeat].
  - Human interruption point marked at each phase.
  - Editorial style. No color.

No additional displays required.

---

## 8. Open Questions and Research Gaps

- **Claude Code installation success rates across school environments.** Anecdotal evidence plenty; published measurement thin. Author may want to pilot with three teachers in different IT environments.
- **Plan mode's appropriate scope.** Always? For first sessions only? For destructive ops? The chapter should give a clear heuristic.
- **The /init CLAUDE.md quality.** /init's output quality varies by codebase. Author may want a worked example showing a good /init output and a thin one, with how to improve.

---

## 9. Sourcing Notes

- **Anthropic Claude Code docs** — code.claude.com. URL stable; reverify at press.
- **Kay 1972** — Xerox PARC TR; multiple republications.
- **Brooks 1995** — anniversary edition.
- **Challen 2026 talk** — geoffreychallen.com.
