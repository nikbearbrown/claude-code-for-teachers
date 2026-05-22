# Research: Chapter 7 — Hooks: The Enforcement Layer
## Claude Code for Teachers: A Practitioner's Guide

**Chapter one-line:** A CLAUDE.md instruction that says "never generate a final grade" is a request. A Hook that blocks grade generation is enforcement. This is the chapter where "do not" becomes "cannot."

**Research date:** 2026-05-21

---

## 1. Primary Sources

### Foundational papers and texts

- **Anthropic. "Claude Code Hooks reference" (code.claude.com/docs/en/hooks).** Canonical. Hook events (PreToolUse, PostToolUse, SessionStart, SessionEnd, UserPromptSubmit — 25 lifecycle points total per 2026 docs). Hook types (shell command, HTTP request, LLM prompt, subagent). Configuration in `.claude/settings.json`. The `/hooks` command. Cite URL.
- **Shannon, Claude E. "A Symbolic Analysis of Relay and Switching Circuits." MIT MS thesis, 1937 / *Trans. AIEE* 57 (1938): 713–723.** Logic gates: physical mechanisms that enforce boolean conditions regardless of context. Hooks are Shannon gates for Claude Code.
- **Shannon, Claude E. "A Mathematical Theory of Communication." *Bell System Technical Journal* 27 (1948): 379–423, 623–656.** Information theory foundation; cite for context.
- **Reason, James. *Human Error*. Cambridge University Press, 1990.** Defense-in-depth; Swiss-cheese model. Hooks are a deterministic defense layer.
- **Deming, W. Edwards. *Out of the Crisis*, ch. 1. MIT Press, 1986.** "A bad system will beat a good person every time." The chapter's argument for enforcement over advisory.
- **2026 practitioner guides on Claude Code hooks** (ofox.ai, developersdigest, dev.to/vibehackers). Practitioner-side examples beyond Anthropic's docs.

### Key empirical cases

- **The teacher's "I told Claude not to generate a final grade and it did anyway" moment (TIKTOC opening).** CLAUDE.md instruction is advisory. Claude follows context, training, and instruction probabilistically. The chapter explains why and what to do.
- **The grade-generation block hook.** TIKTOC's worked example. PreToolUse hook intercepts any write where the content matches a numeric-grade regex; blocks the write.
- **The verification-after-edit hook.** PostToolUse hook runs a verification script after every file edit. Catches regressions immediately.
- **The session-logging hook.** SessionEnd hook logs what Claude touched. Useful for classroom oversight.

---

## 2. The Core Concept — State of the Field

### What is settled

- **Hooks exist as a Claude Code feature with 25 lifecycle points** as of 2026 docs (TIKTOC says "PreToolUse, PostToolUse, SessionStart, SessionEnd" — these are a subset).
- **Hooks are deterministic; CLAUDE.md is advisory.** Anthropic-documented.
- **Hook types: shell command, HTTP request, LLM prompt, subagent.** Anthropic-documented.
- **Configuration in `.claude/settings.json`.** Anthropic-documented.
- **`/hooks` command browses configured hooks.** Anthropic-documented.
- **Context cost: zero unless the hook returns output.** Anthropic-documented; useful for the chapter's "why hooks are nearly free" framing.
- **PreToolUse is the primary security checkpoint.** Practitioner consensus (2026 guides).

### What is disputed

- **Whether all CLAUDE.md "never X" rules should be hooks.** TIKTOC takes a strong position: if a rule must hold every time, it is a Hook, not a CLAUDE.md instruction. Some practitioners argue advisory rules are sufficient for low-stakes; hooks for high-stakes. The book's stronger position is defensible because the grading-tool stakes are real.
- **Whether teachers can write hooks themselves.** TIKTOC's adoption-risk #4 names Hooks chapter as needing a contributor with Claude Code production experience. The chapter's pedagogy depends on this — if hooks feel out-of-reach to teachers, the chapter's argument collapses.
- **Whether Claude can write hooks for the teacher.** Yes — "Write a hook that blocks any output containing a numeric grade." This is the chapter's accessibility lever.

### What has changed recently (last 5 years)

- Hooks were introduced in Claude Code 2024–2025; the 25-lifecycle-points expansion is 2026.
- 2026 feature: hooks can be defined in skill or subagent frontmatter, scoped to that component's lifecycle (newer; worth a sidebar mention).
- Industry adoption of hook-based enforcement in agentic systems (2024–2026) supports the chapter's argument.

---

## 3. Application Domain Examples

(Domain coverage map: Ch 7 sits in grading tool.)

For the grading tool, three hooks:

1. **PreToolUse hook: block final grade generation.** Triggers before any Write tool use. Inspects the content for patterns matching a numeric grade ("85%", "A-", "5/5", etc.). If matched, blocks the write and returns an error to Claude: "Refusing to write final grade. Use the flag-pattern workflow instead."

2. **PostToolUse hook: run verification.** Triggers after any Edit tool use. Runs `npm run lint` or equivalent. If the verification fails, blocks the next step and returns the failure to Claude: "Verification failed: {error}. Revert or fix before continuing."

3. **SessionEnd hook: log what Claude touched.** Triggers at session end. Logs file paths modified, tools used, total tokens. Useful for the teacher's classroom oversight record.

Writing each hook by asking Claude: "Write a PreToolUse hook in `.claude/hooks/block-grades.sh` that blocks any Write where the content matches a numeric grade pattern." Claude writes the hook; the teacher reviews; commits.

---

## 4. The Book's Thesis Connection

