# claude-code-for-teachers-a-practitioners-guide
## Full TOC Draft — All Phase Outputs Compiled

**Working title:** Claude Code for Teachers: A Practitioner's Guide
**Series:** Practitioner Guides for the AI Classroom · Bear Brown & Company
**Author:** Humanitarians AI · bear@bearbrown.co · Bear Brown, LLC
**Practitioner voice:** Seth Brown
**Document:** Full TOC Draft — compiled from all phase outputs
**Version:** 1.0
**Status:** Pre-production — terminal build domain to be confirmed
(see OQ-1)

---

## Document structure

1. Book Concept and Thesis
2. Learner Profile
3. Book Type and Deployment Specification
4. Field Positioning
5. Three-Act Learning Arc
6. Prerequisite Map
7. Build Arc and Terminal Deliverables
8. Chapter-by-Chapter TOC
9. Chapter Anatomy Template
10. Case Study Strategy
11. Hard Topics, Contested Claims, Aging Risk
12. Market Positioning
13. Feature List
14. Out of Scope
15. Adoption Risk Register
16. Open Questions

---

# PART 1 — BOOK CONCEPT AND THESIS

## Book concept summary

> This book teaches **K-12 CS teachers to conduct Claude Code through
> real classroom builds** — a class website, a grading tool, an
> interactive simulation — **and then to teach that same discipline
> to their students**, using the conducting framework they just
> practiced on their own work. It fills the gap left by generic AI
> tools-for-teachers resources (which teach teachers to use Claude
> as a faster lesson-plan generator) and developer-facing Claude
> Code courses (which target engineers, not educators). It succeeds
> when **the teacher can sit next to a student who is mid-build and
> say exactly where the line is, because they have drawn it
> themselves**.

**One-sentence logline:**
The teacher who builds with Claude Code and the teacher who teaches
students to build with Claude Code are the same person practicing
the same discipline — you cannot teach the line until you have
drawn it yourself.

## Central thesis

"This book argues that the teacher-as-builder and the teacher-as-
instructor are the same discipline applied twice — that a K-12 CS
teacher who conducts Claude Code through their own classroom builds
using explicit handoff conditions, CLAUDE.md, skills, and hooks is
practicing exactly the discipline they are trying to instill in
their students, and this matters because a teacher who has never
drawn the line cannot teach it."

## Thesis test

The TOC reflects the thesis at every act:

- ACT ONE: The teacher builds their first class website page using
  the conducting discipline, then designs a classroom activity using
  the same concept. Building and teaching in the same chapter. ✓
- ACT TWO: The teacher builds a grading tool — higher stakes, every
  supervisory capacity exercised, skills and hooks introduced —
  and designs classroom activities at each step. ✓
- ACT THREE: The teacher builds an interactive classroom simulation
  and deploys it in their actual classroom. The build serves the
  students. The discipline is demonstrated, not described. ✓

**Thesis test: PASS**

---

# PART 2 — LEARNER PROFILE

## Primary reader

A K-12 CS teacher, 2026. Ten-plus years in the classroom. Three
to four years teaching CS. Experienced educator, early in their
CS journey. Has tried Claude for lesson plans. Watches students
use AI in ways that make them uneasy but has no operational
language for what to do instead. Tired and committed simultaneously.
Has 30 minutes on Monday night.

**CSTA 2025 data portrait:** 74% of CS teachers have 10+ years
of classroom experience. Only 26% have taught CS for 10+ years.
96% participated in professional development in the past year.
Almost half did fewer than 11 hours of PD. The book's reader
is experienced, committed, undersupported, and hungry for
operational guidance that respects their experience.

## Prior knowledge assumed

- Claude.ai for lesson planning and basic prompting
- Google Classroom or similar LMS
- Some coding experience (enough to have been hired as a
  CS teacher — not necessarily deep)
- Comfortable running a terminal command if given exact syntax

## Prior knowledge NOT assumed

- Claude Code in the terminal
- CLAUDE.md, Skills, Hooks, Subagents
- The five supervisory capacities by name
- The Boondoggling framework
- Software Design Documents
- The students book (assumed available and assignable;
  not assumed read)

## Prior misconceptions

1. "Claude Code is just a better version of Claude.ai" —
   it is an agentic system with file access, terminal access,
   and autonomous multi-step execution; the autonomy requires
   a different discipline
2. "I need to be a developer to use Claude Code" — the
   teacher-as-builder pattern requires specification writing
   and verification, not deep coding ability
3. "AI for teachers means faster lesson plans" — the book
   teaches AI for teachers as a build discipline, not a
   content generation shortcut
4. "My students know more than me, so I can't teach this" —
   the teacher who has built with Claude Code knows something
   the technically fluent student does not: what the discipline
   costs when skipped

## Motivation type

**Primary:** Professional — the teacher needs tools that work
in their actual classroom on Tuesday.
**Secondary:** Intellectual — the teacher who has watched the
homework/quiz gap in their own class wants the repair kit.
**Not primary:** Prestige or publication — this is a practitioner
handbook, not a research contribution.

## Prerequisite map

| Prerequisite | Safe to assume? | If not: where addressed |
|---|---|---|
| Basic Claude prompting | Yes | — |
| Terminal basics | Probably | Ch 1 first session walkthrough |
| Claude Code installed | No | Ch 1 installation |
| CLAUDE.md concept | No | Ch 2 (full chapter) |
| Skills concept | No | Ch 6 (full chapter) |
| Hooks concept | No | Ch 7 (full chapter) |
| Subagents concept | No | Ch 9 (full chapter) |
| Five supervisory capacities | No | Ch 5 (full chapter) |
| Students book concepts | No | Referenced; not required |

**Front-loading decision:** Terminal installation and first
session walkthrough are addressed in Chapter 1 as primary
instruction. The dictation shortcut (Mac OS System Settings →
Accessibility → Dictation; double-tap to speak; Windows: Win+H)
is introduced here for time-pressed teachers. No prerequisite
chapter required.

---

# PART 3 — BOOK TYPE AND DEPLOYMENT SPECIFICATION

## Book type

**PRIMARY TYPE:** Practitioner handbook with course-textbook
bones. The teacher reads it cover to cover once, then consults
it chapter by chapter during builds and classroom activity design.

**NOT:** A course textbook for students; a developer productivity
guide; a theoretical AI education framework.

## Deployment specification

**Primary adoption context:**
Self-directed K-12 CS teacher finding it through professional
development, CSTA community, or the teachers book's own
recommendation ecosystem. The Iowa State AI High School Teachers
Summer Program (3-week university course) is a natural adoption
channel, not a competitor.

**Secondary adoption context:**
University teacher training programs and CS education PD providers
who need a practitioner text with real builds.

**Tertiary adoption context:**
District-level AI professional development programs that need
a handbook rather than a workshop deck.

**Companion relationship:**
`claude-code-for-students-a-practitioners-guide` ($1 Kindle) is
the student companion. The teachers book references it explicitly
throughout. Teachers can assign it without a budget conversation.
Chapter 13 maps the students book to classroom activities.

**What the book is NOT designed for:**
Generic AI ethics PD; teachers who want to ban AI use; university
CS education research seminars; developer audiences.

**How the TOC signals book type:**
Three acts, three build tiers, interleaved structure (every chapter
applies the concept in both directions simultaneously), terminal
deliverable deployed in the teacher's actual classroom. A PD
coordinator reviewing this TOC knows immediately what a teacher
will have built by the end.

---

# PART 4 — FIELD POSITIONING

## The positioning statement — consolidated

The competitive landscape has a clean gap:

- AI-for-teachers resources (Teach For All, Anthropic Education
  Report, "50 AI tools for teachers" genre) teach teachers to use
  Claude as a faster lesson-plan generator. This book teaches
  teachers to conduct Claude Code through real builds.
- Developer-facing Claude Code courses (Vanderbilt/Coursera,
  AI Hero) target engineers. This book targets educators.
- University summer programs (Iowa State, CodePath) are
  institutional. This book is the Monday-morning resource.
- The arxiv research (cc-self-train, Challenge/Unlock, Architor)
  is for researchers. This book gives the same discipline in
  plain language for the practitioner.
- No practitioner handbook yet exists for the K-12 CS teacher
  who is both builder and instructor.

## Positioning statements by comparable

**vs. Anthropic Education Report / Teach For All:**
"Unlike AI-for-teachers programs, which teach educators to
generate content with Claude, this book teaches K-12 CS teachers
to conduct Claude Code through real classroom builds — class
websites, grading tools, interactive simulations — using the same
phase-gate discipline that prevents the most common AI-assisted
development failures."

**vs. Vanderbilt/Coursera Claude Code:**
"Unlike the Vanderbilt Claude Code course, which teaches developers
to delegate like a tech lead, this book teaches CS teachers to
conduct like a composer — building their own classroom tools and
teaching students to do the same in the same chapter."

**vs. the students book in this series:**
"This book is the teacher's half of a two-book pair. The students
book teaches the conducting discipline to students. This book
teaches the same discipline to the teachers who assign it — and
adds the classroom activity design that makes the students book
teachable."

## Research validation

The CSTA 2025 CS Teacher Landscape report provides the market
portrait: experienced educators, early in CS journey, wanting
more than 11 hours of PD per year.

The Anthropic Education Report (August 2025) documents that
educators are already building custom tools, not just generating
lesson plans — validating the teacher-as-builder thesis.

Geoffrey Challen's "A Day With Claude" (January 2026) provides
the closest practitioner account: a teacher who uses Claude Code
to build his own course tools and adapted his CS curriculum around
AI coding agents. His "the challenge is getting your idea out of
your own brain into a specification" is the /v0 gate discovered
independently.

---

