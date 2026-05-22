# Research: Chapter 9 — Subagents: Keeping the Build Clean
## Claude Code for Teachers: A Practitioner's Guide

**Chapter one-line:** A subagent is a Claude session that runs in its own context and reports back a summary. When your grading tool research starts filling the session with file reads, delegate the research. Keep the main build clean.

**Research date:** 2026-05-21

---

## 1. Primary Sources

### Foundational papers and texts

- **Anthropic. "Claude Code Subagents" documentation (code.claude.com/docs).** Canonical. Subagent format (Markdown + YAML frontmatter); location (`.claude/agents/` project; `~/.claude/agents/` personal); allowed tools, system prompt configuration. Cite URL.
- **Simon, Herbert A. *The Sciences of the Artificial*, ch. 7 ("The Architecture of Complexity"). MIT Press, 1996.** "Nearly decomposable systems": large problems broken into subsystems solvable independently. The subagent is Simon's nearly decomposable subsystem.
- **Simon, Herbert A. "The Architecture of Complexity." *Proceedings of the American Philosophical Society* 106, no. 6 (1962): 467–482.** Original paper. Open access.
- **Hutchins, Edwin. *Cognition in the Wild*. MIT Press, 1995.** Distributed cognition; offloading subtasks to external workers. The subagent is a cognitive offload.
- **2026 practitioner guides on Claude Code subagents** (ofox.ai, boringbot, trensee). Practitioner examples.

### Key empirical cases

- **The teacher's "session is slowing down" moment (TIKTOC opening).** Grading-tool session is filling with research that isn't part of the build. Context window degrading. Subagent is the answer.
- **The pattern-analysis subagent (TIKTOC worked example).** Reads all submissions; identifies common misconceptions; returns a structured report. Main session stays clean.
- **The Writer/Reviewer pattern.** One Claude session implements; subagent reviews from clean context with no bias toward the code it didn't write. Strong 2026 practitioner pattern.

---

## 2. The Core Concept — State of the Field

### What is settled

- **Subagents exist as a Claude Code feature.** Anthropic-documented. Markdown + YAML frontmatter in `.claude/agents/`.
- **Isolated context.** Subagent runs in its own context window; only the summary returns. Confirmed by Anthropic and 2026 practitioner guides.
- **Allowed tools and system prompt configurable per subagent.** Useful for specialization.
- **Subagents vs. Skills.** Skills are content Claude loads (same context window); Subagents are workers that run separately. Anthropic-distinguished.

### What is disputed

- **When to use a subagent vs. /clear vs. /compact.** Practitioner consensus is evolving. Recommendation: subagent for tasks with clear input/output and isolated context need; /clear for fresh start; /compact for keeping current context with focus.
- **Whether to use auto-memory across subagent sessions.** Subagents can maintain their own auto memory. Useful for recurring research; risk of stale context.
- **The Writer/Reviewer pattern.** Some practitioners argue the bias-isolation benefit is overstated (the subagent shares the same model). The book's position: even same-model, clean-context review catches what same-context review misses. Defensible.

### What has changed recently (last 5 years)

- Subagents were introduced in Claude Code 2024–2025; the 2026 generation includes the Writer/Reviewer pattern and frontmatter-based hooks-in-subagents.
- Auto memory (Claude accumulates learnings without explicit teacher writing) is a 2025–2026 feature. Subagents can maintain their own.
- Agent teams (multiple subagents coordinated by a main agent) are emerging 2026 patterns. The book sidesteps this complexity — single subagents are enough for student-scale builds.

---

## 3. Application Domain Examples

(Domain coverage map: Ch 9 sits in grading tool.)

For the grading tool, three subagent uses:

1. **Pattern-analysis subagent.** Reads all submissions; identifies common misconceptions; returns structured report. Main session never sees the per-submission reads.
2. **Research subagent for late-submission policy.** Investigates how to handle late submissions across the school's existing tools. Returns findings only, not the files read.
3. **Writer/Reviewer pattern for the grading-tool code.** Main session writes the tool; a reviewer subagent reads the final code from clean context, identifies issues the writer missed.

Configuration in `.claude/agents/pattern-analyzer.md`:

