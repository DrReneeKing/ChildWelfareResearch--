# Builder Guide Module 12: Containerization for Reproducibility (Optional, CS Track)

**Status: Optional, self-paced.** Not part of the live agenda; this and `module-11` are added-depth modules for instructors teaching CS/programming who want more technical substance than the general track's "AI writes the script for you" framing.

---

## Facilitator Notes *(remove or move to course-toolkit before publishing)*

- Unlike every other module, this one assumes the participant already codes. Don't offer it to non-coders.
- Point people here from the Day 5 "Using NAIRR Resources Beyond This Week" session, or whenever a CS instructor asks about reproducibility or containers specifically.
- **Get the technical framing right:** Docker itself typically can't run directly on shared HPC systems (its daemon needs root, which multi-user clusters don't grant). The Morehouse Supercomputing Facility supports **Apptainer** (formerly Singularity) instead: build and test with Docker locally, then convert to a `.sif` image to actually run on the cluster. If this module gets drafted as "just run Docker on the cluster," that's wrong and will confuse students the first time they try it.
- This reuses `module-04`'s build pattern (lecture outline → assignment → quiz → public/private split) rather than inventing a new one; if a participant hasn't done `module-04` yet, point them there first.

---

## Before You Start

Get a module number (`XX`) from the participant; this either fills a slot already on their curriculum map (`course-site/schedule.md`) or is a bonus module beyond it.

## Step 1: Lecture Outline

Cover, at minimum:
- Why reproducibility matters: "works on my machine" failures, dependency drift, and why research computing specifically cares (an unrerunnable result isn't verifiable)
- Docker locally, Apptainer on the cluster: the root-access constraint, and the build → convert → run workflow
- A concrete example: containerizing a small script with a couple of dependencies, end to end
- A wrap-up tying back to the course's HPC assignment thread

Already have material on containers? Bring it and ask your AI coding assistant to restructure it into this format.

Draft into `course-site/modules/module-XX.md` (public outline) and `course-toolkit/lecture-prep-notes/module-XX-notes.md` (full prep notes); same public/private split as `module-04`.

## Step 2: Runnable Assignment

Ask your AI coding assistant to scaffold:
1. A small script with a couple of real dependencies (something that'd plausibly break on a version mismatch)
2. A `Dockerfile` that builds a working image locally
3. The conversion step to an Apptainer `.sif` image
4. A Slurm batch script that runs the `.sif` image on the cluster (`apptainer exec` or `apptainer run`), with each line explained

Draft supplementary material (starter code, Dockerfile, setup instructions) into `course-site/resources/tools.md`.

## Step 3: Quiz

`course-toolkit/quizzes/module-XX-quiz.md`, with a full answer key. Mix conceptual questions (e.g. "why can't you just run the Docker image directly on the cluster?") with applied ones (e.g. debugging a failed Apptainer build). Stays private.

## Step 4: Public/Private Leak Check

Re-read `course-site/modules/module-XX.md`; confirm no answer keys, prep notes, or grading detail made it into the public file.

---

## Checkpoint

- [ ] Module number confirmed (curriculum-map slot or bonus module)
- [ ] Lecture outline in `course-site/modules/module-XX.md`, full prep notes in `course-toolkit/lecture-prep-notes/module-XX-notes.md`
- [ ] Dockerfile, Apptainer conversion steps, and Slurm script drafted; supplementary material in `course-site/resources/tools.md`
- [ ] Quiz with answer key in `course-toolkit/quizzes/`
- [ ] Public file re-checked for accidental private content

Pairs with `module-11` (parallel computing with MPI/OpenMP); neither depends on the other.
