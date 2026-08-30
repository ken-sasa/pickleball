# Global Pickleball Research Evidence Map — Seed Corpus Notes v0.1

**Snapshot date:** 2026-08-18  
**Status:** Discovery seed only — not a completed systematic review  
**Records:** 28 included scholarly records

## Purpose

This seed corpus initializes the Open Pickleball Research Commons Evidence Map with real scholarly records while preserving a strict distinction between **discovery** and **systematic completeness**.

The present file is suitable for schema testing, gap discovery, backwards/forward citation chasing, and planning a reproducible systematic search. It must not be described as an exhaustive census of pickleball research.

## Discovery procedure

Initial discovery used the Consensus scholarly index on 2026-08-18 with broad and domain-focused queries including:

- `pickleball year:2018-2026 human:true`
- `pickleball physiology exercise cardiovascular fitness year:2018-2026 human:true`
- `pickleball biomechanics performance movement skill year:2018-2026 human:true`

Records were selected only when pickleball was a substantive exposure, intervention, setting, performance task, or review topic. Generic racket-sport or exercise papers returned by semantic search were not entered.

## Coding procedure

The 28 records were machine-assisted, abstract-level coded against `CODEBOOK.md` and `evidence-map-schema-v0.1.csv`.

Rules used in this seed pass:

1. Do not infer data-collection country from author affiliation.
2. Use `NR` when the indexed abstract does not report a field.
3. Preserve unweighted case counts separately from weighted national estimates in notes.
4. Code design from the reported methods rather than blindly copying an index label.
5. Mark every record `single_coded`.
6. Mark open-science, funding, and conflict fields `unknown` unless directly verified.
7. Do not claim causality from cross-sectional associations.

`coder_id = AI_ASSISTED_SEED` explicitly indicates that this is not an independently human-verified extraction.

## Snapshot composition

### By publication year

| Year | Records |
|---:|---:|
| 2019 | 1 |
| 2020 | 3 |
| 2021 | 3 |
| 2022 | 1 |
| 2023 | 2 |
| 2024 | 4 |
| 2025 | 13 |
| 2026 | 1 |

### By primary domain

| Domain | Records |
|---|---:|
| injury_safety | 14 |
| physical_health_fitness | 5 |
| social_connection | 4 |
| psychology_wellbeing | 2 |
| participation_behavior | 1 |
| technology_ai | 1 |
| aging_physical_function | 1 |

### By primary design

| Design | Records |
|---|---:|
| cross_sectional | 9 |
| surveillance | 6 |
| quasi_experimental | 4 |
| narrative_review | 1 |
| prospective_cohort | 1 |
| systematic_review | 1 |
| qualitative | 1 |
| scoping_review | 1 |
| retrospective_cohort | 1 |
| case_series | 1 |
| biomechanical_lab | 1 |
| randomized_trial | 1 |

## Immediate signal from the seed map

The first-pass literature is strongly concentrated in **injury/safety**, frequently using emergency-department surveillance or retrospective clinical data. There is a smaller but growing literature on physical activity and fitness, psychosocial outcomes, social connection, and targeted interventions.

In contrast, the seed search found relatively little directly pickleball-specific work on:

- validated sport-specific performance testing;
- longitudinal player development;
- coaching and pedagogy;
- match analytics and tactical structure;
- standardized computer-vision benchmarks;
- youth development outside injury surveillance;
- facilities and environmental effects;
- management/economics;
- policy/governance;
- experimentally manipulated social design features such as partner-rotation rules.

These are **provisional research gaps**, not claims of absence. They must be checked in the systematic search.

## Verification gates before v1.0

The seed corpus should advance through the following gates:

### Gate A — Bibliographic verification

- resolve every DOI;
- verify authors, journal, year, and publication type;
- verify data-collection country from full text where possible;
- identify duplicate reports from shared samples.

### Gate B — Systematic search

Run a reproducible search across at minimum:

- PubMed/MEDLINE;
- SPORTDiscus;
- Scopus or Web of Science where institutional access permits;
- PsycINFO for psychosocial work;
- Google Scholar only as a supplementary discovery source;
- dissertation/thesis indexes if grey literature is in scope.

Freeze database, date, query string, result count, deduplication rule, and screening decisions.

### Gate C — Double coding

Independently double-code a non-trivial subset, quantify categorical agreement, adjudicate disagreements, and revise ambiguous definitions before stable release.

### Gate D — Open-science audit

Verify preregistration, open data, open code, funding statements, and conflict-of-interest statements from the publications or linked repositories rather than abstracts alone.

## Recommended first publishable product

After Gates A-C, the corpus can support a methods/evidence paper provisionally framed as:

**Mapping the Emerging Science of Pickleball: A Living Evidence Map and Open Research Infrastructure**

The paper should emphasize the infrastructure, reproducible taxonomy, growth and composition of the field, and empirically demonstrated gaps rather than simply counting publications.
