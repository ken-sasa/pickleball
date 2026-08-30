# Pickleball Field Measurement Protocol v0.1

**Status:** Pilot protocol — not yet validated  
**Purpose:** A low-cost, repeatable measurement battery for ordinary courts, gyms, clubs, universities, and community events.

## 1. Design objective

The protocol is designed around one constraint:

> **A useful pickleball measurement system should be deployable in the places where pickleball is actually played.**

The v0.1 battery therefore prioritizes court markings, a paddle, balls, cones/tape, a stopwatch, and an optional smartphone/tablet over laboratory-only equipment.

The protocol is a candidate research instrument. Reliability, validity, learning effects, assessor effects, and sensitivity to skill level must be tested before scores are treated as established normative measures.

## 2. Recommended session length

Target: **15–20 minutes per participant** for the core battery, excluding consent and research questionnaires.

Suggested order:

1. metadata and readiness check;
2. movement task;
3. serve-control task;
4. soft-game control task;
5. rally-continuity task;
6. optional device/video measures;
7. post-session social measures when relevant.

Keep task order fixed within a study unless order is experimentally manipulated.

## 3. Minimum equipment

- regulation-marked pickleball court or a documented equivalent layout;
- participant's usual paddle or study-standard paddle, recorded explicitly;
- study-standard ball type when feasible;
- stopwatch or timing application;
- cones or removable floor markers;
- clipboard/tablet for scoring;
- optional smartphone/tablet tripod for video.

Record equipment and environmental deviations rather than silently treating them as equivalent.

## 4. Pre-measurement metadata

Map the session to PR-MDS v0.1 and record at minimum:

- `study_id`
- `protocol_version`
- `site_id`
- `collection_date`
- `country_iso3`
- `participant_id`
- `session_id`
- `session_type = measurement`
- `indoor_outdoor`
- `pickleball_experience_months` when available
- `skill_rating_system` and `skill_rating_value` when available

Also record paddle/ball standardization if those factors may affect the outcome.

## 5. Core Task A — Court-line change-of-direction

### Construct

Pickleball-specific short-distance acceleration, braking, and direction change using existing court landmarks.

### Procedure

1. Define the two court lines used as endpoints before data collection.
2. Participant begins from a standardized ready position.
3. On the start cue, participant moves to the designated line, makes the required line contact/criterion, returns, and completes the predefined shuttle sequence.
4. Conduct one familiarization trial.
5. Conduct two recorded trials with a standardized rest interval.
6. Store both trials; do not retain only the better score in raw data.

### Required reporting

- exact route and line-contact rule;
- footwear and surface if relevant;
- timing method;
- trial times;
- whether timing was manual or device-derived;
- adverse event or incomplete trial.

### Candidate derived variables

- best time;
- mean time;
- trial-to-trial absolute difference.

The derivation rule must be declared before analysis.

## 6. Core Task B — Serve placement control

### Construct

Ability to execute legal study-defined serves into predefined target regions with repeatable placement.

### Procedure

1. Define target zones on the legal receiving court using removable markers or a documented coordinate grid.
2. Use a fixed number of attempts from each serving side; v0.1 recommends **6 per side (12 total)** as a practical pilot dose.
3. Use the same scoring system for every participant in the study.
4. Record each attempt individually before calculating totals.

### Minimum attempt-level fields

- attempt number;
- serving side;
- in/out under the study rule definition;
- target-zone hit;
- optional landing coordinate;
- optional ball speed;
- video availability.

### Candidate summary metrics

- legal/in rate;
- target-hit rate;
- mean radial error when coordinates are available;
- left/right-side asymmetry.

Do not collapse accuracy into a single score until the scoring rule has been tested for reliability and discrimination.

## 7. Core Task C — Soft-game control

### Construct

Ability to sustain controlled low-velocity exchanges in the non-volley-zone context.

### Candidate procedure

1. Use a standardized cooperative partner, feeder, or validated feeding method.
2. Define a target region and exchange pattern.
3. Run a fixed-duration or fixed-attempt block.
4. Record successful controlled returns and failure type.

Because partner behavior can materially affect the score, v0.1 treats this task as **pilot-only** until partner/feeder reliability is quantified.

### Candidate fields

- attempt number;
- feed valid/invalid;
- return in target/not in target;
- net error;
- long/wide error;
- exchange length;
- partner/feeder identifier.

## 8. Core Task D — Rally continuity

### Construct

Ability to sustain a standardized cooperative exchange.

### Candidate procedure

- Use a predefined exchange type (for example, cooperative dink or groundstroke rally).
- Use a fixed time window or fixed maximum number of shots.
- Count successful consecutive contacts and interruptions.
- Record partner identity or feeding system.

### Candidate metrics

- longest successful sequence;
- successful contacts per minute;
- interruption rate.

This is distinct from competitive rally performance and should not be interpreted as match quality without validation.

## 9. Optional video layer

When consent, ethics, and local policy permit, mount a smartphone/tablet in a standardized position.

Record:

- device model;
- frame rate and resolution;
- camera location/orientation;
- zoom setting if relevant;
- whether video is raw, stabilized, or transformed;
- file-to-session linkage using pseudonymous IDs.

Video may support later validation of manual timing, court position, shot classification, and computer-vision benchmarks.

Do not upload identifiable participant video to an open repository merely because the tabular dataset is shareable.

## 10. Optional social layer

For studies of Pickleball as Social Technology, append a brief session-level social record rather than embedding a long psychosocial battery into every performance test.

Candidate fields:

- number of distinct people played with;
- number not known before the session;
- partner rotation count;
- new conversations beyond necessary game coordination;
- contact exchange;
- intention to play together again;
- subsequent joint play at follow-up.

Validated scales should be stored with instrument name, version, language, scoring rule, and licensing constraints.

## 11. Assessor protocol

Before formal data collection:

- use a written task script;
- train assessors on start/stop criteria;
- test at least a subset with two independent assessors;
- record assessor ID;
- document deviations immediately.

The assessor should not silently repeat a trial because a result “looks wrong.” Repeat criteria must be defined in advance.

## 12. Reliability study for v0.2

The first validation study should estimate, where appropriate:

- test-retest reliability;
- inter-rater reliability;
- within-session trial variability;
- learning/familiarization effects;
- association with external skill indicators;
- floor/ceiling effects by skill level;
- feasibility and completion time.

Report raw trial distributions, not only reliability coefficients.

## 13. Data architecture

Recommended tables:

```text
participants.csv
sessions.csv
movement_trials.csv
serve_attempts.csv
soft_game_attempts.csv
rally_trials.csv
social_session.csv        # optional
video_manifest.csv        # optional
```

Use IDs to link tables. Preserve attempt-level data and derive summary scores downstream.

## 14. v0.1 principle

**Measure simply, preserve raw observations, and validate before declaring a score meaningful.**
