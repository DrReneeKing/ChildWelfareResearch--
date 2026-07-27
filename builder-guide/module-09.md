# Builder Guide Module 09: Publish Your Course Site

**Time:** Day 5, 10:15–11:00 AM (shared block with Modules 08 and 10; see facilitator note)
**Feeds:** Turns on GitHub Pages for `course-site`

---

## Facilitator Notes *(remove or move to course-toolkit before publishing)*

- Modules 08, 09, and 10 now share a single 45-minute block. Publishing (this module) has a hard prerequisite step; the leak check below; that shouldn't be rushed. Recommend triaging office hours setup (Module 08) quickly, capping this module at ~20 minutes, and treating Module 10 as more of a guided discussion than a hands-on build, given the time.

---

## Before you start

Publishing via GitHub Pages is one way to share your finished course site, not a requirement; you can just as easily export or hand off the material to Google Classroom, Canvas, Blackboard, or whatever LMS your institution already uses. The steps below assume you're publishing with GitHub Pages; if you're going another route, skip to your LMS's import process instead.

## Step 1: Pre-publish leak check

Before turning anything on, diff your two repos mentally (or literally, if comfortable with git) and confirm `course-site` contains none of:
- Answer keys or rubric scoring detail
- Grading scale or weighting
- Any student data, even de-identified samples
- Your private lecture prep notes

## Step 2: Turn on GitHub Pages

In `course-site` → **Settings** → **Pages** → set source branch (usually `main`) → save.

## Step 3: Verify

Visit the published URL. Click through every page; syllabus, schedule, modules, resources, office hours; confirm nothing 404s and nothing private is visible.

## Step 4: Keep it live each semester

Note what you'll need to update each term (dates, office hours link, any semester-specific policy language) so future-you isn't starting from scratch.

---

## Checkpoint

- [ ] Leak check complete; no private content in `course-site`
- [ ] GitHub Pages live and verified
- [ ] Notes on what to update each semester
