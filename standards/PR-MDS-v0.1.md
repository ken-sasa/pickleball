# Pickleball Research Minimum Data Set (PR-MDS) v0.1

**Status:** Candidate specification for pilot testing  
**Version:** 0.1  
**Date:** 2026-08  
**Project:** Open Pickleball Research Commons

## 1. Purpose

The Pickleball Research Minimum Data Set (PR-MDS) is a proposed common data layer for empirical pickleball research.

It is not intended to make every study collect the same outcomes. Its purpose is to make independently collected datasets easier to understand, compare, pool, replicate, and reuse by defining:

1. a **small common core**;
2. optional domain modules;
3. common missing-value and provenance rules;
4. explicit distinctions between observed, reported, coded, and derived variables.

Version 0.1 is a draft for field testing. It should not be described as an established international standard.

## 2. Design rule

> **Minimum common core, extensible modules.**

A field belongs in the Core only when it is broadly useful across study types, reasonably low burden, and important for interpretation or interoperability.

Study-specific variables remain welcome. PR-MDS compatibility does not require a study to restrict itself to PR-MDS fields.

## 3. Data model

PR-MDS assumes that research data may contain several linked units:

- **Study** — research project or protocol
- **Site** — institution, club, court, event, or other data-collection location
- **Participant** — pseudonymized research participant
- **Session** — bounded playing or measurement episode
- **Match/Game** — competitive or recreational game unit
- **Rally** — optional fine-grained performance unit
- **Event** — optional injury, social-interaction, or other event record

Stable pseudonymous identifiers should be used to link tables. Direct personal identifiers should not be placed in openly shared research datasets.

## 4. Core variables

The machine-readable dictionary is in `pr-mds-v0.1.csv`.

### A. Provenance core

| Variable | Requirement | Definition |
|---|---|---|
| `record_id` | REQUIRED | Unique row/record identifier within the dataset |
| `study_id` | REQUIRED | Stable identifier for the study or protocol |
| `protocol_version` | REQUIRED | Version of the data-collection protocol used |
| `site_id` | RECOMMENDED | Pseudonymous or public site identifier |
| `collection_date` | REQUIRED* | ISO 8601 date; may be generalized for public release when disclosure risk exists |
| `country_iso3` | REQUIRED | ISO 3166-1 alpha-3 country code for the data-collection site |
| `data_source_type` | REQUIRED | `participant_report`, `observer`, `device`, `video`, `administrative`, `derived`, or `mixed` |

`*` A less precise public-release date may be used if the exact date creates disclosure risk, but the transformation must be documented.

### B. Participant core

| Variable | Requirement | Definition |
|---|---|---|
| `participant_id` | REQUIRED for participant-level data | Pseudonymous participant identifier |
| `age_band` | RECOMMENDED | Standard age band; do not infer if not collected |
| `dominant_hand` | RECOMMENDED | `right`, `left`, `ambidextrous`, `other`, `unknown` |
| `pickleball_experience_months` | RECOMMENDED | Months since regular pickleball participation began |
| `skill_rating_system` | CONDITIONAL | Rating system name if a formal or structured rating is reported |
| `skill_rating_value` | CONDITIONAL | Rating value paired with `skill_rating_system` |
| `prior_racket_paddle_sport` | RECOMMENDED | Whether participant reports prior racket/paddle-sport experience |

Demographic variables such as sex, gender, race/ethnicity, disability, or socioeconomic measures can be scientifically important but are not universal Core requirements in v0.1 because definitions, sensitivity, relevance, and legal/ethical handling vary across studies and jurisdictions. Studies should collect and report them when justified by their research question and governance framework.

### C. Session/exposure core

| Variable | Requirement | Definition |
|---|---|---|
| `session_id` | REQUIRED for session-level data | Stable session identifier |
| `session_type` | REQUIRED | `practice`, `recreational_play`, `competition`, `measurement`, `lesson`, `other` |
| `play_format` | RECOMMENDED | `singles`, `doubles`, `mixed`, `not_applicable` |
| `indoor_outdoor` | RECOMMENDED | `indoor`, `outdoor`, `mixed`, `unknown` |
| `session_duration_min` | RECOMMENDED | Total session duration in minutes |
| `active_play_duration_min` | OPTIONAL | Estimated or measured active playing time |
| `games_played` | RECOMMENDED | Number of games completed in the session |

## 5. Standard age bands

When exact age is not required for analysis or cannot be shared safely, use:

