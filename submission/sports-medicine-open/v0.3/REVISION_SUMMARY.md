# Revision Summary v0.3

## Trigger

v0.3 responds to a simulated editor plus three-reviewer stress test of v0.2. The main concern was legitimacy: a founder-designed research layer was being proposed before external consensus, pilot use, and explicit comparison with mature standards.

## Major conceptual changes

1. **Title and thesis changed.**  
   From: `Standardize Provenance Before Outcomes`  
   To: `Outcome Harmonization Needs Context and Provenance`  
   The claim is now structural rather than chronological.

2. **Context separated from provenance.**  
   Participant, site, protocol, and exposure metadata are treated as context; lineage and derivation are treated as provenance.

3. **OPRC positioned alongside existing standards.**  
   The manuscript now explicitly compares W3C PROV, FAIR, Common Data Elements, IOC/STROBE-SIIS, COMET/core outcome sets, and OPRC.

4. **PR-MDS status lowered and clarified.**  
   v0.3 is a `pre-consensus candidate`, not a standard, reporting guideline, certification scheme, or outcome set.

## PR-MDS changes

- unified provenance classification across human-readable specification, CSV dictionary, and JSON Schema;
- added explicit derivation metadata: source records, method, software/model, version, pipeline version, and unit;
- added `exposure_measurement_method`;
- moved `dominant_hand` and prior racket/paddle-sport history from universal core to a sport-specific module;
- moved sex/gender and related sensitive characteristics to a participant/equity module rather than implying irrelevance;
- added a four-criterion provisional core-selection rule;
- added JSON Schema validation;
- retained only `mapped` / `pilot-compatible` compatibility language.

## Evidence Map changes

- renamed the 28-record resource a **demonstration corpus**;
- added `sample_size_unit` to prevent participants, cases, injuries, and publications from being conflated;
- standardized bibliographic publication-year handling where identified;
- retained `AI_ASSISTED_SEED` and `single_coded` status;
- added a four-publication engineering stress test spanning injury survey, activity measurement, randomized intervention, and computer-vision biomechanics.

## Governance and transparency

- competing-interest wording now discloses that Kento Sasano is founder/current maintainer of OPRC while declaring no financial competing interests related to the work;
- added a governance draft designed to reduce founder dependence;
- added a structured external review protocol;
- opened GitHub Issue #3 for external review;
- current completed external review count remains **0** and pilot-site count remains **0**.

## Submission boundary

Journal submission should not state that v0.3 has external validation until completed reviews and their response matrix are archived. Zenodo DOI remains pending authenticated deposit.
