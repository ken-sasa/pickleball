# Pickleball Research Minimum Data Set (PR-MDS) v0.3

**Status:** Pre-consensus candidate for external review and pilot testing  
**Version:** 0.3  
**Project:** Open Pickleball Research Commons

## 1. Purpose

PR-MDS v0.3 proposes a small **context-and-provenance layer** that can be mapped across heterogeneous pickleball studies. It is not a core outcome set, reporting guideline, accreditation or certification scheme, universal protocol, or claim of international consensus.

The design target is **minimum sufficient interoperability**: preserve enough shared context to interpret independently designed studies together while leaving theories, outcomes, instruments, and analyses study-specific.

## 2. Provisional core-selection rule

A field belongs in the candidate universal core only when all of the following are provisionally true:

1. it is useful across multiple study designs or domains;
2. it materially improves interpretation, linkage, exposure description, or derivation transparency;
3. it can be collected or mapped with low burden in ordinary sport-research settings;
4. it can be defined with acceptable privacy and international portability.

These judgments must be tested. Inclusion in v0.3 creates no presumption of permanent core status.

## 3. Levels

PR-MDS allows linked records at several levels:

- **Study** — research project or protocol
- **Site** — data-collection location or organizational unit
- **Participant** — pseudonymized participant
- **Session** — bounded participation or measurement episode
- **Match/Game** — optional sport-specific unit
- **Rally/Event** — optional fine-grained unit
- **Derived record** — value produced from one or more source observations

## 4. Candidate universal core

### 4.1 Identity and study context

| Variable | Requirement | Definition |
|---|---|---|
| `record_id` | REQUIRED | Unique record identifier within a release |
| `study_id` | REQUIRED | Stable study/protocol identifier |
| `protocol_version` | REQUIRED | Version of protocol governing the record |
| `site_id` | RECOMMENDED | Pseudonymous or public data-collection site identifier |
| `collection_date` | RECOMMENDED | ISO 8601 date or documented generalized date |
| `country_iso3` | RECOMMENDED | ISO 3166-1 alpha-3 location of data collection |

### 4.2 Participant context

| Variable | Requirement | Definition |
|---|---|---|
| `participant_id` | CONDITIONAL | Stable pseudonymous identifier for linked participant-level data |
| `age_value` | OPTIONAL-CONTROLLED | Exact age where scientifically justified and appropriately governed |
| `age_band` | RECOMMENDED | Public-release or low-resolution age representation |
| `pickleball_experience_months` | RECOMMENDED | Months since regular pickleball participation began |
| `skill_rating_system` | CONDITIONAL | Named structured rating system when a rating value is present |
| `skill_rating_value` | CONDITIONAL | Value paired with `skill_rating_system` |

### 4.3 Session and exposure context

| Variable | Requirement | Definition |
|---|---|---|
| `session_id` | CONDITIONAL | Stable session identifier for session-linked data |
| `session_type` | RECOMMENDED | `practice`, `recreational_play`, `competition`, `measurement`, `lesson`, `other` |
| `play_format` | RECOMMENDED | `singles`, `doubles`, `mixed`, `not_applicable`, `unknown` |
| `indoor_outdoor` | RECOMMENDED | `indoor`, `outdoor`, `mixed`, `unknown` |
| `session_duration_min` | RECOMMENDED | Total session duration in minutes |
| `active_play_duration_min` | OPTIONAL | Active participation time in minutes |
| `games_played` | OPTIONAL | Completed games within the session |
| `exposure_measurement_method` | RECOMMENDED | `direct_timing`, `device_derived`, `administrative_record`, `self_report`, `scheduled_duration`, `estimated`, `mixed`, `unknown` |

## 5. Unified provenance classification

All PR-MDS v0.3 artifacts use the same controlled provenance classes:

- `DIRECT_OBSERVATION`
- `SELF_REPORT`
- `DEVICE_MEASURED`
- `VIDEO_CODED`
- `ADMINISTRATIVE_RECORD`
- `ALGORITHM_DERIVED`
- `ANALYTIC_DERIVED`
- `MIXED`

Each analytically important value SHOULD identify `provenance_class`.

For `ALGORITHM_DERIVED` and `ANALYTIC_DERIVED` records, the following SHOULD also be preserved when applicable:

- `source_record_ids`
- `derivation_method`
- `software_or_model`
- `software_or_model_version`
- `pipeline_version`
- `unit`

A full W3C PROV representation may be used when richer lineage is needed. PR-MDS is deliberately a lightweight domain layer rather than a competing provenance ontology.

## 6. Domain modules

The following are outside the universal v0.3 core and should be defined within relevant modules.

### 6.1 Injury and health module

Candidate fields include injury definition, onset, mechanism, body region, medical attention, time loss, pain, illness, and exposure denominators. Existing IOC/STROBE-SIIS definitions should be reused or explicitly cross-walked rather than silently replaced.

### 6.2 Participant and equity module

Candidate fields include sex-related variables, gender-related variables, disability, socioeconomic indicators, and other characteristics whose scientific relevance and governance vary across questions and jurisdictions.

### 6.3 Sport-specific participant module

Candidate fields include dominant hand, prior racket/paddle-sport experience, playing role, equipment, court surface, and competition characteristics.

### 6.4 Performance and analytics module

Candidate fields include `match_id`, `game_id`, `rally_id`, shot/event classes, outcome, player coordinates, device metadata, camera settings, label source, annotation uncertainty, and benchmark split.

### 6.5 Social connection module

Candidate fields include prior acquaintance, partner rotation, new interaction, repeat-play intention, contact exchange, subsequent joint play, network ties, belonging, and loneliness measures.

## 7. Missingness

Recommended machine-readable missingness is explicit rather than encoded as arbitrary numeric values.

- `NA` — not applicable
- `NR` — not reported / not collected
- `UNK` — unknown despite attempted ascertainment

Blank values may be used only when the dataset contract explicitly defines their meaning.

## 8. Compatibility statement

A dataset may be described as **PR-MDS v0.3 mapped** when:

1. applicable candidate core fields are mapped to their defined meanings;
2. the exact PR-MDS version is reported;
3. deviations and unmapped fields are documented;
4. units and missingness are explicit;
5. provenance is recorded for analytically important variables;
6. derived fields preserve sufficient derivation metadata to reproduce or audit the transformation when feasible.

Use `mapped` or `pilot-compatible`; do not use `certified`.

## 9. Validation state

As of v0.3:

- structured human external reviews completed: **0**
- independent prospective pilot sites completed: **0**
- formal consensus process completed: **0**
- JSON Schema available: **yes**
- four-publication schema stress test completed: **yes**

These values should change only when the corresponding work is actually completed.

## 10. Promotion and retirement policy

No field is permanent because it appeared early. External review and pilot use may:

- retain it in the core;
- simplify its definition;
- move it to a module;
- split one field into multiple fields;
- replace it with an existing external standard;
- deprecate or remove it.

Stable releases must preserve a public audit trail of these decisions.
