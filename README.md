# course-site

**This repo is PUBLIC.** Everything here is visible to the world the moment GitHub Pages is turned on (planned: Day 5 of the accelerator, not before). Publishing via GitHub Pages is one option for sharing your finished course site, not a requirement; you can just as easily export or hand off the material to Google Classroom, Canvas, Blackboard, or whatever LMS your institution already uses.

Before publishing, double-check:
- No grading keys, rubrics, or student data have leaked in from `course-toolkit`
- No personal contact info beyond what you intend to share publicly
- Links to `course-toolkit` content are removed or replaced with public-safe versions

Already teaching a version of this course? Bring what you have; upload or paste your existing syllabus, learning outcomes, or assignments at any point, and Claude will adapt them instead of you starting from a blank template.

## Why repo structure matters

This folder isn't just storage; it's the environment Claude works inside as you build this course. See the root `CLAUDE.md` for how Claude should operate here, and `skills/` for the step-by-step guides it reads before walking you through each module; keeping both current is what makes every prompt you write more effective.

## What's in here
| File/Folder | Purpose |
|---|---|
| `_config.yml` | GitHub Pages / Jekyll site config |
| `index.md` | Course homepage, FAQs |
| `syllabus.md` | Published syllabus |
| `schedule.md` | Curriculum map / weekly schedule |
| `modules/` | One file per module: overview, slides link, assignments, notebook templates |
| `office-hours.md` | Booking link (Calendly/Teams) + policy |
| `resources/` | Supplementary materials, split by type: `datasets.md`, `tools.md`, `references.md` |
| `builder-guide/` | The SLM walkthrough (Modules 00–10, plus optional CS-track Modules 11–13); step-by-step instructions for building this course |