- `<18`
- `18-24`
- `25-34`
- `35-44`
- `45-54`
- `55-64`
- `65-74`
- `75-84`
- `85+`
- `NR`

Researchers may retain exact age in controlled data while publishing a derived age band. The derivation must be documented.

## 6. Optional modules

### 6.1 Performance module

Candidate variables include:

- `match_id`
- `game_id`
- `rally_id`
- `point_outcome`
- `rally_shots`
- `rally_duration_sec`
- `serve_attempts`
- `serve_legal`
- `return_in_play`
- `third_shot_type`
- `shot_type`
- `unforced_error`
- `winner`
- `player_position_x`
- `player_position_y`

Fine-grained event definitions should be validated before promotion into a stable module.

### 6.2 Health and safety module

Candidate variables include:

- `injury_event`
- `injury_onset`
- `body_region`
- `injury_mechanism`
- `medical_attention`
- `time_loss_days`
- `pain_score`
- `fatigue_score`
- `fall_event`

Health variables require appropriate ethics, privacy, and measurement governance.

### 6.3 Social connection module

Candidate variables include:

- `partner_known_before_session`
- `new_person_interacted_with`
- `new_contact_count`
- `repeat_partner_intent`
- `post_session_contact_exchange`
- `subsequent_joint_play`
- `belonging_measure_name`
- `belonging_score`
- `loneliness_measure_name`
- `loneliness_score`
- `intergenerational_contact`

These fields support the Pickleball as Social Technology research program. Claims about tie formation or causal social effects require designs that distinguish exposure, selection, and outcome.

### 6.4 Physical-function module

Candidate variables include:

- balance tests;
- mobility tests;
- reaction-time measures;
- agility measures;
- heart-rate measures;
- perceived exertion;
- physical-activity measures.

The exact instrument, version, unit, and administration protocol must accompany any score.

## 7. Missing-value rules

Do not encode missingness with arbitrary numeric values such as `-1`, `99`, or `999` unless a legacy instrument requires them.

Recommended textual codes are:

- `NA` — not applicable
- `NR` — not reported / not collected
- `UNK` — unknown despite attempted ascertainment
- blank — permitted only when the dataset documentation explicitly defines blank as missing

Do not infer values from contextual clues when the variable was not measured.

## 8. Provenance classes

Every analytically important variable should be classifiable as one of:

- **OBSERVED** — directly observed by a trained or designated observer
- **SELF_REPORTED** — reported by a participant
- **DEVICE_MEASURED** — generated by a sensor or device
- **VIDEO_CODED** — coded from video
- **ADMINISTRATIVE** — obtained from an event, club, league, or other record system
- **ALGORITHM_DERIVED** — inferred by software/model from underlying observations
- **ANALYTIC_DERIVED** — calculated during analysis

For derived variables, preserve the source variable(s), algorithm/formula, software/version where relevant, and derivation date or pipeline version.

## 9. Skill ratings

Never store a rating value without identifying the rating system. Ratings from different systems must not be treated as numerically interchangeable unless an explicit validated crosswalk is used.

Recommended representation:

```text
skill_rating_system = <system name>
skill_rating_value  = <value as reported>
skill_rating_date   = <date, if available>
```

Self-assessed skill should be identified as self-assessed rather than represented as an official rating.

## 10. Public-release guidance

PR-MDS defines interoperability, not permission to share data. Before public release:

- remove direct identifiers;
- assess re-identification risk from combinations of age, date, site, event, and rare characteristics;
- honor consent and ethics conditions;
- comply with applicable institutional policy, contracts, and law;
- document any generalization or suppression performed for disclosure control.

## 11. Compatibility statement

A study may describe a dataset as **“PR-MDS v0.1 mapped”** when:

1. applicable Core fields are mapped to the PR-MDS definitions;
2. deviations are documented;
3. missing values follow documented rules;
4. provenance is available for key variables;
5. the exact PR-MDS version is reported.

For v0.x releases, use “mapped” or “pilot-compatible” rather than implying certification.

## 12. Validation questions for v0.2

The pilot phase should answer:

1. Which Core variables are frequently unavailable or burdensome?
2. Which definitions produce inter-rater disagreement?
3. Which fields differ systematically across countries or settings?
4. Can the schema represent both recreational and competitive play without distortion?
5. What minimum social, health, and performance modules are scientifically useful?
6. What public-release transformations best balance reproducibility and privacy?

## 13. Change policy

No field becomes permanently mandatory because it appeared in v0.1. Promotion, removal, or definition changes should be justified by pilot evidence, external review, and backward-compatibility considerations.