# PART 5 — THREE-ACT LEARNING ARC

## The arc statement

This book takes the K-12 CS teacher from **their first terminal
command** to **deploying an interactive classroom simulation they
built themselves** — first by establishing the conducting discipline
on a low-stakes class website, then by practicing it on a grading
tool that immediately saves them time, then by applying it at full
complexity to build something their students learn from directly.

## The interleaved structure

Every chapter covers one conducting concept and applies it in both
directions simultaneously: the teacher's own build, then a
classroom activity using the same concept. The teacher who reads
a chapter on handoff conditions and immediately applies it in both
directions never has to translate the concept. They finish every
chapter already knowing how to teach it, because they just did both.

## The pebble-in-the-pond opening

Chapter 1 gives the teacher their first terminal session: they
ask questions about a project folder before touching anything.
This establishes the explore-first discipline at the lowest
possible stakes. The pebble: one web page built with explicit
handoff conditions in Chapter 3. Everything that follows expands
the pond.

## Act One — Establish (Chapters 0–4)

**Starting state:** The teacher has Claude for lesson plans but
no terminal discipline. They don't have the language for what
they're watching happen with their students.
**Ending state:** The teacher has built one deployable web page
using CLAUDE.md, specification prompts, and explicit handoff
conditions. They have designed one classroom activity using
the same concept.
**Inciting question:** "If I've drawn the line on my own build,
can I teach my students where it is?"
**Transition condition:** The teacher has completed a small
deployable build with explicit handoff conditions and designed
one classroom activity using the same concept. They are ready
for a build that costs something if it goes wrong.

## Act Two — Build (Chapters 5–9)

**Starting state:** The teacher has the basic discipline but
has not applied it to a high-stakes build.
**Ending state:** The teacher has a working grading tool with
human-in-the-loop enforcement (hooks), reusable skills, and
a subagent for context-clean research. They have designed
classroom activities at every step.
**Hardest moment:** Chapter 8 — the dangerous middle in a
grading tool. Claude produces feedback that passes every
handoff condition and is still pedagogically wrong. The Act
Two crisis.
**Transition condition:** The teacher has experienced a dangerous
middle moment on a build that mattered. They know what the
discipline costs to skip. They are ready to build for students,
not just for themselves.

## Bridge chapter

Seth's voice. The moment his builds stopped being about
productivity and started being about what he could make that
didn't exist before. The teacher who just built a grading tool
needs this moment before taking on a harder build.

## Act Three — Apply (Chapters 10–14)

**Starting state:** The teacher has the full conducting discipline
but has not applied it to a build that serves students directly.
**Ending state:** The teacher has deployed an interactive classroom
simulation they built themselves, watched students use it, and
conducted a revision build based on what they observed.
**Terminal deliverable:** The simulation deployed in the teacher's
actual classroom, with a post-build document and a classroom
activity where students use it as the starting point for their
own build.

## Seth's arc across the book

Seth opens the book as the practitioner who has done what
the teacher is about to do. He is retrospective, specific,
and honest about what was hard. His voice closes at the bridge
chapter — he hands the build to the teacher. The final chapter
belongs to the teacher.

---

# PART 6 — PREREQUISITE MAP

## Prerequisite chain by chapter

| Chapter | Prerequisites | Load-bearing? |
|---|---|---|
| Ch 0 (Introduction) | None | No |
| Ch 1 (First Terminal Session) | None | Yes — establishes agentic loop |
| Ch 2 (CLAUDE.md) | Ch 1 | Yes — governs all subsequent builds |
| Ch 3 (Specifications) | Ch 1–2 | Yes — five-element format used throughout |
| Ch 4 (Handoff Conditions) | Ch 3 | Yes — gate between all build steps |
| Ch 5 (Five Capacities) | Ch 1–4 | Yes — labels used in all subsequent chapters |
| Ch 6 (Skills) | Ch 2, Ch 5 | No — additive to CLAUDE.md |
| Ch 7 (Hooks) | Ch 2, Ch 6 | No — enforcement layer |
| Ch 8 (Dangerous Middle) | Ch 3–7 | No — crisis chapter |
| Ch 9 (Subagents) | Ch 5–6 | No — context management |
| Bridge | Ch 5–9 | No — motivational transition |
| Ch 10 (Three-File System) | Ch 2, Ch 3 | Yes — governs simulation build |
| Ch 11 (Simulation Build) | Ch 10, Ch 5 | Yes — full build arc |
| Ch 12 (Deploying in Class) | Ch 11 | No — deployment and revision |
| Ch 13 (Teaching the Discipline) | All prior | No — synthesis |
| Ch 14 (Post-Build Document) | All prior | No — terminal deliverable |

## The students book prerequisite

The teachers book references the students book throughout but
does not require the teacher to have read it. Chapter 13 maps
the students book explicitly. The assumption: the teacher has
assigned it or will assign it. At $1 Kindle, assigning it is
a one-sentence classroom decision.

---

# PART 7 — BUILD ARC AND TERMINAL DELIVERABLES

## The three build tiers

Every build tier has a parallel classroom activity track.
The interleaved structure means both tracks run simultaneously.

| Tier | Chapters | Teacher builds | Classroom activity | Terminal artifact |
|---|---|---|---|---|
| Foundations | 1–4 | Class website (one page) | Observation and specification exercises | One deployable web page |
| Core | 5–9 | Grading tool | Rubric and feedback tool activities | Working grading tool with hooks |
| Application | 10–14 | Interactive simulation | Simulation-based learning activities | Simulation deployed in class |

## Terminal deliverable specification

**The interactive classroom simulation, deployed:**

Required components for the teacher:
1. Three governing files complete before build begins:
   CLAUDE.md (technical constitution), DESIGN.md (visual
   constitution), PROJECT.md (intent layer + technical state)
2. Build execution log (specification per step, handoff
   condition evaluation, supervisory capacity label)
3. Student-facing verification pass (does a student who has
   never seen this know what to do in the first 30 seconds?)
4. Revision build based on classroom observation
5. Post-build document (five sections)

**Post-build document — five sections:**
1. What I built (one paragraph, plain language)
2. What I delegated to Claude and why
3. What I kept for myself and why
4. What I learned that I didn't know before
5. What I would do differently

**Classroom activity terminal deliverable:**
One classroom activity designed around the simulation that
puts students in the conducting role — where they must draw
the line themselves.

## Chapter exercise structure

Every chapter has three required components:
1. Teacher build component (applying the concept to the
   current build tier)
2. Classroom activity design component (applying the same
   concept to a student-facing activity)
3. One assessable exercise connecting both

Bloom's distribution across the full book:
- Understand/Apply: Ch 1–4 (conducting basics)
- Apply/Analyze: Ch 5–9 (supervisory capacities, skills, hooks)
- Analyze/Evaluate: Ch 8, 13 (dangerous middle, teaching synthesis)
- Create: Ch 10–14 (simulation build and deployment)

---

# PART 8 — CHAPTER-BY-CHAPTER TOC

---

## ACT ONE — ESTABLISH
*Chapters 0–4: The conducting discipline on a class website*

---

### Chapter 0 — Introduction: The Line

**One-line:** There is a line between what Claude executes and
what only you can do. This book teaches you to draw it — by
building real things, then teaching students to draw it
themselves.

**Learning outcomes:**
1. (Understand) Explain the difference between prompting Claude
   and conducting a build with Claude.
2. (Understand) Describe what the interleaved structure means
   for how to read this book.
3. (Remember) Identify the three builds that form the book's arc.

**Opening:** Seth, eighteen months after the students book. Not
explaining the homework/quiz gap anymore. Describing the first
time he built something real with Claude Code and understood why
the discipline matters from the inside. The teacher meets him
here — not as a student to manage, but as someone who has done
what the teacher is about to do.

<!-- → [DIAGRAM: The book's arc as three build tiers on a
timeline. Tier 1: class website (Act One). Tier 2: grading tool
(Act Two). Tier 3: interactive simulation (Act Three). Each tier
labeled with the conducting concept it introduces. Editorial
style. No color.] -->

**Core content:**
- What Seth learned that the students book couldn't teach him
- The two tracks running through every chapter: your build,
  your classroom
- How to use the students book alongside this one
- What the teacher will have built and taught by Chapter 14
- Dictation shortcut: Mac OS System Settings → Accessibility
  → Dictation (double-tap to speak); Windows: Win+H. The
  teacher who has 30 minutes on Monday night benefits from
  not typing every specification.

**Assessable exercises:**
1. (Remember) Name the three builds in this book's arc and
   the conducting concept each one introduces.
2. (Understand) What is the difference between a teacher who
   uses Claude to generate lesson plans and a teacher who
   conducts Claude through a classroom build? One paragraph.
3. (Understand) Read the first chapter of the students book.
   Name one concept Seth learns that you will teach using
   your own build experience.

**Wayback Machine:** 🕰️ **John Dewey** (1859–1952) — philosopher
of education who argued that the teacher learns by teaching —
that the act of making the discipline explicit for students
deepens the teacher's own understanding. His concept of
"reflective practice" is the interleaved structure in
theoretical form.

**Bridge:** The reader knows the arc. Chapter 1 puts them in
the terminal for the first time.

---

### Chapter 1 — Your First Terminal Session: Claude Code Is Not ChatGPT

**One-line:** Claude Code runs in your terminal, reads your files,
runs commands, and works autonomously. That autonomy is the
feature — and the reason you need a discipline before you start.

**Learning outcomes:**
1. (Understand) Explain the agentic loop and how it differs from
   a chatbot conversation.
2. (Apply) Install Claude Code and run a first session in a
   project directory.
3. (Understand) Explain the context window constraint and why
   it is the primary resource to manage.

