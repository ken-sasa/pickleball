# OPRC Demonstration Corpus Codebook v0.3

**Status:** Demonstration-only coding manual  
**Purpose:** Test whether the Evidence Map and PR-MDS architecture can represent heterogeneous pickleball scholarship without implying systematic-review completeness.

## 1. Scientific boundary

The demonstration corpus is:

- AI-assisted;
- abstract-level unless otherwise documented;
- single-coded;
- non-systematic;
- unsuitable for estimating the prevalence of research topics or pooled effects.

The corpus tests schema behavior and metadata ambiguity. It does not substitute for a systematic search, duplicate screening, full-text verification, or independent coding.

## 2. Unit of coding

The default unit is a distinct scholarly publication. Publications known to share an underlying sample should be linked when this can be verified.

Do not infer unreported information from author affiliation, journal scope, or contextual assumptions.

## 3. Source type

Use one of:

- `journal_article`
- `review`
- `conference_paper`
- `preprint`
- `thesis_dissertation`
- `report`
- `other_scholarly`

## 4. Study design

Use the closest primary design:

- `randomized_trial`
- `quasi_experimental`
- `prospective_cohort`
- `retrospective_cohort`
- `cross_sectional`
- `case_control`
- `surveillance`
- `case_series`
- `qualitative`
- `mixed_methods`
- `measurement_validation`
- `biomechanical_lab`
- `computer_vision_ml`
- `simulation_modeling`
- `systematic_review`
- `scoping_review`
- `meta_analysis`
- `narrative_review`
- `other`

When multiple components exist, code the design that best represents the principal empirical claim and explain secondary components in `notes`.

## 5. Domain taxonomy

Use exactly one primary domain:

- `injury_safety`
- `biomechanics_performance`
- `physical_health_fitness`
- `aging_physical_function`
- `psychology_wellbeing`
- `social_connection`
- `participation_behavior`
- `education_coaching`
- `management_economics`
- `technology_ai`
- `facilities_environment`
- `policy_governance`
- `other`

Secondary domains may be pipe-separated.

## 6. Sample size and unit

`sample_size` must never be interpreted without `sample_size_unit`.

Allowed example units include:

- `participants`
- `patients`
- `cases`
- `injuries`
- `sessions`
- `matches`
- `publications`
- `other`
- `NR`

A weighted national estimate is not the analytic sample size. When a source reports both, code the unweighted analytic sample where available and place the weighted estimate in `notes` or a dedicated field.

## 7. Country

Use the location of data collection, not author affiliation. Use ISO 3166-1 alpha-3 when known. Use `MULTI` only for genuinely multinational samples and `NR` when the location is not reported in the source consulted.

## 8. Exposure and intervention

Use concise natural-language descriptions. Examples:

- `recreational pickleball participation`
- `8-week supervised pickleball program`
- `singles versus doubles match play`
- `dink-shot task recorded by video`

If a study reports duration, frequency, or intensity, preserve the reported measure without assuming that it is directly equivalent to another study's exposure definition.

## 9. Outcomes

List principal outcomes separated by semicolons. Preserve validated instrument names and units when they are reported. Do not code an outcome merely because it appears in an introduction or discussion.

## 10. Missingness

- `NA` — not applicable
- `NR` — not reported in the consulted source
- `unknown` — status could not be determined

Do not replace missingness with assumptions.

## 11. Verification status

Use:

- `single_coded`
- `double_coded_agreement`
- `double_coded_resolved`
- `audited`

All v0.3 demonstration-corpus records remain `single_coded` unless an actual independent second coding pass occurs.

## 12. Publication year

Prefer the final bibliographic publication year used by the publisher or journal issue. If online-first and issue years differ and this matters for chronological analysis, preserve both in separate metadata rather than silently switching conventions.

## 13. AI-assisted coding disclosure

The coding workflow may use an LLM to suggest structured fields, but the LLM is not an independent reviewer. `coder_id = AI_ASSISTED_SEED` indicates that the record was generated through an AI-assisted extraction workflow and has not undergone independent human verification.

## 14. Four-publication stress test

The v0.3 engineering stress test uses four heterogeneous publications to inspect whether the candidate context-and-provenance layer can represent:

1. player-survey injury epidemiology;
2. physiological/activity-intensity measurement;
3. a randomized intervention;
4. video/computer-vision kinematic analysis.

The stress test assesses schema coverage and ambiguity only. It does not validate scientific outcomes or establish PR-MDS content validity.
