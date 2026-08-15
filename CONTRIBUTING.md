# Contributing to Open Pickleball Research Commons

Thank you for helping improve open and reproducible pickleball research.

## What kinds of contributions are useful?

Contributions may include:

- corrections to variable definitions;
- proposals for new optional variables or modules;
- evidence-map additions and screening corrections;
- translations;
- validation results;
- replication reports;
- field-protocol improvements;
- benchmark datasets or evaluation code;
- documentation improvements.

## Before proposing a new core variable

The PR-MDS core is intentionally small. A variable should enter the core only if it is plausibly useful across multiple research domains and the cost or burden of collecting it is low.

A proposal should explain:

1. construct and operational definition;
2. why it belongs in the minimum core rather than an optional module;
3. measurement burden;
4. expected missingness or sensitivity;
5. internationalization concerns;
6. evidence or use cases supporting inclusion;
7. backward-compatibility implications.

## Evidence Map contributions

Please follow `evidence/CODEBOOK.md` and preserve provenance. Do not infer missing study characteristics when the source does not report them. Use `NR` (not reported) where specified rather than guessing.

## Versioning and change control

Materials under `v0.x` are candidate specifications. Proposed changes should be reviewable and documented. Changes to required fields, construct definitions, or coding categories should not be silently overwritten.

## Research integrity

Contributors should distinguish:

- directly observed values;
- participant-reported values;
- assessor-coded values;
- algorithmically derived values;
- analytically transformed values.

Do not upload personally identifiable information, sensitive participant-level data, or data whose sharing is inconsistent with consent, ethics approval, institutional policy, contractual terms, or applicable law.

## Accessibility and simplicity

Prefer concise definitions, plain data structures, and field-deployable procedures. Complexity should be justified by scientific value.

## Attribution

Substantive contributions should be documented through Git history, releases, and—where appropriate—paper-specific contribution statements. Repository contribution alone does not automatically determine scholarly authorship.
