# Builder Guide Module 02: Learning Outcomes → Curriculum Map

**Time:** Day 1, 2:15–3:00 PM (Learning Outcomes) + Day 2, 10:15–11:00 AM (Curriculum Map & Schedule)
**Feeds:** `course-toolkit/learning-outcomes-map.md` (private) + `course-site/schedule.md` (public)

---

## Facilitator Notes *(remove or move to course-toolkit before publishing)*

- This module now spans an overnight gap; outcomes on Day 1 afternoon, curriculum map the next morning. Open the Day 2 session with 5 minutes for people to re-read their own outcomes doc before building the schedule on top of it; don't assume it's fresh in their heads.
- This is the session where "Why HPC?" (Day 1, 2:00–2:15, right before this block) turns into something concrete. Push participants to flag *which* outcomes will be assessed via an HPC-based assignment now; even a rough guess; since Module 04 (Module Builder) picks up directly from this flag.

---

## Step 0: Confirm the Participant's Track

Check which track they selected on their application before drafting anything: **Track I (New Course/Program Design)**, **Track II (Assignment Development)**, or **Track III (Course/Program Revision)**. This changes how much of this module they actually need.

- **Track I:** full session as written below; draft outcomes one at a time from scratch.
- **Track II:** they likely already have a course and syllabus, and are here to build one (or a few) new or updated assignments; not a whole course. Still have them outline a learning outcome for each assignment they're building, scoped to that assignment rather than a full 3–5-outcome course-wide pass. Ask one thing at a time, same discipline as Step 1: assignment topic first, then students' prior experience, then the HPC+AI angle; don't stack all three into one message. If they already have course-wide outcomes, map the assignment against the existing one it serves instead of drafting new. Compress the curriculum-map step to "where does this sit in your existing schedule."
- **Track III:** they have existing outcomes to revise, not draft fresh; use the "already have outcomes" branch in Step 1. Curriculum map becomes a check-and-adjust pass, not a from-scratch sequence.

Whichever track: before moving into Module 04, each HPC-based assignment or outcome also needs a dataset or resource identified (`course-site/resources/datasets.md`); this is a prerequisite, not optional busywork.

**A distinction worth being explicit about, every track:** the HPC-based (and AI-based) flag describes what *students* do to complete the assignment — using HPC resources and AI tools themselves — not that the instructor used Claude to help build the assignment material. Conflating those is an easy trap in a fast-scoped Track II session especially. The goal is an assignment where students use HPC + AI, not just one that Claude helped write.

This is what Module 03's Track I vs. Track II/III split (below, and its own facilitator notes) refers back to; don't make them re-declare it.

---

## Part 1: Learning Outcomes (Day 1, 2:15–3:00 PM)

### Step 1: Draft 3–5 outcomes

Use Claude to turn a rough sense of "what I want students to be able to do" into properly scoped outcomes. A useful prompt:

> *"Help me write 3-5 learning outcomes for a [course topic] course. Students range from [describe prior experience]. I want at least one outcome where students themselves use HPC resources and an AI coding assistant to complete the work."*

Already have learning outcomes drafted for this course? Paste them in and ask Claude to map them against the HPC requirement instead of starting from scratch.

### Step 2: Map each outcome to an assessment type

For each outcome, note in `course-toolkit/learning-outcomes-map.md`:
- How it will be assessed (assignment, quiz, exam)
- Whether it's HPC-based

**You don't need to know the technical details of the HPC assignment yet**; just flag it. Module 04 is where Claude helps you design the actual assignment, whether you code or not.

### Step 3: Fill in the table

```
| Module | Learning Outcome | Assessment | HPC-Based? |
|---|---|---|---|
```

---

## Part 2: Curriculum Map (Day 2, 10:15–11:00 AM)

### Step 4: Sequence your modules

Working from the outcomes table, sketch a week-by-week (or module-by-module) map. Ask Claude to help sequence; e.g.:

> *"Given these learning outcomes [paste table], suggest a logical order across N weeks, noting where the HPC-based assignment should land."*

### Step 5: Build `course-site/schedule.md`

This is the public-facing version; topic and assignment-due-date only, no grading detail.

---

## Checkpoint

- [ ] `course-toolkit/learning-outcomes-map.md` has outcomes (3–5 for Track I, or one per assignment for Track II/III), each mapped to an assessment
- [ ] At least one outcome flagged as HPC-based, with a dataset or resource identified for it (`course-site/resources/datasets.md`)
- [ ] `course-site/schedule.md` has a full module sequence with assignment due dates (Track I), or an updated/confirmed schedule showing where this week's assignment(s) land (Track II/III)