**Opening:** The teacher opens their terminal for the first time
with Claude Code running. Claude reads their project directory,
proposes a structure, starts making files. The teacher watches.
Something about this feels different from the chatbot.

<!-- → [DIAGRAM: The agentic loop — three phases in a cycle:
Gather context → Take action → Verify results → [repeat].
Human interruption point marked at each phase. Editorial
style. No color.] -->

**Core content:**
- The agentic loop: gather context, take action, verify results
- Why Claude Code differs from Claude.ai: file access, terminal
  access, autonomous multi-step execution
- The context window: why it fills fast, why performance
  degrades as it fills — the single most important resource
- Permission modes: default (asks before changes), plan mode
  (read-only until approved), auto mode
- Questions before code: the most important rule. Before your
  first build session, spend time asking Claude questions about
  the project folder. Ask what it sees. Ask it to describe the
  structure. Do not ask it to build anything. This teaches
  you the boundary — what it can one-shot vs. what needs
  precise instruction.
- Installation: `npm install -g @anthropic-ai/claude-code`,
  run `claude` in a project directory, run `/init` to generate
  a starter CLAUDE.md
- /clear between unrelated tasks; /rewind to restore previous
  state; Esc to stop Claude mid-action

**Teacher build:** The teacher runs their first session in a
folder they will use for the class website. They ask five
questions about what Claude sees. They make no changes.
They read the /init-generated CLAUDE.md.

**Classroom activity:** Students run their first Claude Code
session on a provided starter project, ask three codebase
questions, and document what Claude told them — without making
any changes. Observation before action.

**Assessable exercises:**
1. (Apply) Install Claude Code. Run /init in a project folder.
   Read the generated CLAUDE.md. What did Claude notice that
   you didn't tell it?
2. (Analyze) Run Claude in plan mode. Ask it to propose a plan
   for adding a new page to your class website. Read the plan.
   Do not approve it yet. What assumptions did Claude make
   that you need to correct?
3. (Evaluate) What is the single most important resource to
   manage in a Claude Code session? Why does it matter more
   than prompt quality?

