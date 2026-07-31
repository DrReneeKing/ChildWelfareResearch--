# Builder Guide Module 14: Build Your LMS Presence (Optional, Self-Paced)

**Status: Optional, self-paced.** Not part of the live agenda. Deepens `module-08`'s brief "export to Canva/Blackboard" step into a full branded build: real institution colors, a reusable HTML design system, per-module pages matching your actual LMS structure, branded slide decks, and instructor guides.

---

## Facilitator Notes *(remove or move to course-toolkit before publishing)*

- Requires at least one fully-built module (`module-04`) before there's real content to work with here.
- This produces a *lot* of material across a full course — set the expectation that it's a multi-session effort, not a single sitting, and that the participant should validate one module fully before letting their AI assistant replicate the pattern across the rest.
- If the participant already has a live Canvas (or other LMS) course, point them at exporting a Common Cartridge and reading its actual page-naming convention *before* any design work starts — matching what already exists matters more than a fresh design.

---

## Step 0: Match your real LMS structure (if you have one)

Export a Common Cartridge from your existing course (Canvas: Settings → Export Course Content). Unzip it; `course_settings/module_meta.xml` shows your real module/page structure, and the `wiki_content/` HTML files show your actual page-naming convention. Build to match this, not a structure invented from scratch. Starting fresh? Default to: Overview, Introduction, Learning Outcomes, Readings, Checklist, Assignments per module — confirm with your AI assistant before it builds anything.

## Step 1: Real brand identity

Have your assistant verify your institution's actual brand colors (hex codes, sourced — not guessed) and pick real webfonts that fit your subject.

## Step 2: One shared design system

A single CSS block, pasted into every page — light and dark theme, real typography. Built around **dropdowns, blocks, and callouts** rather than decorative icons, unless you specifically want icons.

## Step 3: One module's full page set

Built from real content already in `course-site/modules/module-XX.md` and `course-toolkit/lecture-prep-notes/`. Preview it before letting your assistant build the rest.

## Step 4: Slide decks

One deck per module or per week — your call. Branded, with real charts for real data (e.g., your actual grading weights), not static images.

## Step 5: Instructor's Guide

One document per module pulling together the outcome, reading, assignment, session timing, talking points, and misconceptions — built so a colleague or GTA could teach from it cold.

## Step 6: Replicate

Once you've approved the first module's full set, have your assistant repeat it for the rest.

---

## Checkpoint

- [ ] Brand colors verified, design system built (dropdown/block/callout, not icons, unless requested)
- [ ] Real LMS structure matched (or a default confirmed)
- [ ] One module's page set, slide deck, and Instructor's Guide built and reviewed
- [ ] Remaining modules replicated from the validated template

Reusable for your next course: same steps, new institution/brand/content inputs.

## Full documentation for faculty

An Overview, User Guide, How-To quickstart, a reusable blank "Instructions for Input" checklist (with Faculty Input Needed call-outs and a per-module progress-status tracker), a filled-in worked example, and APA citations for both the AI assistance used and the redesigned course itself live in the sibling folder `4 Course Design Assistant - User Guide/` — outside both repos, written for a human to read directly rather than for an AI assistant to execute.
