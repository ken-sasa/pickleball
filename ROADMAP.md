# Open Pickleball Research Commons — Roadmap

## Founding phase: v0.1

Goal: establish a small, inspectable research core that can be reviewed before any claim of standardization.

- [x] Define project scope and principles
- [x] Draft PR-MDS v0.1
- [x] Define PR-MDS machine-readable variable dictionary
- [x] Define Evidence Map schema and coding rules
- [x] Draft low-cost field measurement protocol
- [x] Draft Pickleball as Social Technology framework
- [x] Populate the first 28-record evidence-map seed corpus
- [x] Document discovery queries and seed-corpus limitations
- [ ] Bibliographically verify all seed records and resolve every DOI
- [ ] Expand the Evidence Map through a reproducible multi-database search
- [ ] Conduct external methodological review
- [ ] Test PR-MDS on at least one real field dataset
- [ ] Test inter-rater reliability of Evidence Map coding

## Validation phase: v0.2

Goal: replace plausible definitions with tested definitions.

### PR-MDS
- Pilot the core variables in university, club, and community settings.
- Record missingness, burden, ambiguity, and ceiling/floor effects.
- Separate truly universal core fields from optional modules.
- Add explicit derivation rules and validation checks.

### Evidence Map
- Verify bibliographic metadata against DOI/publisher/database records.
- Verify data-collection country and principal sample size from full text where possible.
- Identify duplicate reports and shared underlying samples.
- Develop and freeze a reproducible search strategy.
- Record database, query, date, screening decision, and exclusion reason.
- Double-code a non-trivial validation subset.
- Quantify agreement for inclusion, study-design, and domain coding.
- Publish study-level extraction data where licensing permits.
- Audit preregistration, open data, open code, funding, and conflict-of-interest fields from the underlying publications.

### Field protocol
- Estimate test-retest reliability where appropriate.
- Report equipment, court conditions, assessor training, and timing.
- Compare smartphone/tablet-assisted and manual scoring where feasible.

### Social Technology program
- Validate operational definitions for interaction opportunity, tie formation, repeated contact, belonging, and cross-group contact.
- Distinguish association from causal effects.
- Pre-register at least one prospective study.
- Prefer a simple first manipulation such as fixed versus structured rotating partners while holding total play time broadly constant.

## Network phase: v0.3

Goal: make the infrastructure usable beyond a single research group.

- Recruit at least three independent pilot sites.
- Add replication-package templates.
- Create translation guidance without changing construct identity.
- Establish contributor and change-control governance.
- Publish a public issue template for proposed variable changes.

## Stable release target: v1.0

A v1.0 release should require, at minimum:

1. documented use in real studies;
2. external review by multiple domain experts;
3. versioned change history;
4. a stable minimum core;
5. clear licensing and citation rules;
6. archival release with DOI;
7. machine-readable schemas plus human-readable definitions;
8. reproducible and independently checked evidence-map procedures.

## Longer-term research infrastructure

### PB-Bench
A benchmark suite for court detection, player detection, ball tracking, rally segmentation, shot classification, position estimation, and point-outcome inference.

### Pickleball Observatory
A longitudinal dataset tracking publications, disciplines, countries, methods, datasets, trials, technologies, and research gaps.

### Multi-site replication network
A lightweight protocol for institutions to reproduce selected studies using the same core variables and provenance rules.

### Annual State of Pickleball Science
A versioned, data-backed annual synthesis generated from the Evidence Map and Observatory rather than a narrative-only report.

## Candidate publication sequence

1. **Mapping the Emerging Science of Pickleball: A Living Evidence Map and Open Research Infrastructure**
2. **A Minimum Data Specification for Reproducible Pickleball Research**
3. **A Low-Cost Field Measurement Battery for Pickleball: Feasibility and Reliability**
4. **Pickleball as Social Technology: Experimental Evidence from Partner-Rotation Design**
5. **An Open Benchmark for Pickleball Match and Video Analytics**

The first paper should not move from concept to submission until the Evidence Map has passed systematic-search and double-coding gates.

## Governing rule

**Do not increase complexity unless the additional field, protocol, or module creates clear scientific value or interoperability.**