**Links:** [code.claude.com](https://code.claude.com)

**Wayback Machine:** 🕰️ **Alan Kay** (born 1940) — computer
scientist who designed the first object-oriented programming
language and argued that "the best way to predict the future
is to invent it." His concept of the Dynabook — a personal
computer as an instrument for learning, not just a tool for
executing pre-specified tasks — is the intellectual ancestor
of Claude Code as a learning environment rather than an
answer machine.

**Bridge:** The reader has been in the terminal. Chapter 2
gives them the file that makes every subsequent session smarter.

---

### Chapter 2 — CLAUDE.md: Your Coding Constitution

**One-line:** CLAUDE.md is the file Claude reads at the start
of every session. It is the difference between a Claude that
knows your project and a Claude that guesses.

**Learning outcomes:**
1. (Understand) Explain what CLAUDE.md is, where it lives,
   and when Claude reads it.
2. (Apply) Write a CLAUDE.md for a classroom build project
   using the five-element format.
3. (Analyze) Distinguish CLAUDE.md content (always-on rules)
   from Skills (on-demand) and Hooks (enforcement).

**Opening:** The teacher starts their second Claude Code session.
Claude has no memory of the first one. The teacher types the
same context they typed yesterday. This chapter ends that.

<!-- → [DIAGRAM: CLAUDE.md in the session context — loaded at
session start, persists across the session, governs every
prompt. Contrast: without CLAUDE.md (Claude guesses) vs. with
CLAUDE.md (Claude knows). Editorial style.] -->

**Core content:**
- What CLAUDE.md is: markdown file read at every session start
- Where it lives: project root, .claude/CLAUDE.md, user
  ~/.claude/CLAUDE.md, managed policy location for districts
- The five-element format: bash commands Claude can't guess,
  code style deviations, test runners, architectural decisions,
  environment quirks
- What NOT to include: anything Claude can figure out from code,
  standard conventions, anything that changes frequently
- The 200-line rule: bloated CLAUDE.md causes Claude to ignore
  the actual instructions
- CLAUDE.md vs Skills vs Hooks: advisory vs. on-demand vs.
  enforcement (full treatment in Ch 6 and Ch 7)
- /init generates a starter; refine it; check into git
- The /memory command: browse and edit all CLAUDE.md files
  loaded in the current session

<!-- → [TABLE: CLAUDE.md include/exclude — two columns. Include:
bash commands, code style deviations, test runners, architectural
decisions, quirks. Exclude: what Claude can figure out, standard
conventions, changing content. No color.] -->

**Teacher build:** The teacher writes their first CLAUDE.md
for the class website project. Five entries. Under 200 lines.
Checked into git.

**Classroom activity:** Students write a CLAUDE.md for a
provided starter project. Class discussion: what did different
students include? What happened when they ran Claude with and
without it?

**Assessable exercises:**
1. (Apply) Write a CLAUDE.md for your class website project.
   Run /init first, then refine. Keep it under 200 lines.
2. (Analyze) Run Claude without your CLAUDE.md, then with it,
   on the same task. Document three specific differences.
3. (Evaluate) After one week of use: which entries is Claude
   ignoring? Why? Fix one.

**Wayback Machine:** 🕰️ **Donald Knuth** (born 1938) — computer
scientist who created TeX and invented literate programming:
the practice of writing the explanation of a program alongside
the code, so that the human reader and the machine reader are
served simultaneously. CLAUDE.md is literate programming applied
to AI collaboration — the human writes the context so both the
human and the AI can navigate the project.

**Bridge:** The reader has a CLAUDE.md. Chapter 3 teaches them
to write Claude prompts that are specifications, not requests.

---

### Chapter 3 — From Prompts to Specifications: The First Build

**One-line:** "Add a page to my class website" is a request.
A specification names the file, the structure, what it must
not touch, and what done looks like. The class website is the
first build.

**Learning outcomes:**
1. (Apply) Write a five-element specification prompt for a
   Claude Code task.
2. (Apply) Execute a build step using Explore → Plan → Approve
   → Implement → Commit.
3. (Analyze) Identify the difference between a prompt that
   delegates and a specification that conducts.

**Opening:** The pebble. The teacher builds their first page —
not the whole site, one page — using a specification prompt.
It works. They understand exactly why.

<!-- → [DIAGRAM: The Explore → Plan → Implement → Commit workflow.
Four phases in a linear sequence. Phase 1 (Explore): plan mode,
read-only. Phase 2 (Plan): Ctrl+G to edit plan in text editor.
Phase 3 (Implement): switch out of plan mode. Phase 4 (Commit):
descriptive commit message. Editorial style.] -->

**Core content:**
- The five elements of a specification prompt:
  1. The specific task (the one thing)
  2. The invariants (what must not change)
  3. The context (CLAUDE.md sections governing this step)
  4. The output format (what done looks like)
  5. The negative constraint (what Claude must not do)
- The Explore → Plan → Implement → Commit workflow
- Plan mode: Claude reads files without making changes;
  Ctrl+G to edit the plan in your text editor before approving
- Why Claude has no memory between sessions: every specification
  must contain the constraints that govern it
- Give Claude a way to verify its own work: whenever possible,
  include a test or a bash command Claude can run to check
  output before reporting done

<!-- → [TABLE: Prompt vs. specification — two-column comparison.
Five rows showing the same task described as a request (left)
and a specification (right). No color.] -->

**Teacher build:** The teacher builds the first page of their
class website — a course home page with their syllabus structure.
One page, one five-element specification, plan mode, approve,
implement, verify.

**Classroom activity:** Students build their first page using
the five-element format. Peer review: did each student's
specification contain all five elements? What happened when
one was missing?

**Assessable exercises:**
1. (Apply) Write a five-element specification for the next
   page of your class website. Run it in plan mode. Edit the
   plan before approving.
2. (Analyze) Compare your specification to a vague prompt
   covering the same task. What did Claude do differently?
3. (Create) Design a classroom activity that teaches the
   five-element format without using the word "specification."

**Wayback Machine:** 🕰️ **George Pólya** (1887–1985) —
mathematician whose *How to Solve It* (1945) formalized the
problem-solving process as a sequence of explicit steps:
understand the problem, devise a plan, carry out the plan,
look back. The five-element specification format is Pólya's
problem-solving sequence applied to Claude Code prompting.

**Bridge:** The reader has built a page. Chapter 4 names the
gate between build steps: the handoff condition.

---

### Chapter 4 — Handoff Conditions: The Gate Between Steps

**One-line:** Not "looks good." A specific, testable condition
that must be true before the next step begins. This is what
separates conducting from approving.

**Learning outcomes:**
1. (Understand) Define a handoff condition and explain why
   "looks good" fails as one.
2. (Apply) Write handoff conditions for three steps in the
   class website build.
3. (Analyze) Identify the "dangerous middle" — steps where
   Claude's output requires specific verification not in the
   obvious checklist.

**Opening:** The teacher reviews Claude's output. It looks
correct. They approve it. Three days later: a broken link
they would have caught if they'd checked the one thing they
forgot to check.

<!-- → [DIAGRAM: The handoff condition gate. Build step N →
[Handoff condition: specific, testable, binary] → Pass → Build
step N+1. Fail path: /rewind to step N checkpoint, respecify,
rerun. Editorial style.] -->

**Core content:**
- What a handoff condition is: specific, testable, binary
- Why "looks good" fails: it's a feeling, not a criterion
- The dangerous middle in a class website build
- Writing a handoff condition: "Every link on the new page
  opens correctly. No CSS from prior pages has changed.
  The page renders correctly on mobile." Binary. Testable.
- The STOP block: explicit conditions under which Claude must
  pause and wait for human verification before continuing
- When a handoff condition fails:
  - /rewind: press Esc twice or type /rewind, select the
    checkpoint before the failed step, write a better
    specification including the failed condition as a negative
    constraint, run from clean state. Forward correction adds
    failed attempts to the context window. Two failed
    corrections → /clear and rewrite from scratch.
  - /clear: resets context entirely between unrelated tasks or
    after context has accumulated too many failed approaches

<!-- → [TABLE: Strong vs. weak handoff conditions. Five examples.
Left: weak. Right: strong. Rows: link check, CSS isolation,
mobile rendering, content accuracy, file structure. No color.] -->

**Teacher build:** The teacher adds handoff conditions to every
step of the class website build and runs a structured verification
pass. Finds one failure. Uses /rewind to restore state. Respecifies.

**Classroom activity:** Students add handoff conditions to a
provided build sequence. Class exercise: test each other's
conditions by deliberately introducing the errors they're meant
to catch.

**Assessable exercises:**
1. (Apply) Write handoff conditions for the next three steps
   in your class website build. Each must be specific and binary.
2. (Analyze) Identify one "dangerous middle" step in your build.
   Write the handoff condition that catches it.
3. (Create) Design a classroom exercise that teaches handoff
   conditions using a non-coding build (a recipe, a lesson plan,
   a rubric).

**Gate 1:** The teacher has built one deployable web page using
CLAUDE.md, specification prompts, and explicit handoff conditions.
They have designed one classroom activity using each concept.
They are ready for a build that costs something if it goes wrong.

**Wayback Machine:** 🕰️ **W. Edwards Deming** (1900–1993) —
statistician who argued that quality is built into a process
through explicit verification at every step, not inspected in
at the end. His Plan-Do-Check-Act cycle is the handoff condition
principle applied to manufacturing. His observation that "a bad
system will beat a good person every time" is the argument for
hooks in Chapter 7.

**Bridge:** The reader has the basic discipline. Act Two begins.
Chapter 5 names the five things the teacher must never delegate.

---

## ACT TWO — BUILD
*Chapters 5–9: The grading tool — every supervisory capacity exercised*

---

### Chapter 5 — The Five Supervisory Capacities

**One-line:** These are the five things you do that Claude cannot.
Name them. Exercise them explicitly. Never delegate them.

**Learning outcomes:**
1. (Remember) Name and define the five supervisory capacities.
2. (Apply) Label the supervisory capacity required at each step
   of a provided grading tool build sequence.
3. (Analyze) Diagnose a build that went wrong by identifying
   which supervisory capacity was absent.

**Opening:** Seth mid-build on a grading tool. Something is
wrong with Claude's output. He can't tell what — it seems fine,
it produces feedback, it's fast. He almost ships it. What capacity
would have caught this? Answer: plausibility auditing.

<!-- → [DIAGRAM: Five supervisory capacities as a labeled five-
column layout. Each column: abbreviation (PA, PF, TO, IJ, EI),
plain name, one-sentence definition, example in grading context.
Editorial style. No color.] -->

**Core content:**

**[PA] Plausibility Auditing:** Hearing the wrong note.
In a grading tool: "This feedback is technically accurate.
But would I say this to this student? Does it match the rubric
in the way the rubric intends?" Claude produces fluent output
calibrated for accuracy, not for pedagogical appropriateness.

**[PF] Problem Formulation:** Deciding what the build IS before
Claude sees it. "Am I building a tool that generates feedback,
or a tool that flags patterns across submissions so I can write
the feedback myself?" Claude optimizes within the frame. If the
frame is wrong, the output is wrong, elegantly.

**[TO] Tool Orchestration:** Choosing which Claude task, in
what order, with what trust level. "Do I give Claude the whole
rubric or just the criteria for this assignment?"

**[IJ] Interpretive Judgment:** Supplying meaning Claude cannot
supply. "This feedback is correct, but this student has been
struggling all semester. The feedback needs a different tone."

**[EI] Executive Integration:** Holding the whole build toward
a single goal. "Three prompts ago we agreed the tool would never
generate a final grade. This output is generating grades. Stop."

<!-- → [TABLE: Five supervisory capacities — label, name, what
it catches, example failure when absent. Five rows. No color.] -->

**Teacher build:** A complete grading tool build sequence
analyzed step by step, with each supervisory capacity labeled.

**Classroom activity:** Students analyze a provided Claude
transcript where one supervisory capacity is systematically
missing. They identify which one, trace the consequences, and
propose the intervention. Cross-reference with students book
Chapter 5.

**Assessable exercises:**
1. (Apply) Label the supervisory capacity required at each step
   of your grading tool build plan.
2. (Analyze) A build transcript is provided where plausibility
   auditing was absent. Identify the exact moment and what the
   teacher should have done.
3. (Create) Design a classroom activity teaching the five
   supervisory capacities using a non-coding context.

**Wayback Machine:** 🕰️ **Norbert Wiener** (1894–1964) —
founder of cybernetics, who formalized the feedback loop as the
mechanism by which a system maintains its goal in the face of
disturbance. The five supervisory capacities are the feedback
mechanisms that keep a Claude Code build aligned with the
teacher's intent when Claude's autonomous execution would
otherwise drift.

**Bridge:** The reader knows the five capacities. Chapter 6
gives them the Skills system that makes exercising them
systematic and reusable.

---

### Chapter 6 — Skills: Build Once, Use Every Semester

**One-line:** A Skill is a CLAUDE.md file for a specific task —
a lesson plan generator, a rubric builder, a grading workflow.
Build it once. Invoke it with /skill-name every semester.

**Learning outcomes:**
1. (Understand) Explain what a Skill is and how it differs from
   CLAUDE.md (always-on) and Hooks (enforcement).
2. (Apply) Build a lesson-plan-generator skill and a grading-
   workflow skill using the SKILL.md format.
3. (Apply) Invoke a skill with /skill-name and configure
   automatic triggering.

**Opening:** The teacher is writing the same grading workflow
specification for the third time. This chapter ends that.

<!-- → [DIAGRAM: Skills vs. CLAUDE.md vs. Hooks — three columns.
CLAUDE.md: loads every session, always-on. Skills: loads on
demand, invoked by /name or by Claude when relevant. Hooks:
runs on lifecycle events, deterministic enforcement.
No color.] -->

**Core content:**
- What a Skill is: a SKILL.md file in .claude/skills/ giving
  Claude domain knowledge and reusable workflows
- The SKILL.md format: name, description, instructions,
  template, example output
- Two types: reference skills (knowledge Claude uses throughout
  a session) and action skills (workflows invoked with /skill-name)
- The disable-model-invocation: true flag: hides skill from
  Claude until manually invoked — useful for skills with side
  effects, reduces context cost to zero until needed
- Context cost: skill descriptions load at session start; full
  content loads only when used — keeps CLAUDE.md lean
- Skills across projects: symlinks to share skills across
  classroom repositories
- Teacher-relevant skills to build: lesson-plan-generator,
  rubric-builder, grading-workflow, differentiation-helper,
  feedback-generator
- The Education Agent Skills Library (152 evidence-based
  teaching skills across 19 learning-science domains, MCP tools)

<!-- → [TABLE: Teacher skill catalog — skill name, what it does,
when to invoke, disable-model-invocation setting (yes/no).
Six rows: lesson plan, rubric, grading workflow, differentiation,
feedback generator, exit ticket. No color.] -->

**Teacher build:** The teacher builds two skills: a lesson-plan-
generator and a grading-workflow skill. Both invoked. Both
verified. Both checked into git for next semester.

**Classroom activity:** Students build a skill for a repeated
task in a project they're working on. Class discussion: what
tasks are good skill candidates? What tasks are not?

**Assessable exercises:**
1. (Apply) Build a lesson-plan-generator skill. Test with
   three different subjects. Document what it does well and
   where you still need interpretive judgment.
2. (Apply) Build a grading-workflow skill that includes an
   explicit phase gate stopping Claude from generating a
   final grade.
3. (Analyze) Review a provided skill that is too long. Identify
   what should stay, what should move to CLAUDE.md, what should
   become a Hook.

**Wayback Machine:** 🕰️ **Charles Babbage** (1791–1871) —
mathematician who designed the Analytical Engine and articulated
the principle that analytical work should be organized into
reusable subroutines — operations that could be stored on
punched cards and re-executed without re-specification. A Claude
Skill is a Babbage subroutine: once specified, invocable forever.

**Bridge:** The reader has skills. Chapter 7 adds the enforcement
layer: the Hook that runs regardless of what Claude decides.

---

### Chapter 7 — Hooks: The Enforcement Layer

**One-line:** A CLAUDE.md instruction that says "never generate
a final grade" is a request. A Hook that blocks grade generation
is enforcement. This is the chapter where "do not" becomes
"cannot."

**Learning outcomes:**
1. (Understand) Explain the difference between CLAUDE.md
   instructions (advisory) and Hooks (deterministic enforcement).
2. (Apply) Write a PostToolUse hook that blocks grade generation
   in a grading tool.
3. (Apply) Write a PreToolUse hook that runs verification after
   every file edit.

**Opening:** The teacher adds "never generate a final grade" to
their CLAUDE.md. Claude generates a final grade. This chapter
explains why, and what to do instead.

<!-- → [DIAGRAM: The enforcement hierarchy. CLAUDE.md: advisory —
Claude reads and tries to follow. Skills: on-demand — loaded
when invoked. Hooks: deterministic — runs regardless of what
Claude decides. Three tiers, labeled. No color.] -->

**Core content:**
- What a Hook is: a script that runs automatically at specific
  points — unlike CLAUDE.md, Hooks are deterministic
- Hook events: PreToolUse (before Claude uses a tool),
  PostToolUse (after), SessionStart, SessionEnd
- Hook types: shell command, HTTP request, LLM prompt, subagent
- Context cost: zero unless the hook returns output
- The enforcement rule: if a rule must hold every time, it is
  a Hook, not a CLAUDE.md instruction
- Writing hooks by asking Claude: "Write a hook that blocks
  any output containing a numeric grade"
- Configuring hooks in .claude/settings.json; /hooks to browse
- Teacher-relevant hooks:
  - Block grade generation in grading tool
  - Run verification after every file edit
  - Log session activity for classroom oversight
  - Require confirmation before batch operations on student data
- The handoff condition made operational: Hooks enforce the
  conditions that handoff conditions specify

<!-- → [TABLE: CLAUDE.md instruction vs. Hook — two columns.
Five examples. Left: instruction in CLAUDE.md. Right: equivalent
Hook. Rows: grade generation block, CSS isolation, file
protection, verification run, session logging. No color.] -->

**Teacher build:** The teacher adds three hooks to their grading
tool: a PreToolUse hook blocking final grade generation, a
PostToolUse hook running verification after every file edit,
and a SessionEnd hook logging what Claude touched.

**Classroom activity:** Students design hooks for a provided
student project. The constraint: every hook must enforce a
condition currently only in CLAUDE.md. Class discussion: what
is the difference between telling Claude not to do something
and preventing it?

**Assessable exercises:**
1. (Apply) Write a hook that blocks your grading tool from
   generating a final grade. Test it by explicitly asking Claude
   to generate a grade.
2. (Apply) Write a hook that runs a verification script after
   every file Claude edits in your class website.
3. (Evaluate) Review your grading tool's CLAUDE.md. Which
   instructions should be hooks instead? Convert at least one.

**Wayback Machine:** 🕰️ **Claude Shannon** (1916–2001) —
mathematician and electrical engineer who founded information
theory and designed the first digital circuits. His concept
of the logic gate — a physical mechanism that enforces a boolean
condition regardless of context — is the conceptual ancestor
of the Hook. Shannon's gates don't advise; they enforce.

**Bridge:** The reader has enforcement. Chapter 8 is about the
hardest moment in a grading tool build: when enforcement passes
and the output is still wrong.

---

### Chapter 8 — The Dangerous Middle: When Claude Is Right and Wrong Simultaneously

**One-line:** The hardest moment in a grading tool build: Claude
produces feedback that passes every handoff condition you wrote
and is still pedagogically wrong. This chapter is about the
condition you didn't know to write.

**Learning outcomes:**
1. (Analyze) Identify the "dangerous middle" in a grading tool
   build — outputs that pass surface checks but fail
   pedagogical judgment.
2. (Apply) Write handoff conditions that require domain knowledge,
   not just technical correctness.
3. (Evaluate) Assess when plausibility auditing must substitute
   for a handoff condition that cannot be automated.

**Opening:** Seth describes the moment in his own grading tool
build where the output was correct and wrong simultaneously.
The teacher reads it and recognizes something they've already
experienced.

**Core content:**
- The three documented failure modes (Anthropic RCT):
  AI Delegation, Progressive AI Reliance, Iterative AI Debugging
- The debugging gap: largest performance disparity on diagnostic
  questions — exactly the skill grading develops
- The handoff condition you cannot write: "Does this feedback
  match what I would say to this specific student?" —
  irreducibly human, cannot be automated, requires plausibility
  auditing every time
- The narrowing principle: scope the tool more narrowly. Use
  Claude to flag patterns across submissions, not to generate
  individual student feedback. The interpretive judgment layer
  stays with the teacher.
- The "first draft, never final word" rule: AI grading accuracy
  ~50-55% with rubric, ~33% without. First draft only.
- ESL and AAVE bias: documented 15-20% score discrepancies for
  English language learners; racial bias in AI teacher assistant
  tools. The equity handoff condition: does this feedback treat
  all students' language as equally valid?

<!-- → [DIAGRAM: The narrowing principle. Before: Claude generates
individual student feedback (dangerous). After: Claude flags
patterns across submissions → teacher writes individual feedback
(safe). Arrows showing the two paths. No color.] -->

**Teacher build:** The teacher rebuilds their grading tool with
narrower scope: Claude flags patterns, teacher writes individual
feedback.

**Classroom activity:** Students audit a provided AI-generated
feedback set for pedagogical appropriateness. Identify three
instances where the feedback is technically correct but
pedagogically wrong. Rewrite them. Discussion: what made the
rewrite require a human?

**Assessable exercises:**
1. (Analyze) Review five pieces of AI-generated feedback.
   Identify which ones pass technical handoff conditions but
   fail pedagogical judgment.
2. (Apply) Redesign your grading tool's scope based on the
   narrowing principle.
3. (Evaluate) Write a policy for classroom AI grading use that
   you could explain to a student who asks why.

**Wayback Machine:** 🕰️ **Alfred Binet** (1857–1911) —
psychologist who developed the first intelligence test and
immediately warned against misusing it: "the scale is a rough
guide for identifying children who need help, not a label
for fixed intelligence." His insistence on the human
interpretation layer — that a number requires a professional
judgment to be useful — is the grading tool's plausibility
auditing requirement stated as a founding principle.

**Bridge:** The reader has a working grading tool with appropriate
scope. Chapter 9 addresses context management as the tool
grows more complex: the subagent.

---

### Chapter 9 — Subagents: Keeping the Build Clean

**One-line:** A subagent is a Claude session that runs in its
own context and reports back a summary. When your grading tool
research starts filling the session with file reads, delegate
the research. Keep the main build clean.

**Learning outcomes:**
1. (Understand) Explain what a subagent is and how it differs
   from a Skill and a main session.
2. (Apply) Delegate a research task to a subagent.
3. (Apply) Define a custom subagent for a specialized classroom
   task.

**Opening:** The teacher's grading tool session is slowing down.
Claude is taking longer to respond. The context window is filling
with research that isn't part of the build.

<!-- → [DIAGRAM: Main session vs. subagent. Main session: context
window filling with build history, file reads, research.
Subagent: isolated context, reads many files, returns summary
only. Arrows showing summary return to main session. No color.]
-->

**Core content:**
- What a subagent is: isolated Claude session with its own
  context window, returns summary to main session
- Subagents vs Skills: Skills are content Claude loads,
  Subagents are workers that run separately
- Context cost: subagents are isolated — their work doesn't
  bloat the main conversation
- How to spawn: "Use a subagent to investigate how to handle
  late submissions in a grading workflow. Return findings only,
  not the files you read."
- Custom subagents in .claude/agents/: define specialized
  workers with their own system prompt and allowed tools
- Teacher-relevant subagent patterns:
  - Research subagent: investigate X, return summary only
  - Review subagent: review this output for edge cases
  - Pattern analysis: analyze submissions for common
    misconceptions, return a pattern report
- The Writer/Reviewer pattern: one Claude session implements,
  a subagent reviews from clean context with no bias toward
  the code it didn't write
- Auto memory: Claude accumulates learnings across sessions
  without the teacher writing anything; subagents can maintain
  their own auto memory

**Teacher build:** The teacher adds a pattern analysis subagent
to their grading tool workflow: reads all submissions, identifies
common misconceptions, returns a structured report — without
cluttering the main grading session.

**Classroom activity:** Students define a custom subagent for
a specialized task. Constraints: defined scope (specific files,
specific output format), returns summary not full transcript.

**Assessable exercises:**
1. (Apply) Delegate a research task to a subagent. Verify that
   the main session context did not grow during the research.
2. (Apply) Define a custom subagent for peer review analysis.
   Specify: allowed tools, system prompt, output format.
3. (Analyze) Compare a session where you researched inline vs.
   a subagent session for the same research. What was the
   difference in context growth?

**Gate 2:** The teacher has a working grading tool with skills,
hooks, and subagents. They have experienced the dangerous middle
and narrowed the tool's scope appropriately. They are ready to
build for students, not just for themselves.

**Wayback Machine:** 🕰️ **Herbert Simon** (1916–2001) —
Nobel laureate who formalized the concept of decomposition in
complex systems: breaking a large problem into nearly
decomposable subsystems that can be solved independently and
integrated. The subagent is Simon's nearly decomposable
subsystem applied to Claude Code: isolated context, local
solution, summary integration.

**Bridge:** The reader has the full conducting discipline. The
Bridge chapter transitions from productivity to pedagogy.

---

### BRIDGE — From Tools That Save Time to Tools That Change What's Possible

**One-line:** Seth describes the moment his builds stopped being
about productivity and started being about what he could make
that didn't exist before.

**No learning outcomes. No exercises. No classroom activity.**
Seth's voice. One frame. The teacher turns the page ready
for Chapter 10.

**Core content:**
- The productivity frame vs. the possibility frame
- The grading tool served the teacher. The simulation serves
  the student. That's a different design question.
- What an interactive simulation can do that a worksheet cannot
- Seth's first simulation: what he built, what surprised him,
  what students did with it that he didn't expect
- Why the Brutalist three-file system matters now: the simulation
  has aesthetic and pedagogical decisions that need to be
  protected from Claude's improvisation
- The teacher's Act Three question: what concept in your
  curriculum has no good interactive analog yet?

<!-- → [DIAGRAM: The shift from productivity to pedagogy. Two
objects: grading tool (serves teacher) → interactive simulation
(serves student). The design question changes when the
beneficiary changes. Simple. Editorial style.] -->

**Wayback Machine:** 🕰️ **Seymour Papert** (1928–2016) —
mathematician and educator who invented Logo and argued that
children learn most deeply when they build things for others
to use — when the artifact has an audience beyond the maker.
His concept of "objects to think with" is the simulation's
pedagogical theory.

---

## ACT THREE — APPLY
*Chapters 10–14: The interactive classroom simulation*

---

### Chapter 10 — The Three-File System: Intent, Constitution, State

**One-line:** Before Claude writes a single line of the simulation,
three files define everything. The Intent Layer is human, always.
The Technical Constitution governs what Claude never improvises.
The Project State tracks what is built and what is pending.

**Learning outcomes:**
1. (Understand) Explain what each of the three files protects
   and why all three must be populated before generation begins.
2. (Apply) Write the Intent Layer of a PROJECT.md for an
   interactive simulation.
3. (Apply) Write a DESIGN.md specifying the simulation's visual
   and interaction vocabulary completely enough that Claude
   cannot improvise.

**Opening:** The teacher opens Claude Code and types "build me
an interactive sorting algorithm simulator." Claude builds
something. It works. It looks fine. But the color scheme isn't
the teacher's. The interaction model isn't what the teacher had
in mind. The pedagogical scaffolding is missing. The teacher
didn't draw the line before Claude started.

<!-- → [DIAGRAM: The three-file system as three concentric
circles or three nested boxes. Outer: CLAUDE.md (technical
constitution). Middle: DESIGN.md (visual constitution). Inner:
PROJECT.md (project state — Intent Layer is human, always).
Editorial style. No color.] -->

**Core content:**
- **CLAUDE.md (Technical Constitution):** What Claude never
  improvises. Naming conventions, what it must never touch
  without instruction, verification checklist. Changes when
  the tech stack changes, not when the project changes.
- **DESIGN.md (Visual Constitution):** Complete color system
  (six variables maximum — no others), typography, spacing,
  interaction vocabulary, and explicit list of what the system
  never does. Not a guideline. A boundary.
- **PROJECT.md (Project State):** Two layers.
  Layer 1 — Intent (human, never overwritten by Claude): what
  this simulation is, what the student should understand,
  what the tone is.
  Layer 2 — Technical State (AI layer): what is built, what
  is pending, generation log.
- The phase gate: generation does not begin until both layers
  of PROJECT.md are populated
- The Brutalist governing principle: maximally informed,
  minimally autonomous, by design

<!-- → [TABLE: Three-file system — file name, what it contains,
who writes it, when it changes. Three rows. No color.] -->

**Teacher build:** The teacher writes all three files for their
simulation before writing a single specification prompt.
Three files, fully populated, before Claude sees the project.

**Classroom activity:** Students write the Intent Layer of a
PROJECT.md for a simulation they want to build. Class exercise:
read each other's Intent Layers without seeing the simulation
concept. Can you tell what it's trying to teach?

**Assessable exercises:**
1. (Apply) Write all three files for your simulation project
   before running Claude. If it takes more than 45 minutes,
   the scope is too large.
2. (Analyze) Review a provided PROJECT.md with a weak Intent
   Layer. Identify what's missing and rewrite it.
3. (Evaluate) What decisions in your simulation are pedagogical
   (Intent Layer) vs. technical (CLAUDE.md)? List three of each.

**Links:** [brutalist.art](https://brutalist.art)

**Wayback Machine:** 🕰️ **Mies van der Rohe** (1886–1969) —
architect whose principle "less is more" and concept of a
structural frame that defines what is built without determining
every detail is the three-file system as architectural
philosophy: the constitution defines the boundary; within the
boundary, execution is delegated; outside the boundary,
nothing happens without explicit instruction.

**Bridge:** Three files complete. Chapter 11 begins the build.

---

### Chapter 11 — Building the Simulation: Conducting at Full Complexity

**One-line:** The three files are in place. The build begins.
Every step has a specification, a handoff condition, and a
labeled supervisory capacity. This is what conducting looks
like at full complexity.

**Learning outcomes:**
1. (Apply) Execute a build sequence for the simulation, completing
   Claude tasks and human tasks in dependency order.
2. (Apply) Apply each supervisory capacity at the steps requiring
   it, labeled explicitly.
3. (Analyze) Identify when the simulation build is going off-script
   and stop before the three-file system is violated.

**Opening:** Seth's simulation build — real build, real prompts,
real Claude outputs. The teacher reads it and recognizes the
framework in action.

<!-- → [DIAGRAM: The simulation build loop. Three files populated
→ Specification → Claude executes → Handoff condition check →
[Pass: next step / Fail: /rewind and respecify]. Subagent
research branch off the main loop. Supervisory capacity label
at each human step. Editorial style.] -->

**Core content:**
- Running the build: Explore → Plan → Implement → Commit
  applied to simulation development
- Context management during a complex build:
  /clear between unrelated tasks; subagents for research;
  /compact with explicit focus; /rewind when a handoff fails
- The scope creep moment: Claude suggests "while I'm here"
  improvements — log in PROJECT.md Layer 2, do not execute
- Verification for a simulation: does a student who has never
  seen this know what to do in the first 30 seconds?
- Give Claude a way to verify its own work: define a target
  state for each simulation state, give Claude a way to
  screenshot and compare, ask it to iterate until it matches.
  The feedback loop produces significantly better visual output
  than single-pass generation.
- The Writer/Reviewer pattern: subagent reviews interaction
  design from the perspective of a student who knows nothing
  about the topic
- /clear between unrelated tasks; after two failed corrections,
  /clear and write a better specification

**Teacher build:** Phase 1 of the simulation build, documented
step by step. Every specification, every handoff condition, every
supervisory capacity labeled. One rejection and revision in full.

**Classroom activity:** Students run Phase 1 of their own
simulation build using their three files. Required: a build log
documenting each specification, handoff condition, and supervisory
capacity label. Peer review of build logs.

**Assessable exercises:**
1. (Apply) Execute Phase 1 of your simulation build. Document
   every specification prompt and handoff condition evaluation.
2. (Analyze) At least one Claude output will require revision.
   Document the failure and the revision specification.
3. (Evaluate) At the end of Phase 1: what would you change in
   your three files?

**Wayback Machine:** 🕰️ **Donald Schön** (1930–1997) — educator
who introduced the concept of "reflection-in-action": the
practitioner who thinks about what they are doing while they
are doing it, adjusting in real time rather than only after
the fact. The supervisory capacity labels in the build log are
Schön's reflection-in-action made operational — the teacher
naming what they are doing as they do it.

**Bridge:** The simulation works in the terminal. Chapter 12
deploys it in class.

---

### Chapter 12 — Deploying in Class: From Build to Lesson

**One-line:** The simulation works in your terminal. Now it
has to work with 30 students who have never seen it. This chapter
is about the gap between "it works" and "it teaches."

**Learning outcomes:**
1. (Apply) Deploy a classroom simulation as a shareable web
   artifact that students can access without setup.
2. (Analyze) Identify the gap between "works in terminal" and
   "works in classroom" and conduct a revision build.
3. (Apply) Design a classroom activity that uses the simulation
   as a learning tool rather than a demonstration.

**Opening:** The teacher projects the simulation on the classroom
screen for the first time. A student clicks something unexpected.
The simulation breaks. This chapter prepares for that moment
before it happens.

<!-- → [DIAGRAM: The student-facing verification pass. Three
checks in sequence. Check 1: does a student who knows nothing
about the code know what to do in 30 seconds? Check 2: are
failure states informative or just broken? Check 3: does the
simulation have a path from easy to hard? Binary results.
Revision build path if any check fails.] -->

**Core content:**
- Deployment options: Claude Artifacts (fastest path to a
  shareable URL), GitHub Pages (free hosting for HTML/CSS/JS),
  class website integration from Act One
- The student-facing verification pass: what "it works for
  students" looks like differently from "it works in my terminal"
- First 30 seconds test: does a student know what to do without
  instructions?
- Failure states: are they informative or just broken?
- Progression: does the simulation have a path from easy to hard?
- Conducting a revision build based on classroom observation:
  watch students use it, note what confuses them, conduct a
  new build session to fix it
- The feedback loop as a teaching opportunity: showing students
  how the simulation was built from their feedback is itself
  a lesson in conducting

**Teacher build:** The teacher deploys and runs a student-facing
verification pass. Identifies two gaps. Conducts a revision build.
Deploys again.

**Classroom activity:** Students deploy their simulations and
run a cross-class usability test: a student from another group
tries each simulation without any explanation. The builder
observes. Documents what breaks. Conducts a revision build.

**Assessable exercises:**
1. (Apply) Deploy your simulation. Give it to one person who
   knows nothing about the topic. Document what they did that
   you didn't expect.
2. (Analyze) Conduct a revision build based on that observation.
   Document the specification, handoff condition, and supervisory
   capacity exercised most.
3. (Evaluate) What is the difference between a simulation that
   works and one that teaches? Name three specific design
   decisions in yours.

**Wayback Machine:** 🕰️ **Maria Montessori** (1870–1952) —
educator who argued that educational materials must be designed
to be self-correcting: the student who uses the material
discovers their own errors without needing teacher intervention.
Her concept of the "control of error" — built into the material
itself — is the first 30 seconds test applied to educational
design.

**Bridge:** The simulation is deployed. Chapter 13 maps what
students are learning to what the teacher now knows how to teach.

---

### Chapter 13 — Teaching the Discipline: What Your Students Are Reading

**One-line:** Your students have the students book. This chapter
maps what they're learning to what you now know how to teach —
and how to design activities that make both books work together.

**Learning outcomes:**
1. (Apply) Map each chapter of the students book to a classroom
   activity using the teacher's built tools as context.
2. (Apply) Design an assessment requiring students to document
   their supervisory capacity use during a build.
3. (Analyze) Distinguish the teacher's role in a Boondoggled
   student build from the teacher's role in a traditional coding
   class.

**Opening:** The teacher reads Chapter 5 of the students book —
the five supervisory capacities — and recognizes what Seth is
describing from the inside. The chapter that once seemed abstract
is now familiar.

<!-- → [TABLE: Students book chapter map — chapter number, what
students learn, corresponding teacher build experience, suggested
classroom activity. 14 rows. No color.] -->

**Core content:**
- The students book chapter map: what students are learning
  and when, mapped to this book's build tiers
- Using the teacher's grading tool as a teaching artifact:
  "Here's a tool I built with Claude Code. Here's the build
  log. Here's where I exercised plausibility auditing."
- Using the teacher's simulation as a teaching artifact:
  "Here's the simulation you've been using. Here's how I
  built it. Here's what I would do differently."
- Assessment design for conducting: what does "the student
  exercised plausibility auditing" look like in a build log?
  How do you assess the supervisory capacity, not just the
  output?
- The teacher's role during a student build: not fixing their
  code — asking supervisory capacity questions. "What was your
  handoff condition for this step? Did it pass? What did you
  do when it didn't?"
- The Geoffrey Challen insight: "The challenge now isn't turning
  specifications into code. The challenge is getting your idea
  out of your own brain and into a specification so the coding
  agent can do the rest." Teaching specification writing IS
  CS education.

**Teacher build:** None — this chapter's output is a classroom
activity design and a build log assessment template.

**Classroom activity:** The teacher designs an activity requiring
students to submit a build log alongside their code. The build
log documents: every specification prompt, every handoff
condition evaluation, every supervisory capacity label. Peer
review of build logs, not code.

**Assessable exercises:**
1. (Apply) Design a build log template for students capturing
   specification prompts, handoff conditions, and supervisory
   capacity labels.
2. (Apply) Create a rubric for assessing the build log that is
   separate from the rubric for assessing the code.
3. (Evaluate) What is the hardest supervisory capacity for your
   students to exercise? Design an activity isolating and
   practicing that specific capacity.

**Wayback Machine:** 🕰️ **Lee Shulman** (born 1938) — educator
who introduced the concept of "pedagogical content knowledge":
the specific knowledge a teacher needs not just to know a
subject but to teach it to others. His argument that subject
knowledge and pedagogical knowledge must be integrated —
that the expert and the teacher are different roles requiring
different preparation — is the argument for this book existing
separately from the students book.

**Bridge:** The discipline is taught. Chapter 14 is the record
of what the teacher built.

---

### Chapter 14 — Your Terminal Deliverable: The Post-Build Document

**One-line:** The simulation is deployed. The build is done.
This chapter is the record of what you built, what you learned,
and what you would do differently.

**Learning outcomes:**
1. (Create) Produce a post-build document for the interactive
   simulation using the five-section template.
2. (Evaluate) Assess your own build against the five supervisory
   capacities.
3. (Create) Design a second build based on what the first one
   taught you.

**Opening:** Not Seth's build. Yours. The simulation is running
in your classroom. Students are using it. This chapter asks
you to account for every decision.

<!-- → [DIAGRAM: The post-build document as the arc's terminal
artifact. A simple timeline from Chapter 0 (the teacher opens
the terminal) to Chapter 14 (the teacher accounts for every
decision). Five milestones labeled: first session / first page /
grading tool / simulation deployed / post-build document.
Editorial style.] -->

**Core content:**
- The post-build document: five sections
  1. What I built (one paragraph, plain language)
  2. What I delegated to Claude and why
  3. What I kept for myself and why
  4. What I learned that I didn't know before the build
  5. What I would do differently
- The post-build document as a teaching artifact: share it
  with students. Model the discipline, don't just describe it.
- What comes next: the second simulation (built faster, better
  three files), the teacher-as-builder community (CSTA, Claude
  Connect), the Irreducibly Human series

**Terminal deliverable:** The teacher's post-build document
for the interactive simulation. One document. Five sections.
Honest about what worked and what didn't.

**Closing:**
"You built it. Your students learned from it. You know what
every decision cost you and what it gave you. That is what
conducting looks like when it's complete. The next build
starts here."

**Assessable exercises:**
1. (Create) Write your post-build document for the interactive
   simulation. Five sections. Honest.
2. (Evaluate) Which supervisory capacity was hardest to exercise
   consistently in your build? Design a practice exercise that
   targets that capacity in your students.
3. (Create) Design the second simulation — what you would build
   with what the first one taught you. Start with the three files.

**Wayback Machine:** 🕰️ **Donald Schön** (1930–1997) — educator
who introduced "reflection-on-action": the practitioner who,
after an episode of practice, thinks carefully about what they
did and why, in order to improve future practice. The post-build
document is Schön's reflection-on-action made mandatory —
the structure that ensures the build changes the teacher, not
just the repository.

---

# PART 9 — CHAPTER ANATOMY TEMPLATE

All 14 chapters plus bridge follow this structure. The Cowork
enrichment pass processes items marked with comments.

1. **One-line descriptor** (capability build, not topic)
2. **Learning outcomes** (3–5, Bloom's level labeled)
3. **Chapter opening** (Seth narrative, teacher scenario,
   or failure case — problem before framework)
4. **Figure comments** — `<!-- → [DIAGRAM: ... ] -->` or
   `<!-- → [TABLE: ... ] -->` embedded at point of use
5. **Core content sections** (4–6): concept → teacher build
   application → classroom activity application
6. **Teacher build** (explicit build step for this chapter's
   concept, part of the three-tier arc)
7. **Classroom activity** (classroom-facing application of
   the same concept; cross-reference to students book chapter
   where applicable)
8. **Assessable exercises** (minimum 3; at least one requiring
   production; at least one connecting to classroom activity)
9. **Links** (where applicable: code.claude.com, boondoggling.ai,
   brutalist.art, humanitarians.ai/tools)
10. **AI Wayback Machine** — `## 🕰️ AI Wayback Machine` — one
    pre-2000 figure per chapter, connected to chapter's
    intellectual substance
11. **Bridge** (one sentence; raises what next chapter answers)

**Phase gates embedded:** Gate 1 at end of Chapter 4,
Gate 2 at end of Chapter 9. Both gates state explicitly
what must be true before the next act begins.

**Enforcement:** A draft chapter missing items 4 (figures),
6 (teacher build), 7 (classroom activity), 10 (Wayback Machine),
or 11 (bridge) is an incomplete draft. Do not advance to peer
review without resolving it.

**Seth's voice rule:** Seth's retrospective voice is present
in Chapters 0, 5, 8, and the Bridge. It is illustrative in
other chapters. The teacher is the primary actor from Chapter 1
forward. Seth never gives instructions; he describes what he
experienced.

---

# PART 10 — CASE STUDY STRATEGY

## Domain coverage map

| Domain | Chapters | Primary use |
|---|---|---|
| Class website | 1–4 | Act One build arc |
| Grading / rubric tools | 5–9 | Act Two build arc |
| Interactive simulation | 10–14 | Act Three build arc |
| Student submission patterns | 8 | Dangerous middle evidence |
| CS curriculum concept visualizer | 10–11 | Simulation worked example |
| Cross-class usability test | 12 | Student-facing verification |

## Case escalation

Act One cases: low stakes — the broken link, the wrong CSS.
Single concept, clear resolution.
Act Two cases: higher stakes — the grading tool that produces
technically correct and pedagogically wrong feedback. Multiple
concepts, judgment required.
Act Three cases: full complexity — Seth's real simulation build
session across four chapters. No single right answer.

## Worked example format (teacher builds)

Situation → The build decision the teacher faces → What the
specification looked like → What Claude produced → The handoff
condition evaluation → What the supervisory capacity that was
exercised was → The classroom activity this informs.

## Sourcing requirement

CSTA 2025 data cited for reader profile claims. Anthropic
Education Report cited for teacher-as-builder validation.
Geoffrey Challen talk cited for practitioner evidence.
Anthropic RCT cited for the grading chapter's empirical
foundation. All case studies explicitly labeled as illustrative
or sourced.

---

# PART 11 — HARD TOPICS, CONTESTED CLAIMS, AGING RISK

## Contested claims

| Claim | Status | Book's position |
|---|---|---|
| AI grading is accurate enough for classroom use | Disputed | 50-55% accuracy with rubric; first draft only; human judgment required |
| Hooks prevent all unauthorized Claude behavior | Overstated | Hooks are deterministic for the events they cover; Claude can still act outside hook events |
| The terminal barrier is low for all K-12 CS teachers | Disputed | Installation and first session walkthrough provided; terminal comfort varies |
| Claude Code is appropriate for all student builds | Platform-specific | Framework applies to any agentic coding tool; Claude Code is current implementation |

## Hard chapters

**Chapter 8 (Dangerous Middle):** The AI grading accuracy data
must be stated precisely — not as "AI can't grade" but as "AI
grading is a first draft tool at 50-55% accuracy with a rubric."
The ESL and AAVE bias findings require careful, specific
statement. Do not draft without someone who has taught this
in K-12 context.

**Chapter 7 (Hooks):** The technical content (writing hooks,
.claude/settings.json) requires a contributor with Claude Code
production experience. The conceptual content (CLAUDE.md is
advisory, Hooks are enforcement) is the chapter's core argument
and must be stated without ambiguity.

## Aging risk

| Content type | Risk | Review cadence |
|---|---|---|
| Claude Code feature references (hooks, skills, subagents) | High | Before each edition |
| CLAUDE.md syntax and /init behavior | High | Before each edition |
| Specific tool references (GitHub Pages, Claude Artifacts) | High | Before each edition |
| AI grading accuracy percentages | Medium | On new major studies |
| Five supervisory capacities | Low | On major framework revision |
| Three-file system (Brutalist) | Medium | On major tool change |
| Seth's narrative | None | N/A |
| CSTA and Anthropic Education Report data | Medium | Before each edition |

**Aging mitigation:** Main text teaches the discipline, not
the feature set. All feature-specific content is in Appendix A
(command reference), updatable without touching main text.
All URLs are live references. All statistics include publication
dates.

---

# PART 12 — MARKET POSITIONING SUMMARY

## The gap this book fills

No practitioner handbook teaches the conducting discipline to
K-12 CS teachers at the level of their actual classroom builds.
Every comparable resource is either developer-facing, research-
facing, or teaches teachers to use Claude as a content generator
rather than a build tool. The gap is closing — independent
researchers are arriving at phase-gated AI use simultaneously —
but no Monday-morning resource yet exists for this reader.

## Market size estimate

Primary: ~50,000 K-12 CS teachers in the US (CSTA estimate).
Secondary: 100–500 PD program adoptions per year at steady state.
Tertiary: District-level AI PD programs.

Natural adoption channels: CSTA community, Iowa State AI High
School Teachers Summer Program, Anthropic/Teach For All Claude
Connect (1,000+ educators in 60+ countries), teacher PD
networks.

---

# PART 13 — FEATURE LIST

| Feature | Priority | Production effort |
|---|---|---|
| 14-chapter + bridge architecture | ESSENTIAL | Low |
| Three-act learning arc | ESSENTIAL | Low |
| Interleaved structure (teacher build + classroom activity per chapter) | ESSENTIAL | Medium |
| Seth's practitioner voice | ESSENTIAL | Medium |
| Three build tiers (website, grading tool, simulation) | ESSENTIAL | High |
| Five supervisory capacities framework | ESSENTIAL | Low |
| CLAUDE.md full chapter treatment | ESSENTIAL | Medium |
| Skills chapter | ESSENTIAL | Medium |
| Hooks chapter | ESSENTIAL | High |
| Assessable exercises (3+ per chapter) | ESSENTIAL | Medium |
| Terminal deliverable (post-build document) | ESSENTIAL | Low |
| Gate 1 and Gate 2 explicit conditions | ESSENTIAL | Low |
| AI Wayback Machine (15 figures) | IMPORTANT | Low |
| Figure comments for Cowork enrichment | IMPORTANT | Medium |
| Students book chapter map (Ch 13) | IMPORTANT | Low |
| Three-file system templates (Appendix B) | IMPORTANT | Low |
| Appendix A (Claude Code quick reference) | IMPORTANT | Low |
| Medhavy integration (Kindle/online edition) | VALUABLE | High |
| Companion website | ASPIRATIONAL | High |

**Minimum Viable Book:** ESSENTIAL features only. Adoptable
by a self-directed K-12 CS teacher who finds it independently.

---

# PART 14 — OUT OF SCOPE

Permanently excluded:

| Topic | Reason | Covered better in |
|---|---|---|
| Full Claude Code API and advanced orchestration | Developer scope | code.claude.com documentation |
| AI grading as primary assessment | Research shows 50-55% accuracy; first-draft-only policy enforced by hooks | Excluded by design |
| Walker (Unity refactoring) | Game development supplement | Future edition |
| Agent teams | Power user pattern | Advanced follow-on |
| Server-side deployment and databases | Too complex for classroom-scale builds | Advanced follow-on |
| Generic AI ethics / responsible use policy | Not this book's scope | ai-for-teachers-a-practitioners-guide |
| MCP server configuration | Advanced feature | code.claude.com documentation |
| Full Boondoggling Score methodology | Student book scope | claude-code-for-students |

All exclusions acknowledged in the introduction. The students
book and code.claude.com are named explicitly as the resources
for excluded topics.

---

# PART 15 — ADOPTION RISK REGISTER

| # | Risk | Likelihood | Impact | Mitigation |
|---|---|---|---|---|
| 1 | Terminal barrier for non-coding-native CS teachers | High | High | Ch 1 includes complete first-session walkthrough with exact commands; dictation shortcut for time-pressed teachers |
| 2 | Aging risk: Claude Code feature specifics | High | Medium | Features in appendices; discipline in main text; live URL references |
| 3 | Grading tool chapter (Ch 8) requires careful statement of accuracy limits | Medium | High | ESL/AAVE bias data cited precisely; "first draft only" policy enforced by hooks |
| 4 | Hooks chapter (Ch 7) requires contributor with Claude Code production experience | Medium | High | Flag as contributor recruitment target; do not draft from documentation alone |
| 5 | Interleaved structure is harder to write than sequential | Medium | Medium | Each chapter has explicit teacher build and classroom activity sections; co-author / contributor can draft one track per chapter |
| 6 | Seth's practitioner voice requires authentic narrative | Medium | Medium | Seth drafts his own sections; narrative must not be paraphrased by other contributors |
| 7 | School district technology restrictions may limit Claude Code access | Medium | Low | Framework applies to any agentic tool; CLAUDE.md and skills concepts transfer; deployment appendix covers access options |

---

# PART 16 — OPEN QUESTIONS

| # | Question | Stakes | Decision deadline | Owner |
|---|---|---|---|---|
| 1 | What CS concept does the Act Three simulation teach? (sorting algorithms, memory allocation, recursion, or other?) | Worked example quality; must be a concept in actual CS curriculum | Before chapter drafting begins | Author + CS teacher advisory |
| 2 | Should the grading tool have a specific subject domain (CS, writing, math) or be domain-agnostic? | Classroom activity design; example specificity | Before Act Two drafting | Author |
| 3 | Does the book include a district-level deployment appendix for teachers in restricted technology environments? | Adoption barrier mitigation | Publisher proposal stage | Author + Publisher |
| 4 | Seth's practitioner voice scope: which chapters does Seth draft vs. which does he review? | Production planning; schedule | Before manuscript schedule | Author + Seth |
| 5 | Should Appendix A (Claude Code quick reference) be maintained on a separate web page rather than in the book, given command evolution? | Aging risk | Before production | Author |
| 6 | Windows dictation shortcut (Win+H) and Linux equivalent: confirm and document before Chapter 0 is final | Accessibility; reader profile includes Windows users per CSTA data | Before manuscript | Author |

---

## Appendix A — Claude Code Quick Reference for Teachers

The commands and concepts most useful at classroom scale.

**Session management:**
| Command | What it does |
|---|---|
| `claude` | Start a session in current directory |
| `claude --continue` | Resume most recent session |
| `claude --resume` | Choose from session list |
| `/clear` | Reset context between unrelated tasks |
| `/rewind` | Restore previous conversation and code state |
| `/compact` | Summarize and compress with control over what survives |
| Esc | Stop Claude mid-action |
| Esc Esc | Open rewind menu |

**Build workflow:**
| Command | What it does |
|---|---|
| `/init` | Generate starter CLAUDE.md from codebase |
| `Shift+Tab` twice | Enter plan mode (read-only until approved) |
| `Ctrl+G` | Edit the plan in your text editor before approving |
| `/memory` | Browse and edit CLAUDE.md and auto memory files |
| `/hooks` | Browse configured hooks |
| `#` + text | Ask Claude to remember something (saves to auto memory) |

**Context management:**
| Command | What it does |
|---|---|
| `/context` | See what's using context space |
| `/btw` | Side question that never enters conversation history |
| `/compact focus on X` | Summarize with explicit focus |

**The core constraint:** The context window fills fast. `/clear`
between unrelated tasks. After two failed corrections on the same
issue, `/clear` and write a better specification from scratch.

Full documentation: [code.claude.com](https://code.claude.com)

---

## Appendix B — Three-File Templates

**CLAUDE.md template for teacher classroom builds:**
```
# [Project Name] — Technical Constitution

## File structure
[Describe the file structure Claude must maintain]

## Stack
[Name the framework, CSS approach, JavaScript constraints]

## Naming conventions
[Specific naming rules]

## What Claude must never touch without explicit instruction
[List protected files and directories]

## Verification
[The command or check that confirms a step is complete]
```

**DESIGN.md template for interactive simulations:**
```
# [Simulation Name] — Visual Constitution

## Color system
[Six variables maximum. List them. No others.]

## Typography
[Display, body, code fonts. No others.]

## Interaction vocabulary
[What interactions are allowed. What the system never does.]

## Accessibility
[Requirements that cannot be compromised]
```

**PROJECT.md template:**
```
# [Simulation Name] — Project State

## Layer 1: Intent (Human Layer — never overwritten by Claude)
What this simulation is:
What the student should understand after using it:
What questions it answers:
What questions it refuses to answer:
The tone:

## Layer 2: Technical State (AI Layer)
What is built:
What is pending:
Generation log:
Open technical questions:
```

---

## Appendix C — Post-Build Document Template

Five sections. One document. Honest.

1. **What I built** (one paragraph, plain language — not technical)
2. **What I delegated to Claude and why**
3. **What I kept for myself and why**
4. **What I learned that I didn't know before the build**
5. **What I would do differently**

---

## Series Links

[boondoggling.ai](https://boondoggling.ai) ·
[brutalist.art](https://brutalist.art) ·
[frictional.xyz](https://frictional.xyz) ·
[irreducibly.xyz](https://irreducibly.xyz) ·
[nikbearbrown.com](https://nikbearbrown.com) ·
[humanitarians.ai/tools](https://www.humanitarians.ai/tools) ·
[code.claude.com](https://code.claude.com)

---

*Full TOC Draft v1.0 — compiled from all phase outputs*
*All phases complete: Vision (i1–i4), Learning Architecture
(l1–l4), Chapter Architecture (c1–c4), Scope & Market (m1–m4)*
*One blocker before production: OQ-1 (simulation domain
confirmation) and OQ-6 (Windows dictation shortcut verification)*
