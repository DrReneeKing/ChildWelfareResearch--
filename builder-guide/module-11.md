# Builder Guide Module 11: Parallel Computing with MPI & OpenMP (Optional, CS Track)

**Status: Optional, self-paced.** Not part of the live agenda; this and `module-12` are added-depth modules for instructors teaching CS/programming who want more technical substance than the general track's "AI writes the script for you" framing.

---

## Facilitator Notes *(remove or move to course-toolkit before publishing)*

- Unlike every other module, this one assumes the participant already codes. Don't offer it to non-coders; it isn't a fit and will just be frustrating.
- Point people here from the Day 5 "Using NAIRR Resources Beyond This Week" session, or whenever a CS instructor asks whether the accelerator has anything with more technical depth.
- This reuses `module-04`'s build pattern (lecture outline → assignment → quiz → public/private split) rather than inventing a new one; if a participant hasn't done `module-04` yet, point them there first so the pattern is familiar.

---

## Before You Start

Get a module number (`XX`) from the participant; this either fills a slot already on their curriculum map (`course-site/schedule.md`) or is a bonus module beyond it.

## Step 1: Lecture Outline

Cover, at minimum:
- Shared-memory (OpenMP) vs. distributed-memory (MPI) parallelism, and why the distinction matters once code moves from a laptop to a multi-node cluster
- When to reach for which: OpenMP for parallelizing loops within a single node's cores; MPI for spreading work across multiple nodes
- A concrete example (e.g. parallel sum or matrix multiply) shown in both models
- A wrap-up tying back to the course's HPC assignment thread

Already have material on parallel computing? Bring it and ask your AI coding assistant to restructure it into this format.

Draft into `course-site/modules/module-XX.md` (public outline) and `course-toolkit/lecture-prep-notes/module-XX-notes.md` (full prep notes); same public/private split as `module-04`.

## Step 2: Runnable Assignment

Ask your AI coding assistant to scaffold:
1. A small, parallelizable problem in serial form (a deliberately slow baseline)
2. An OpenMP version (e.g. `#pragma omp parallel for` in C, or a threaded equivalent)
3. An MPI version (e.g. `mpi4py` in Python, or `MPI_Send`/`MPI_Recv` in C)
4. A Slurm batch script for each version, with each `#SBATCH` line explained; pay particular attention to `--ntasks` vs. `--cpus-per-task`, since a script that mismatches these will run without erroring but won't actually parallelize

Draft supplementary material into `course-site/resources/`: the dataset (if any) into `datasets.md`, starter code and setup instructions into `tools.md`.

## Step 3: Quiz

`course-toolkit/quizzes/module-XX-quiz.md`, with a full answer key. Mix conceptual questions (e.g. "why didn't this OpenMP code speed up on 8 cores?") with applied ones (e.g. reading a Slurm job's wall-clock output). Stays private.

## Step 4: Public/Private Leak Check

Re-read `course-site/modules/module-XX.md`; confirm no answer keys, prep notes, or grading detail made it into the public file.

---

## Checkpoint

- [ ] Module number confirmed (curriculum-map slot or bonus module)
- [ ] Lecture outline in `course-site/modules/module-XX.md`, full prep notes in `course-toolkit/lecture-prep-notes/module-XX-notes.md`
- [ ] OpenMP + MPI starter code and Slurm scripts drafted in `course-site/resources/tools.md`; dataset (if any) in `resources/datasets.md`
- [ ] Quiz with answer key in `course-toolkit/quizzes/`
- [ ] Public file re-checked for accidental private content

Pairs with `module-12` (containerization for reproducibility); neither depends on the other.
