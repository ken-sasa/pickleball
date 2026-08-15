# Open Pickleball Research Commons

**An open, cumulative, and reproducible infrastructure for the science of pickleball.**

Open Pickleball Research Commons (OPRC) is a research infrastructure project for building shared definitions, measurement protocols, evidence maps, datasets, benchmarks, and replication resources for pickleball research.

The project is intentionally broader than a single laboratory, discipline, or paper. Its goal is to make pickleball research easier to compare, reproduce, extend, and reuse across countries and research domains.

> **Status:** Founding draft, v0.1 (August 2026). Materials labeled `v0.x` are proposals for testing and community review, not established international standards.

## Why this repository exists

Pickleball research is expanding across sports science, public health, injury epidemiology, aging, psychology, social connection, biomechanics, computer vision, education, management, and community studies. These studies often use different variables, definitions, protocols, and data structures.

OPRC addresses that fragmentation by developing a lightweight shared research layer:

1. **Evidence** — What has already been studied?
2. **Standards** — What minimum variables should be reported?
3. **Protocols** — How can common constructs be measured reproducibly in ordinary courts and gyms?
4. **Data** — How can results be represented in reusable formats?
5. **Benchmarks** — How can analytic methods be compared on common tasks?
6. **Replication** — How can studies be repeated across institutions and countries?
7. **Observatory** — How is pickleball science itself changing over time?

## Founding workstreams

### 1. Pickleball Research Minimum Data Set (PR-MDS)

`standards/PR-MDS-v0.1.md`

A proposed minimum reporting and data schema for pickleball studies. The first version covers participant characteristics, playing exposure, match/session context, performance, health/safety, social outcomes, and provenance.

The design principle is **minimum common core, extensible modules**. Researchers should not have to collect everything in the repository; they should be able to collect a small compatible core and add domain-specific modules.

### 2. Pickleball Evidence Map

`evidence/`

A living, structured map of the peer-reviewed and scholarly pickleball literature. The map is designed around reusable coding fields rather than a static narrative review.

### 3. Field Measurement Protocol

`protocols/field-measurement-v0.1.md`

A low-cost measurement framework intended for ordinary courts, gyms, universities, clubs, and community events. The emphasis is reproducibility and deployment, not dependence on laboratory-only equipment.

### 4. Pickleball as Social Technology

`social-technology/framework-v0.1.md`

A research program asking:

> **How can sport be designed as a social technology?**

Pickleball is treated not only as physical activity or competition, but as a potentially measurable system for generating interaction, repeated contact, new ties, belonging, and intergenerational connection.

### 5. Future workstreams

Planned components include:

- `benchmarks/` — common computer-vision and match-analysis tasks
- `datasets/` — de-identified and openly reusable research data where ethically and legally possible
- `observatory/` — longitudinal monitoring of pickleball science
- `replications/` — multi-site and international replication packages
- `papers/` — analysis plans, preprints, and reproducibility supplements

## Repository structure

```text
.
├── README.md
├── ROADMAP.md
├── CONTRIBUTING.md
├── evidence/
│   ├── CODEBOOK.md
│   └── evidence-map-schema-v0.1.csv
├── standards/
│   ├── PR-MDS-v0.1.md
│   └── pr-mds-v0.1.csv
├── protocols/
│   └── field-measurement-v0.1.md
├── social-technology/
│   └── framework-v0.1.md
└── [existing score-sheet web app files]
```

## Existing score-sheet prototype

This repository already contains a browser-based pickleball score sheet and offline-capable GitHub Pages prototype. It is being retained as an early field-tool component. In a future release it can be reorganized under a dedicated `tools/` area and aligned with PR-MDS-compatible exports.

## Design principles

OPRC follows six working principles:

- **Open where possible** — methods, schemas, codebooks, and non-sensitive materials should be inspectable and reusable.
- **Minimum before maximum** — prefer a small interoperable core to an exhaustive but unusable standard.
- **Field deployable** — prioritize methods that can work outside elite laboratories.
- **Versioned** — definitions and protocols change only through explicit versions.
- **Reproducible** — distinguish raw observations, derived variables, and analytic decisions.
- **Internationalizable** — avoid Japan- or US-specific assumptions in core schemas when possible.

## Versioning

- `v0.x` — experimental / candidate specification
- `v1.x` — stable specification after validation and external review
- major version changes — incompatible changes to required fields or construct definitions

Archived versions should remain available for reproducibility.

## How to contribute

See `CONTRIBUTING.md`. Contributions are welcome from sports scientists, clinicians, epidemiologists, social scientists, computer-vision researchers, coaches, analysts, clubs, and community organizations.

## Citation

Until a versioned release and archival DOI are issued, cite the repository URL together with the exact version or commit used. A formal `CITATION.cff` and DOI-backed release are planned before v1.0.

## Founding objective

The near-term objective is not to declare a universal standard. It is to release a sufficiently clear and useful **candidate research infrastructure** that other investigators can test, criticize, replicate, and improve.
