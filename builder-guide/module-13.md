# Builder Guide Module 13: ML Hub for Tapis (Optional, CS Track)

**Status: Optional, self-paced.** Not part of the live agenda; this, `module-11`, and `module-12` are added-depth modules for instructors teaching CS/programming who want more technical substance than the general track's "AI writes the script for you" framing.

---

## Facilitator Notes *(remove or move to course-toolkit before publishing)*

- Unlike every other module, this one assumes the participant already codes. Don't offer it to non-coders.
- Point people here from the Day 5 "Using NAIRR Resources Beyond This Week" session, or whenever a CS instructor asks about applied ML, model deployment, or fine-tuning specifically.
- **Get the framing right:** ML Hub for Tapis (`tapis-project/ml-hub` on GitHub) is a developer-facing REST-API framework, not a non-coder-friendly tool; it requires Git, Python 3.10+, and Docker familiarity. It's a third optional CS-track module, not a replacement for the general-track Tapis session everyone else uses (which stays simple via the interactive/batch job path).
- This reuses `module-04`'s build pattern (lecture outline → assignment → quiz → public/private split) rather than inventing a new one; if a participant hasn't done `module-04` yet, point them there first.

---

## Before You Start

Get a module number (`XX`) from the participant; this either fills a slot already on their curriculum map (`course-site/schedule.md`) or is a bonus module beyond it.

## Step 1: Lecture Outline

Cover, at minimum:
- What ML Hub adds on top of Tapis: discovering, downloading, and running inference against pre-trained models (initially via Hugging Face) without hand-building that infrastructure
- The three core pieces: Models Hub (browse/download), Inference Service (submit a request, get a prediction back), Training Engine (fine-tune on their own data)
- A concrete example: one small, well-known Hugging Face model walked through discovery → download → inference end to end
- A wrap-up tying back to the course's HPC assignment thread: why inference or fine-tuning at this scale needs HPC rather than a laptop

Already have material on applied ML/model deployment? Bring it and ask your AI coding assistant to restructure it into this format.

Draft into `course-site/modules/module-XX.md` (public outline) and `course-toolkit/lecture-prep-notes/module-XX-notes.md` (full prep notes); same public/private split as `module-04`.

## Step 2: Runnable Assignment

Ask your AI coding assistant to scaffold:
1. A small script or notebook querying the Models Hub API for a specific pre-trained model (e.g. a small classification or text model on Hugging Face)
2. An inference request against that model via the Inference Service, run on a compute node, not a login node
3. Optionally, for a more advanced assignment: a fine-tuning pass via the Training Engine on a small labeled dataset
4. A Slurm batch script wrapping whichever of the above the assignment uses, with each `#SBATCH` line explained

Draft supplementary material into `course-site/resources/`: the dataset (if any) into `datasets.md`, starter code and setup instructions into `tools.md`.

## Step 3: Quiz

`course-toolkit/quizzes/module-XX-quiz.md`, with a full answer key. Mix conceptual questions (e.g. "why does fine-tuning need HPC when inference on a pre-trained model might not?") with applied ones (e.g. reading an inference request's output/error). Stays private.

## Step 4: Public/Private Leak Check

Re-read `course-site/modules/module-XX.md`; confirm no answer keys, prep notes, or grading detail made it into the public file.

---

## Checkpoint

- [ ] Module number confirmed (curriculum-map slot or bonus module)
- [ ] Lecture outline in `course-site/modules/module-XX.md`, full prep notes in `course-toolkit/lecture-prep-notes/module-XX-notes.md`
- [ ] Model discovery, inference (and optionally fine-tuning) code drafted; supplementary material in `course-site/resources/`
- [ ] Quiz with answer key in `course-toolkit/quizzes/`
- [ ] Public file re-checked for accidental private content

Pairs with `module-11` (parallel computing) and `module-12` (containerization); none depend on each other.
