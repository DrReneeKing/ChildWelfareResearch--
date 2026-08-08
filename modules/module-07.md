# Module 07: Foster Care Systems & Hands-On Data Wrangling

**Weeks:** 16–18 (Fri 11/6/26, Fri 11/13/26, Mon 11/16/26 async)

## Overview

This is the busiest data-science stretch of the semester: three DSSWE modules (Tools, R Basics, Data Wrangling) compress into two class weeks, running alongside content on aging out of care and the foster/kinship/permanency system. Students move from "no coding" to actually opening RStudio and running real code on real child welfare data for the first time.

## Learning Outcome

Describe the transition experience for youth aging out of care and the permanency planning process for foster and kinship families; demonstrate basic proficiency navigating RStudio/Posit and performing initial data wrangling on a child welfare dataset.

## Week 16 (11/6/26) — Aging Out & Treatment

- Aging out: transitioning youth to adulthood without a permanent family — challenges, supports, and outcomes
- Treatment approaches for physical abuse and neglect

## Week 17 (11/13/26) — Kinship Foster Care & Permanency Planning + DSSWE Modules 3–5

- Kinship foster care: placing children with relatives rather than non-relative foster families
- Permanency planning: the legal and practice process for achieving a stable, permanent placement
- Foster and adoptive parents: recruitment, support, and challenges
- **Data Science Activities #2–#4:** creating a data science project in R using child welfare data (the GCBS practice dataset — see `resources/datasets.md`); annotating R script code; importing data into RStudio. See [Working Directory & Projects](../resources/r-rstudio-reference-guide.html#directory) and [Writing & Running a Script](../resources/r-rstudio-reference-guide.html#script) in the reference guide.

## Week 18 (11/16/26, asynchronous) — DSSWE Modules 5–7 Continued

- **Data Science Activities #5–#8:** selecting and filtering data; using `$`, `%in%`, `group_by()`, and `summarize()`; data visualization with ggplot2; organizing project files. See [tidyverse Core Verbs](../resources/r-rstudio-reference-guide.html#tidyverse) in the reference guide.
- **AI touchpoint (Week 18):** once Activity #7's ggplot2 visualization is built, ask the course-approved AI tool to help describe or interpret it in plain language (e.g., a county-level caseload chart) — then check the AI's reading against what the visualization actually shows. A quick, practical rehearsal for the Module 03 AI Ethics assignment's accuracy-checking habit, now applied to your own data instead of a general topic.

## Readings

- *Introduction to Child Welfare* — chapters on aging out and permanency planning
- *R for Data Science* — chapters on data import, tidy data, and data transformation (dplyr basics)

## Assignments

| Assignment | Due | Worth |
|---|---|---|
| Concept Map: Aging Out / Treatment | ~11/6/26 | Part of Chapter Summaries/Concept Maps (20% combined) |
| Concept Map: Kinship Foster Care / Permanency Planning | ~11/13/26 | Part of Chapter Summaries/Concept Maps (20% combined) |
| Data Science Activities #2–#4 (RStudio project setup, R script, data import) | 11/13/26 | Part of Data Science Project (20% combined) |
| Data Science Activities #5–#8 (filtering, wrangling, visualization, file organization) | 11/16/26 | Part of Data Science Project (20% combined) |

## Checklist

- [ ] Complete both concept maps
- [ ] Complete Data Science Activities #2–#4 — get your R project set up and data imported
- [ ] Complete Data Science Activities #5–#8 — practice filtering, wrangling, and a first visualization
- [ ] Try the AI touchpoint: have the course-approved AI tool describe your Activity #7 visualization, then check its reading against your actual chart
- [ ] If any RStudio/Posit setup issues surface, reach out to the instructor now — this is the densest hands-on stretch of the semester

## Competency

Comp 7 (Assess) via permanency-planning case analysis; this module is also where the AUC Data Science Framework's Programming and Data Curation areas get their first real hands-on assessment.

## Data Science Tie-In

This is the heart of the semester's data-science skill-building, compressed into a short window by design (per the DSSWE curriculum sequence) so students hit R basics, wrangling, and an early visualization back-to-back while momentum is high. Consistent with lessons learned from prior DSSWE cohorts: if students are going to feel overwhelmed, it's here — budget extra office-hours time and point students to the GCBS practice dataset (not the restricted AFCARS data) for this hands-on stretch, saving the real federal data for the Module 09 capstone.
