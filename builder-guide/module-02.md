# Builder Guide Module 02: Learning Outcomes → Data Science Curriculum Map

**Time:** Day 1, 2:15–3:00 PM (Learning Outcomes) + Day 2, 10:15–11:00 AM (Curriculum Map & Schedule)
**Feeds:** `course-toolkit/learning-outcomes-map.md` (private) + `course-site/schedule.md` (public)
**Frameworks this module runs on:** AUC Data Science and Analytics Framework (6 outcome areas) · CSWE EPAS (2022) competencies · DSSWE 8-module data science sequence · SW-CORE (when generative/agentic AI, not just data analysis, is involved)

---

## Facilitator Notes *(remove or move to course-toolkit before publishing)*

- This module now spans an overnight gap; outcomes on Day 1 afternoon, curriculum map the next morning. Open the Day 2 session with 5 minutes for people to re-read their own outcomes doc before building the schedule on top of it; don't assume it's fresh in their heads.
- This is the session where "why integrate data science into this course" turns into something concrete. Push participants to flag *which* outcomes will be assessed via a data-science-based assignment now; even a rough guess; since Module 04 (Module Builder) picks up directly from this flag.
- **Bring real source material, not requirements.** The strongest version of this module happens when the participant brings an existing syllabus, a grant/curriculum-mapping document, or prior course data (real datasets, real assignment history) — not just a description of what they want. Adjust Claude's questions to read that material first, rather than starting from a blank-page interview.

---

## Step 0: Confirm the Participant's Track

Check which track they selected on their application before drafting anything: **Track I (New Course/Program Design)**, **Track II (Assignment Development)**, or **Track III (Course/Program Revision)**. This changes how much of this module they actually need.

- **Track I:** full session as written below; draft outcomes one at a time from scratch.
- **Track II:** they likely already have a course and syllabus, and are here to build one (or a few) new or updated assignments; not a whole course. Still have them outline a learning outcome for each assignment they're building, scoped to that assignment rather than a full 3–5-outcome course-wide pass. Ask one thing at a time, same discipline as Step 1: assignment topic first, then students' prior experience, then the data-science angle; don't stack all three into one message. If they already have course-wide outcomes, map the assignment against the existing one it serves instead of drafting new. Compress the curriculum-map step to "where does this sit in your existing schedule."
- **Track III:** they have existing outcomes to revise, not draft fresh; use the "already have outcomes" branch in Step 1. Curriculum map becomes a check-and-adjust pass, not a from-scratch sequence. This is the common case for a course that already teaches its subject and is being redesigned to integrate data science — most of CUSW 415's own build ran this way: real syllabus, real assignments, real datasets already in place, outcomes reworked to name the data-science layer explicitly rather than invented outright.

Whichever track: before moving into Module 04, each data-science-based assignment or outcome also needs a dataset or resource identified (`course-site/resources/datasets.md`); this is a prerequisite, not optional busywork. If the dataset is restricted-use (e.g., federal child welfare data via NDACAN/AFCARS/NCANDS), the terms-of-use/data-sharing agreement is also a prerequisite — flag it in the same place, don't treat it as a Module 04 problem.

**A distinction worth being explicit about, every track:** the data-science-based flag describes what *students* do to complete the assignment — using data science tools and methods themselves — not that the instructor used Claude to help build the assignment material. Conflating those is an easy trap in a fast-scoped Track II session especially. The goal is an assignment where students do data science, not just one that Claude helped write.

A second distinction, specific to this framework: **data-science-based** (students work with data — R, RStudio, Tableau, a dataset) is not the same as **AI-based** (students or the instructor use a generative/agentic AI tool as part of the workflow). An outcome can be either, both, or neither. If it's AI-based, route it through the SW-CORE check in Step 2 below — data science methodology and AI governance are related but separate concerns here.

This is what Module 03's Track I vs. Track II/III split (below, and its own facilitator notes) refers back to; don't make them re-declare it.

---

## Part 1: Learning Outcomes (Day 1, 2:15–3:00 PM)

### Step 1: Draft 3–5 outcomes

Use Claude to turn a rough sense of "what I want students to be able to do" into properly scoped outcomes, grounded in the two frameworks that govern content and competency for this design process:

- **AUC Data Science and Analytics Framework** — six learning-outcome areas any data-science-integrated outcome should draw from: (1) Mathematics & Statistics, (2) Programming, (3) Modeling, (4) Data Curation, (5) Ethics (including impact on the African diaspora, where relevant to the discipline), (6) Communication.
- **CSWE EPAS (2022)** — the accreditation competency each outcome maps to (e.g., Comp 4 Practice-Informed Research, Comp 7 Assess). If this isn't a CSWE-accredited course, substitute the relevant accreditation/competency framework for the discipline.

A useful prompt:

> *"Help me write 3-5 learning outcomes for a [course topic] course. Students range from [describe prior experience]. I want at least one outcome where students themselves work with real data — using data science tools and methods — to complete the work. Map each outcome to one of the six AUC Data Science Framework areas (Math & Stats, Programming, Modeling, Data Curation, Ethics, Communication) and to the relevant EPAS competency."*

Already have learning outcomes drafted for this course? Paste them in and ask Claude to map them against the data-science and EPAS requirements instead of starting from scratch. If a curriculum-mapping document already exists (a prior grant deliverable, a department curriculum map, a spreadsheet like a DSSWE-style module-by-module mapping), read it first and draft outcomes that are consistent with it rather than reinventing the sequence.

### Step 2: Map each outcome to an assessment type

For each outcome, note in `course-toolkit/learning-outcomes-map.md`:
- How it will be assessed (assignment, quiz, exam)
- Whether it's data-science-based, and if so, which of the 6 AUC Framework areas it draws on
- Which EPAS (or equivalent) competency it maps to
- Whether it's AI-based (uses a generative/agentic AI tool as part of the student's or instructor's workflow) — if yes, this outcome needs a SW-CORE pass before Module 04: confirm it fits one of the six stages (Design, Domain, Develop, Determine, Deliver, Deploy), that no identifiable client data is in scope, and that the AI tool is positioned as assistive to professional judgment, not a substitute for it.

**You don't need to know the technical details of the data-science assignment yet**; just flag it. Module 04 is where Claude helps you design the actual assignment, whether you code or not.

### Step 3: Fill in the table

```
| Module | Learning Outcome | Assessment | Data-Science Based? | AUC Framework Area | EPAS Competency |
|---|---|---|---|---|---|
```

---

## Part 2: Curriculum Map (Day 2, 10:15–11:00 AM)

### Step 4: Sequence your modules

Working from the outcomes table, sketch a week-by-week (or module-by-module) map. If the course is integrating data science across an existing content sequence (the common case — a content course gaining a data-science layer, not a data-science course built from zero), use the **DSSWE 8-module sequence** as the scaffold to interleave rather than replace the existing schedule:

1. Introduction to Data Science (what is data science? / framework intro)
2. Sources and Types of Data
3. Data Science Tools (e.g., RStudio/Posit, Tableau)
4. R Basics for Data Science (packages, e.g., tidyverse)
5. Data Wrangling (grammar of wrangling, merging, tidy data)
6. Data Analysis (descriptive statistics, regression, clustering)
7. Data Visualization (ggplot2, facets, boxplots/histograms/bar charts/scatterplots)
8. Ethics, Competencies, and Professional Development (Code of Ethics, role of data science in society, algorithm bias)

These 8 modules don't need their own dedicated weeks — the strongest version threads them through existing content weeks as short activities building toward a capstone data-science assignment near the end of the term. Ask Claude to help sequence, e.g.:

> *"Given these learning outcomes [paste table] and this content-week schedule [paste existing schedule], suggest where each of the 8 DSSWE data-science modules should land, noting where the culminating data-science assignment should sit."*

### Step 5: Build `course-site/schedule.md`

This is the public-facing version; topic and assignment-due-date only, no grading detail.

---

## Checkpoint

- [ ] `course-toolkit/learning-outcomes-map.md` has outcomes (3–5 for Track I, or one per assignment for Track II/III), each mapped to an assessment, an AUC Framework area (where data-science-based), and an EPAS competency
- [ ] At least one outcome flagged as data-science-based, with a dataset or resource identified for it (`course-site/resources/datasets.md`) — including a terms-of-use/data-sharing agreement if the dataset is restricted-use
- [ ] Any AI-based outcome has passed a SW-CORE check (stage identified, no identifiable client data, AI positioned as assistive not substitutive)
- [ ] `course-site/schedule.md` has a full module sequence with assignment due dates (Track I), or an updated/confirmed schedule showing where this week's assignment(s) and the DSSWE data-science modules land (Track II/III)
