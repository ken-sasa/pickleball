# Pickleball Evidence Map — Coding Manual v0.1

**Status:** Candidate coding manual  
**Purpose:** Make study-level evidence extraction reproducible and auditable.

## 1. Unit of coding

The default unit is a distinct scholarly study or report. Multiple publications from the same underlying sample may receive separate publication records but should be linked when the shared sample is known.

Do not infer unreported information from author affiliation, journal scope, or contextual assumptions.

## 2. Inclusion scope

The Evidence Map is intended to cover scholarly work in which pickleball is a substantive object, exposure, intervention, setting, performance task, or analytical domain.

Eligible source types may include:

- journal articles;
- conference papers/proceedings;
- theses/dissertations;
- preprints;
- reports with identifiable methods;
- systematic/scoping reviews and meta-analyses.

News articles, product pages, promotional material, and unsourced commentary should not be entered as scholarly evidence records.

## 3. Core coding taxonomy

### Source type

Use one of:

- `journal_article`
- `conference_paper`
- `preprint`
- `thesis_dissertation`
- `report`
- `review`
- `other_scholarly`

### Study design

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

When a paper contains multiple components, code the design that best represents the principal empirical claim and describe secondary components in `notes`.

### Primary domain

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

Additional domains may be pipe-separated in `domains_secondary`.

## 4. Population coding

`population_description` should preserve the authors' description in concise normalized language.

Do not translate a convenience sample into a broader population claim. For example, a study of players at one tournament is not automatically representative of national competitive players.

`sample_size` should represent the main analytic sample when unambiguous. If multiple samples exist, record the principal sample and explain in `notes`.

## 5. Country coding

Use ISO 3166-1 alpha-3 codes for the location of data collection, not author affiliation.

For multinational studies, use pipe-separated country codes if all are known. Use `MULTI` only when the source identifies a multinational sample but country-level locations cannot be represented cleanly.

## 6. Exposure/intervention and comparator

Use concise natural-language descriptions rather than over-compressed labels.

Examples:

- `8-week pickleball program`
- `regular recreational pickleball participation`
- `pickleball match play`
- `forehand stroke task`

Use `NA` when a comparator is genuinely not applicable; use `NR` if a comparator should exist but is not reported.

## 7. Outcomes

List principal outcomes separated by semicolons. Preserve validated instrument names when relevant.

Examples:

- `injury incidence; body region; mechanism`
- `loneliness; social connectedness`
- `dynamic balance; gait speed`
- `serve accuracy; ball velocity`

Do not code an outcome merely because it appears in the introduction or discussion.

## 8. Open-science fields

For `preregistered`, `open_data`, and `open_code`, use:

- `yes`
- `no`
- `unknown`

Code `yes` only when a usable registration, data resource, or code resource is actually identified.

## 9. Funding and conflicts

For `funding_reported` and `conflict_of_interest_reported`, use `yes`, `no`, or `unknown` to indicate whether the publication reports a statement—not whether the coder believes a conflict exists.

## 10. Screening status

`inclusion_status`:

- `included`
- `excluded`
- `pending`
- `duplicate`

If excluded, populate `exclusion_reason` using one of:

- `not_pickleball_substantive`
- `not_scholarly_source`
- `no_methods_or_data`
- `duplicate_publication`
- `not_retrievable`
- `outside_scope`
- `other`

## 11. Verification status

Use:

- `single_coded`
- `double_coded_agreement`
- `double_coded_resolved`
- `audited`

Version 0.1 should not imply that single-coded records have independent verification.

## 12. Missingness

Use:

- `NA` — not applicable
- `NR` — not reported in the source
- `unknown` — status could not be determined

Do not replace missingness with assumptions.

## 13. Reliability pilot

Before the Evidence Map is treated as a stable research resource:

1. independently double-code a non-trivial sample;
2. quantify agreement for categorical variables;
3. inspect disagreements in domain and design classification;
4. revise ambiguous definitions;
5. document adjudication rules.

## 14. Provenance rule

Every included record should remain traceable to a bibliographic identifier or source. Coding changes should be attributable through Git history or another versioned audit trail.
