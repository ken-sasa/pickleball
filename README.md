# Open Pickleball Research Commons

**An open, cumulative, and reproducible infrastructure for the science of pickleball.**

This repository develops shared research infrastructure for pickleball science: evidence mapping, minimum data standards, field measurement protocols, open datasets, analytics benchmarks, replication resources, and the study of **Pickleball as Social Technology**.

The goal is not to claim a standard before one exists. Materials under `v0.x` are candidate specifications intended for pilot use, criticism, validation, and revision.

## What is here

- `evidence/` — living evidence map, coding manual, and seed scholarly corpus
- `standards/` — PR-MDS candidate minimum data specification
- `protocols/` — low-cost field measurement protocols
- `social-technology/` — theory and study designs for pickleball as a social technology
- existing root web-app files — the original static pickleball score-sheet prototype, retained for continuity

## Current research assets

### Global Pickleball Research Evidence Map v0.1

The repository now includes a **28-record scholarly seed corpus** coded at study level. It spans injury/safety, physical health and fitness, social connection, psychology/well-being, participation behavior, aging/physical function, and technology/AI.

This is explicitly a discovery seed, **not an exhaustive systematic review**. Records are marked `AI_ASSISTED_SEED` and `single_coded` until human/full-text verification and double coding are completed.

See:

- `evidence/evidence-map-v0.1.csv`
- `evidence/SEED_CORPUS_NOTES.md`
- `evidence/CODEBOOK.md`

### PR-MDS v0.1

The **Pickleball Research Minimum Data Set (PR-MDS)** is a candidate core specification for making datasets easier to compare and combine across studies.

The design principle is a small reusable core with extensible modules rather than a compulsory giant questionnaire.

See:

- `standards/PR-MDS-v0.1.md`
- `standards/pr-mds-v0.1.csv`

### Pickleball Field Measurement Protocol v0.1

A candidate 15–20 minute field battery prioritizing equipment that ordinary courts, gyms, clubs, universities, and community events can realistically use.

The v0.1 protocol deliberately preserves attempt-level raw observations and treats reliability and validity as empirical questions rather than assumptions.

See `protocols/field-measurement-v0.1.md`.

### Pickleball as Social Technology

This program asks a broader question:

> **How can sport be designed as a social technology?**

Pickleball is treated as a testbed for studying how rules, partner rotation, court structure, skill matching, repeated encounters, and participation design may influence the formation and persistence of social ties.

See `social-technology/framework-v0.1.md`.

## Research architecture

```text
open-pickleball-research/
├── evidence/
│   ├── CODEBOOK.md
│   ├── evidence-map-schema-v0.1.csv
│   ├── evidence-map-v0.1.csv
│   └── SEED_CORPUS_NOTES.md
├── standards/
│   ├── PR-MDS-v0.1.md
│   └── pr-mds-v0.1.csv
├── protocols/
│   └── field-measurement-v0.1.md
├── social-technology/
│   └── framework-v0.1.md
├── ROADMAP.md
├── CONTRIBUTING.md
└── [original score-sheet web app files]
```

## Scientific posture

The repository follows five principles:

1. **Open before ornate** — publish inspectable definitions, schemas, and protocols early.
2. **Candidate before standard** — a document does not become a standard because its authors call it one.
3. **Raw before composite** — retain attempt-level observations when feasible and derive scores transparently.
4. **Field-deployable when possible** — prioritize methods that can be replicated outside elite laboratories while documenting optional high-resolution layers.
5. **Validation before authority** — reliability, validity, inter-rater agreement, cross-site robustness, and external review are required before stable claims.

## Near-term roadmap

The next validation sequence is:

1. bibliographically verify the 28-record seed corpus and resolve every DOI;
2. run a reproducible multi-database systematic search;
3. double-code a non-trivial Evidence Map subset and quantify agreement;
4. pilot PR-MDS on a real field dataset;
5. test the field battery for feasibility and reliability;
6. pilot a Social Technology study, ideally manipulating a simple feature such as partner-rotation structure;
7. obtain external methodological review before any `v1.0` stable release.

See `ROADMAP.md` for release gates.

## Citation and contribution

Until the first archived release is created, cite the repository and the exact commit or version used. Contributions that improve definitions, identify missing studies, reproduce measurements, add validated translations, or contribute replication data are especially welcome.

See `CONTRIBUTING.md` for integrity and contribution rules.

## Existing score-sheet application

This repository originally hosted a static score-sheet web application. Those files are intentionally retained at the repository root during the founding transition. A later compatibility-preserving change can move the application under `tools/` and align its export schema with PR-MDS.

---

**Open Pickleball Research Commons** aims to make pickleball research cumulative: shared evidence, shared definitions, shared measurements, and studies that can be reproduced rather than rediscovered from scratch.
