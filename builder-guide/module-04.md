# Builder Guide Module 04: Module Builder

**Time:** Part 1; Day 2, 2:30–3:00 PM (Lecture Outline + Slide Deck) · Part 2; Day 3, 11:00 AM–12:30 PM (Quiz + Assignment Supplementary Material) · Part 3; Day 4, 2:30–3:00 PM (Finish Building Your Module)
**Feeds:** `course-site/modules/module-XX.md` (public outline) + `course-toolkit/lecture-prep-notes/module-XX-notes.md` (private, full notes) + `course-toolkit/quizzes/` (private, with answer key) + `course-site/resources/` (public: `datasets.md`, `tools.md`)

---

## Facilitator Notes *(remove or move to course-toolkit before publishing)*

- Day 3, 10:30–11:00 AM ("Using an AI coding assistant for API data extraction, moving data onto HPC") isn't assigned a Builder Guide module number, but it sits right before this arc's Part 2 and is where the HPC-specific piece of the assignment actually gets built. Point participants there as the natural bridge into Part 2 below.
- This is the session where the coder/non-coder split matters most; see the callout in each part.

---

## Before You Start

Pick **one module** from your curriculum map (`course-site/schedule.md`) to build fully, end to end, as a repeatable template. You'll reuse this same process for every other module later; the point of building one *fully* this week is to have a pattern to copy.

**Track II participants** often already know exactly which assignment they came here to build, rather than picking generically from a curriculum map; if so, skip the "pick one module" framing and just confirm which existing course/unit it belongs to. This module is their main goal for the week.

**Before scaffolding anything, confirm a dataset or resource is identified** (`course-site/resources/datasets.md`). This applies to every track, not just Track I; an HPC-based assignment without an identified dataset isn't buildable yet. If this hasn't happened yet, do it now — see the Dataset Discovery walkthrough — before Step 1.

---

## Part 1: Lecture Outline + Slide Deck (Day 2, 2:30–3:00 PM)

### Step 1: Outline the module

Ask Claude to draft a lecture outline from your learning outcome for this module:

> *"Draft a lecture outline for [module topic], covering [outcome]. Include a short intro, 2-3 core concepts, and a wrap-up tying to the HPC assignment."*

Already have lecture notes or slides for this module? Bring them, and ask Claude to restructure them into this format rather than starting over.

### Step 2: Build the slide deck

Source lives in Canva or Slides (per your institution's setup); export a PDF and archive it in the repo once done.

- **If you code:** you can also have Claude generate a deck directly (e.g., via `pptxgenjs`) if you'd rather work from a script than a GUI.
- **If you don't code:** stick with Canva/Slides; Claude can still help you write the outline and speaker notes that go into it.

### Step 3: Split public vs. private

- `course-site/modules/module-XX.md` → student-facing outline, slides link, assignment link
- `course-toolkit/lecture-prep-notes/module-XX-notes.md` → your full prep notes (talking points, timing, anything not meant for students)

---

## Part 2: Quiz + Assignment Supplementary Material (Day 3, 11:00 AM–12:30 PM)

*(Bridge in: Day 3, 10:30–11:00 AM covers moving data onto HPC and using an AI coding assistant for API data extraction; that's the technical backbone for the assignment you're building supplementary material for here.)*

### Step 4: Build the quiz

In `course-toolkit/quizzes/module-XX-quiz.md`, with a full answer key. This stays private.

### Step 5: Build the assignment's supplementary material

First, a question separate from your own coding comfort: **do the students in this course code?** This decides the assignment's structure, not just how you build it; ask it explicitly rather than assuming it tracks your own answer.

- **Students code:** they get a starter notebook/script with clear TODOs to complete themselves, submitted as their own batch/interactive job; the normal case.
- **Students don't code:** don't hand them something to edit as code. Two patterns work well instead:
  - **Pre-run, then interpret:** you (or Claude) run the computation ahead of time; students receive the output; plots, tables, job logs; and the assignment is entirely about interpreting and reasoning about it.
  - **Config-only:** students get a notebook where the only thing they touch is one or two clearly labeled input values (a date range, a sample size, a threshold); they change the value, click Run All, and never read or write code as code.
  Either way, the graded deliverable becomes understanding and reasoning (e.g. *"the job took 40 minutes on 1 node vs. 6 on 8; why?"*), not code correctness.

In `course-site/resources/`: the dataset into `datasets.md`, setup instructions and any tools/software into `tools.md`, and which pattern above this assignment uses alongside whichever of the two it's most relevant to.

If you already have an assignment written for this module, upload or paste it and have Claude adapt it rather than drafting from nothing.

Then, based on your own coding comfort:
- **If you code:** ask Claude to scaffold the actual assignment notebook/script now, so the quiz and supplementary material reference something concrete.
- **If you don't code:** describe the assignment goal and dataset to Claude and have it draft the starter notebook/script *and* a plain-language explanation you can hand to students (and use yourself to write the quiz).

---

## Part 3: Finish Building Your Module (Day 4, 2:30–3:00 PM)

### Step 6: Close any gaps

Cross-check: does `course-site/modules/module-XX.md` link to everything (slides, assignment, quiz link; not the quiz *content*, that stays private)?

### Step 7: Public/private leak check

Before moving on, re-read `course-site/modules/module-XX.md` and confirm no answer keys, grading notes, or private prep content made it into the public file.

---

## Checkpoint

- [ ] Lecture outline + slide deck built and linked in `course-site/modules/module-XX.md`
- [ ] Full prep notes in `course-toolkit/lecture-prep-notes/module-XX-notes.md`
- [ ] Quiz with answer key in `course-toolkit/quizzes/`
- [ ] Dataset identified in `course-site/resources/datasets.md`, tools/setup instructions in `resources/tools.md`
- [ ] Public file re-checked for accidental private content