Ch 7 is the chapter where the conducting discipline becomes deterministic for the highest-stakes operations. CLAUDE.md (Ch 2) advises; Skills (Ch 6) make workflows reusable; Hooks enforce.

The chapter's contribution:
1. **"Do not" becomes "cannot."** For rules that must hold every time, the chapter operationalizes the enforcement.
2. **The enforcement hierarchy.** CLAUDE.md → Skills → Hooks. Three tiers, three roles. The chapter makes the architecture visible.
3. **Teacher accessibility.** Hooks feel intimidating; the chapter must show teachers can write hooks by asking Claude. The accessibility lever.

Student-supplied capacity: deciding *which* rules must hold every time vs. which can be advisory. The teacher's judgment about the project's stakes.

---

## 5. The AI Wayback Machine — Candidate Figures

**TIKTOC names: Claude Shannon (1916–2001).** Excellent fit.

Candidates:
- **Claude Shannon** (1916–2001, USA, mathematician/engineer). Named. Logic gates, information theory. Substantive fit excellent — Shannon's gates enforce booleans regardless of context. Diversity: white male American.
- **Hedy Lamarr** (1914–2000, Austria/USA, actress/inventor). Frequency-hopping spread spectrum. Diversity: woman, Austrian-American. Substantive fit moderate (signal processing rather than enforcement).
- **Grace Hopper** (1906–1992, USA). Compiler-enforced correctness. Diversity: woman, American. Could substitute but used elsewhere in the series.

Recommendation: keep Shannon. Logic-gate parallel is too clean to swap.

---

## 6. Pedagogical Delivery Research

### Prior knowledge required
Ch 2 (CLAUDE.md) + Ch 6 (Skills). The teacher understands advisory vs. reusable, and is ready for deterministic.

### Common misconceptions to disarm
- **"CLAUDE.md is enough."** No. Claude follows context probabilistically; for must-hold rules, advisory fails.
- **"Hooks are for power users."** With "ask Claude to write the hook" pattern, hooks are accessible to teachers.
- **"More hooks = better."** No. Each hook adds maintenance load. Use hooks for must-hold rules; advisory for nice-to-have.
- **"Hooks prevent all bad behavior."** TIKTOC's Contested Claims: overstated. Hooks are deterministic for the events they cover; Claude can still act outside hook events.

### Effective instructional sequences
- **Build three hooks live.** Apply-level exercise. Block grade generation; run verification; log session.
- **"Ask Claude to write the hook" demo.** Concrete: teacher types the request, Claude writes the hook, teacher reviews, commits.
- **The enforcement hierarchy diagram.** Three tiers visible.
- **The "I told CLAUDE.md and it ignored me" case.** Reader recognizes; chapter explains.

### Known failure modes
- **Hooks chapter as engineering-class.** Keep teacher-accessible. "Ask Claude" pattern is the discipline.
- **Over-promising hook coverage.** Be precise about what hooks can and can't enforce.
- **Skipping the contributor recruit (TIKTOC OR#4).** The chapter needs a contributor with production Claude Code experience. Don't draft from docs alone.

### What separates understanding from memorization
A reader who *understands* Ch 7 has written three hooks (asked Claude to draft, then reviewed and committed) for their grading tool, and has tested at least one by deliberately asking Claude to do the prohibited action. A reader who memorized Ch 7 can recite "PreToolUse / PostToolUse / SessionStart / SessionEnd" without applying.

---

## 7. Representation and Display Research

TIKTOC specifies two figures:

- **`<!-- → [DIAGRAM: The enforcement hierarchy.] -->`** Three tiers, labeled:
  - CLAUDE.md: advisory — Claude reads and tries to follow.
  - Skills: on-demand — loaded when invoked.
  - Hooks: deterministic — runs regardless of what Claude decides.

- **`<!-- → [TABLE: CLAUDE.md instruction vs. Hook.] -->`** Five examples:

  | Rule | CLAUDE.md instruction | Equivalent Hook |
  |---|---|---|
  | Grade generation block | "Never generate a final grade" | PreToolUse hook matching numeric-grade pattern in Write |
  | CSS isolation | "Don't change CSS when editing HTML" | PreToolUse hook blocking Edit on `*.css` during HTML tasks |
  | File protection | "Never touch `submissions/`" | PreToolUse hook denying Write/Edit under `submissions/` |
  | Verification run | "Run lint after every edit" | PostToolUse hook running lint script |
  | Session logging | "Log what you touched" | SessionEnd hook writing audit log |

---

## 8. Open Questions and Research Gaps

- **Contributor recruit (TIKTOC OR#4).** Critical. The chapter requires a contributor with production Claude Code hook experience. Don't draft from docs alone.
- **2026 hook expansion.** 25 lifecycle points; hooks-in-skills/subagents. Verify against current docs before press.
- **Hook security implications.** A shell-command hook can execute arbitrary code. The chapter must address: only run hooks you've reviewed; commit hooks to git.
- **District-IT considerations.** Some districts may restrict hook configuration. Brief sidebar; full treatment in appendix.

---

## 9. Sourcing Notes

- **Anthropic Claude Code Hooks reference** — code.claude.com/docs/en/hooks.
- **Shannon 1937 / 1938** — MIT MS thesis / *Trans. AIEE*.
- **Shannon 1948** — *Bell System Technical Journal*; open access.
- **Reason 1990** — Cambridge.
- **Deming 1986** — MIT Press.
- **2026 practitioner guides** — ofox.ai, developersdigest, dev.to/vibehackers. Cite as practitioner sources; not empirical authority.