```markdown
---
name: pattern-analyzer
description: Analyze student submissions for common misconceptions; return structured report
tools: Read, Grep, Glob
---

You analyze student submissions for patterns. Read all files under the path specified. Return a structured report:
1. Top 5 common misconceptions (with example excerpts).
2. Outliers (submissions that don't match the cohort patterns).
3. Coverage statistics (how many submissions exhibit each pattern).

Do NOT write feedback. Do NOT generate grades. Return only the pattern report.
```

The teacher invokes via the main session; the subagent runs; the report returns. Main context unchanged.

---

## 4. The Book's Thesis Connection

Ch 9 closes Act Two. The teacher has a working grading tool with skills (Ch 6), hooks (Ch 7), and now subagents for context management. They've experienced the dangerous middle (Ch 8) and narrowed scope appropriately.

The chapter's contribution:
1. **Context management as discipline.** Subagents protect the main build from research bloat.
2. **The Writer/Reviewer pattern.** Independent review without the implementer's biases.
3. **Closes Gate 2.** The teacher has the full Act Two framework and is ready for Act Three.

Student-supplied capacity: deciding *what* to delegate to a subagent. The scoping decision is the teacher's.

---

## 5. The AI Wayback Machine — Candidate Figures

**TIKTOC names: Herbert Simon (1916–2001).** Strong fit.

Candidates:
- **Herbert Simon** (1916–2001, USA, polymath). Named. "Architecture of Complexity"; nearly decomposable systems. Substantive fit excellent. Diversity: white male American.
- **Allen Newell** (1927–1992, USA, CS). Co-author with Simon on cognitive architecture. Same diversity profile.
- **Carl Hewitt** (born 1944, USA, CS). Actor model — independent agents communicating through messages. Substantive fit moderate-strong. Same diversity profile.

Recommendation: keep Simon. Decomposition is the precise frame.

---

## 6. Pedagogical Delivery Research

### Prior knowledge required
Ch 6 (Skills) + Ch 7 (Hooks). The teacher has built Skills and Hooks; subagents are the third extensibility layer.

### Common misconceptions to disarm
- **"Subagent = another Claude tab."** No. The subagent runs from the main session; only the summary returns.
- **"Subagents are for complex builds only."** Even a single grading-tool session benefits.
- **"More subagents = better."** No. Each adds configuration overhead. Use subagents for tasks that meet the criteria (clear input/output, would otherwise bloat context).
- **"The Writer/Reviewer pattern is overkill."** For high-stakes code (grading-tool blocking grade generation), it's defensible.

### Effective instructional sequences
- **Build the pattern-analysis subagent live.** Apply-level exercise; teacher follows.
- **Show before/after context.** Same task with inline research vs. subagent. Observable difference in context growth.
- **The Writer/Reviewer demo.** Concrete: writer subagent implements; reviewer subagent reads from clean context; comparison.

### Known failure modes
- **Subagent chapter as power-user lecture.** Keep teacher-accessible.
- **Over-specifying subagent system prompts.** Brief, clear, well-scoped.
- **Stale auto memory.** Brief mention; full treatment requires deeper agentic-systems knowledge.

### What separates understanding from memorization
A reader who *understands* Ch 9 has built a pattern-analysis subagent for their grading tool and used the Writer/Reviewer pattern at least once. A reader who memorized Ch 9 can describe subagents without configuring one.

---

## 7. Representation and Display Research

TIKTOC specifies one figure:

- **`<!-- → [DIAGRAM: Main session vs. subagent.] -->`** Worked content:
  - Main session: context filling with build history, file reads, research.
  - Subagent: isolated context; reads many files; returns summary only.
  - Arrows showing summary return.
  - Editorial style.

No additional displays required.

---

## 8. Open Questions and Research Gaps

- **Auto memory across subagent sessions.** Useful but stale-context risk. Brief sidebar.
- **Agent teams.** 2026 emerging pattern. Out of scope; mention briefly.
- **Subagent security considerations.** Each subagent can have its own tool permissions; the teacher should review.
- **Gate 2 acceptance criteria.** TIKTOC names Gate 2 at end of Ch 9. The chapter must end with a concrete checklist: working grading tool + skills + hooks + subagents + experienced dangerous middle + narrowed scope.

---

## 9. Sourcing Notes

- **Anthropic Claude Code Subagents docs** — code.claude.com/docs.
- **Simon 1996** — MIT Press; 3rd ed.
- **Simon 1962** — open access via APS archives.
- **Hutchins 1995** — MIT Press.
- **2026 practitioner guides** — ofox.ai, boringbot, trensee.
