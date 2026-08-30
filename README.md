# Open Pickleball Research Commons (OPRC)

> **Open, cumulative, and reproducible infrastructure for the science of pickleball.**

This repository is evolving from a practical pickleball score-sheet prototype into a research commons for building interoperable, reusable, and testable pickleball science.

## Current status

**Development branch:** `research-commons-v0.1`  
**Scientific status:** candidate / pilot infrastructure, not an established international standard.

The repository currently contains:

- **PR-MDS v0.1** — a candidate Pickleball Research Minimum Data Set;
- a machine-readable PR-MDS variable dictionary;
- a **28-record proof-of-concept Global Pickleball Research Evidence Map seed corpus**;
- an Evidence Map codebook and schema;
- a low-cost **Pickleball Field Measurement Protocol v0.1**;
- a **Pickleball as Social Technology Framework v0.1**;
- a full methods/infrastructure manuscript: **Toward Cumulative Pickleball Science: An Open Research Commons, Minimum Data Standard, and Living Evidence Map**;
- a BibTeX reference library and submission-readiness audit;
- the original browser-based pickleball score-sheet application.

## Why this project exists

Pickleball research is expanding across injury epidemiology, physical activity, aging, psychology, social connection, biomechanics, participation behavior, and technology. The challenge is not only producing more studies, but making independently conducted studies easier to compare, replicate, synthesize, and reuse.

OPRC therefore focuses on a **small shared research layer** rather than forcing every study to use one universal protocol.

## Core principle

> **Minimum common core, extensible modules.**

Studies should remain free to use their own theories, outcomes, instruments, and methods. Shared provenance, participant, and session/exposure fields can nevertheless reduce avoidable incompatibility.

## Repository map

- `standards/` — PR-MDS and machine-readable dictionaries
- `evidence/` — Living Evidence Map schema, codebook, seed corpus, and discovery notes
- `protocols/` — candidate field measurement protocols
- `social-technology/` — social-interaction and relationship-formation research framework
- `papers/` — manuscript, references, and submission-readiness materials
- root web files — existing score-sheet / GitHub Pages application

## Evidence Map status

The current 28-record map is a **discovery seed**, not an exhaustive systematic review. It is explicitly labeled as AI-assisted and single-coded. A stable evidence resource requires bibliographic verification, reproducible multi-database searching, independent coding, agreement assessment, and archived releases.

## PR-MDS status

PR-MDS v0.1 is a candidate specification. It should be evaluated prospectively for burden, ambiguity, missingness, reliability, and scientific utility before promotion to a stable release.

## Manuscript

The current full English manuscript is available at:

`papers/cumulative-pickleball-science-manuscript.md`

Its companion reference library is:

`papers/references.bib`

The current scientific/submission audit is:

`papers/SUBMISSION_READINESS.md`

## Long-term direction

The longer-term architecture includes:

1. a Living Evidence Map;
2. PR-MDS and optional domain modules;
3. validated low-cost court-based measurement protocols;
4. PB-Bench for comparable video/AI tasks;
5. a multi-site replication network;
6. a Pickleball Observatory;
7. an annual, data-backed State of Pickleball Science report.

## Governing rule

**Do not increase complexity unless an added variable, protocol, or module creates clear scientific value or interoperability.**
