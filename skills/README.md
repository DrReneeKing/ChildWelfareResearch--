# Skills

Reusable `SKILL.md` instructions Claude understands, one folder per Builder Guide module. Together they are **Compass**; the interactive walkthrough that replaces reading the static `builder-guide/module-XX.md` files on your own.

| Skill | Use it to | Feeds |
|---|---|---|
| `module-00-01` | Set up your two repos and connect Claude Code; **start here** | environment only |
| `module-02` | Draft learning outcomes, then build your curriculum map | `course-toolkit/learning-outcomes-map.md`, `course-site/schedule.md` |
| `module-03` | Draft your syllabus | `course-site/syllabus.md` |
| `module-04` | Build one module fully: lecture outline, quiz, assignment material | `course-site/modules/module-XX.md`, `course-toolkit/lecture-prep-notes/`, `course-toolkit/quizzes/`, `course-site/resources/` |
| `module-05` | Draft your grading scale and rubrics | `course-toolkit/grading-scale.md`, `course-toolkit/rubrics/` |
| `module-06` | Draft your exam scaffold | `course-toolkit/exams/` |
| `module-07` | *(optional, self-paced)* AI for grading & attendance feedback | `course-toolkit/grading-and-attendance/` |
| `module-08` | Set up office hours booking + policy | `course-site/office-hours.md` |
| `module-09` | Pre-publish leak check, then turn on GitHub Pages | n/a |
| `module-10` | Reuse this template for your next course or cohort | n/a |
| `module-11` | *(optional, self-paced, CS track)* Build a module on parallel computing (MPI/OpenMP) | `course-site/modules/module-XX.md`, `course-toolkit/lecture-prep-notes/`, `course-toolkit/quizzes/`, `course-site/resources/` |
| `module-12` | *(optional, self-paced, CS track)* Build a module on containerization for reproducibility (Docker → Apptainer) | `course-site/modules/module-XX.md`, `course-toolkit/lecture-prep-notes/`, `course-toolkit/quizzes/`, `course-site/resources/` |
| `module-13` | *(optional, self-paced, CS track)* Build a module on ML Hub for Tapis (model discovery, inference, fine-tuning) | `course-site/modules/module-XX.md`, `course-toolkit/lecture-prep-notes/`, `course-toolkit/quizzes/`, `course-site/resources/` |

A `SKILL.md` is a markdown file with a short YAML header (`name`, `description`) followed by step-by-step instructions for an AI assistant to follow in conversation with you. Each one assumes `course-site` and `course-toolkit` are cloned as sibling folders and opened together (see `module-00-01`).

## How to use a skill (any tool)

- **Claude Code / Cursor:** open the repo and say "use the module-02 skill," or just describe what you're working on. The AI reads the matching `SKILL.md`; `CLAUDE.md` points it here.
- **VS Code + Copilot:** open the relevant `skills/module-XX/SKILL.md` and reference it in your prompt.
- **Claude on the web:** upload or paste the `SKILL.md` (plus whatever file you're filling in) into the chat.

Prefer reading instead of talking it through? The same content, written for a human facilitator to read and run live, lives in `../builder-guide/module-XX.md`.
