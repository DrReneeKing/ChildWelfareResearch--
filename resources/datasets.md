# Datasets

## Primary dataset: KIDS COUNT Data Center

**Source:** Annie E. Casey Foundation — [datacenter.aecf.org](https://datacenter.aecf.org/)
**Access:** Free, no registration or data-use agreement required. Browse indicators one at a time, or build a custom report (state/national, by race/ethnicity where available) and export it.

This is the course's single running dataset — used across modules rather than a different dataset per assignment, so students build familiarity with one source in depth instead of re-learning a new dataset's quirks every few weeks.

**Why this one:** it's public-domain, no-code-required (students read and interpret published indicators and custom reports rather than doing raw data engineering — appropriate for an intro practice course, not a research-methods course), and it has real depth on exactly the populations this course's case material already centers: child welfare, kinship care, family economic well-being, broken out by race/ethnicity where available — which also gives the data science content a natural tie-in to the Afrocentric Perspective's attention to racial disparity.

**Where it plugs in:**

| Module | Relevant indicators | Use |
|---|---|---|
| 5 — Implementation I: Child Welfare & Family Systems | Children in foster care; kinship care rates; child poverty by race/ethnicity | Direct tie to the Sullivan–Reid (kinship care) and Torres–Bell (housing instability/poverty) case vignettes — students compare their case's dynamics against state/national indicator data |
| 6 — Implementation II: Mental Health | Children with emotional/behavioral/developmental conditions (where available) | Context for the mental-health rotation — population-level prevalence alongside the individual case-based work |
| 7 — Implementation III: Community Organizations | Economic well-being, family structure indicators by geography | Supports the community-organization rotation's needs-assessment framing |

**Usage pattern:** "pre-run, then interpret" — students are not expected to code or clean data. Either the instructor pulls a custom report ahead of time and students interpret the table/chart, or students themselves use the Data Center's own browse/custom-report interface (no download or spreadsheet manipulation required) and answer interpretation questions about it.

**Open question:** the original (pre-redesign) syllabus had a standalone "Group Data Science Project" (25% of the grade) as a capstone assignment — that's not currently built into any of the 8 redesigned modules. Decide whether this dataset becomes its own dedicated assignment (and if so, which module hosts it — Module 5 is the most natural fit given the direct topical overlap) or stays as supporting/reference material woven into existing module discussions without a separate graded deliverable.

## Secondary dataset: N-SUMHSS (National Substance Use and Mental Health Services Survey)

**Source:** SAMHSA (Substance Abuse and Mental Health Services Administration) — [samhsa.gov/data/data-we-collect/n-sumhss](https://www.samhsa.gov/data/data-we-collect/n-sumhss-national-substance-use-and-mental-health-services-survey/datafiles), microdata via [datafiles.samhsa.gov](https://www.datafiles.samhsa.gov/) (SAMHDA)
**Access:** Free, no registration or data-use agreement required for the public-use files or the pre-built Annual Detailed Tables and state profiles (PDF). Annual releases through 2024 are the most current at the time of writing.

Facility-level data (not individual-level) on every public and private substance-use and mental-health treatment facility in the U.S. — location, services offered, specialized programs (e.g., co-occurring disorders, veterans, pregnant/postpartum, LGBTQ+-specific), and payment types accepted. Formed in 2021 from the merger of the prior N-SSATS (substance use) and N-MHSS (mental health) surveys.

**Why this one:** it's facility/service-availability data, not individual clinical data — so it maps directly onto a core generalist practice skill (knowing what services actually exist and are accessible in a given area) rather than requiring interpretation of clinical/diagnostic data undergraduates aren't yet trained to read. It also has the same no-code accessibility as KIDS COUNT: the Annual Detailed Tables and state profiles are pre-built, ready to interpret without downloading or cleaning microdata.

**Where it plugs in:**

| Module | Relevant content | Use |
|---|---|---|
| 6 — Implementation II: Mental Health & Culturally Competent Practice | State-level facility counts, service types, specialized program availability | Direct tie to the Mental Health rotation — students check what services their rotation site's state/region actually offers against the Afrocentric Perspective Case Study's "Opportunities" (DIASPORA Model) step |
| 5 — Implementation I: Child Welfare & Family Systems | Substance-use treatment facility availability, programs for pregnant/postpartum clients | Ties to the Sullivan–Reid vignette (mother in residential substance-use treatment) — students can check what treatment-facility landscape a case like Renee's would actually be navigating |
| 7 — Implementation III: Community Organizations | Service-type and payment-type breakdowns by geography | Supports community resource-mapping/needs-assessment work — same "what's actually available here" framing as KIDS COUNT, applied to behavioral health specifically |

**Usage pattern:** same "pre-run, then interpret" approach as KIDS COUNT — students work from the pre-built Annual Detailed Tables/state profiles (PDF) rather than the raw public-use microdata files, unless a future, more technical assignment specifically calls for the latter.

## Tertiary dataset: CDC Household Pulse Survey — Indicators of Anxiety or Depression

**Source:** CDC/NCHS via data.cdc.gov (Socrata) — [data.cdc.gov/resource/8pt5-q6wp](https://data.cdc.gov/d/8pt5-q6wp)
**Access:** Free, public, no registration. Real-time API (JSON/CSV) — no site-blocking issues, unlike samhsa.gov, which refused automated access entirely when checked for this course.
**Already downloaded:** [`anxiety_depression_household_pulse.csv`](anxiety_depression_household_pulse.csv) — the full dataset, 16,794 rows, pulled directly from the live API on the date noted below. Opens directly in Excel.

**What it is:** Self-reported symptoms of anxiety and/or depressive disorder, surveyed roughly biweekly from April 2020 through September 2024, broken out nationally, by state, and by demographic subgroup (age, and others depending on survey wave), with 95% confidence intervals on every estimate.

**Why this one, specifically for assigned tasks (not just read-and-interpret):** unlike KIDS COUNT and N-SUMHSS above, this is genuine row-level data students can actually filter, sort, and chart themselves in Excel/Sheets — real assignments are possible here (e.g., "chart the national anxiety-or-depression trend from 2020–2024 and identify the two largest jumps," "compare the 18–29 age group to the 50–59 age group across the full time series," "pick your Mental Health rotation's state and pull its full time series"). It's also the one dataset in this set I verified end-to-end myself — API confirmed live, full row count confirmed, file downloaded and checked against the source, not reconstructed from a summary.

**Where it plugs in:** Module 6 (Mental Health & Culturally Competent Practice) — primary. Also usable in Module 2 (AI in Social Work Practice) as a hands-on example of interpreting real quantitative data before moving into qualitative/case-based work.

**Columns:** `indicator` (Anxiety / Depression / combined), `group` (National/By Age/etc.), `state`, `subgroup`, `time_period_label`, `time_period_start_date`, `time_period_end_date`, `value` (%), `lowci`, `highci`, `confidence_interval`.

**A caution for the assignment you'd build around this:** the survey methodology and question wording changed across phases (2020–2024) — flag this to students so they don't naively treat the full time series as one continuous, uniform measurement; that's itself a useful teaching point about reading government survey data critically.

