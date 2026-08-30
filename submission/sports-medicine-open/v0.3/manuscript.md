# Outcome Harmonization Needs Context and Provenance: A Research Commons for Cumulative Pickleball Science

**Article type:** Current Opinion  
**Author:** Kento Sasano  
**Affiliation:** Faculty of Environmental, Life, Natural Science and Technology, Okayama University, 3-1-1 Tsushima-naka, Kita-ku, Okayama 700-8530, Japan  
**Corresponding author:** Kento Sasano; office@sasano.org

## Abstract

Pickleball research now spans injury epidemiology, exercise and health, aging, psychosocial outcomes, biomechanics, and technology. This breadth creates a coordination problem before the field has accumulated decades of entrenched conventions. This Current Opinion argues that outcome harmonization is difficult to interpret without a shared **context-and-provenance layer**: common identifiers, exposure descriptors, data-source provenance, units, derivation rules, and version history. It proposes the Open Pickleball Research Commons (OPRC), an open and versioned scaffold that connects a Living Evidence Map with the Pickleball Research Minimum Data Set (PR-MDS) and domain-specific modules. OPRC is positioned explicitly alongside, not instead of, established frameworks such as FAIR, W3C PROV, common data elements, IOC/STROBE-SIIS injury-reporting guidance, and core outcome sets. PR-MDS v0.3 is a pre-consensus candidate layer rather than a reporting guideline, outcome set, certification scheme, or universal protocol. A 28-record demonstration corpus and four-paper stress test are used only to test whether the schema can represent heterogeneous research and expose metadata ambiguities; they are not presented as a systematic review. The proposal is deliberately falsifiable. Candidate elements should advance only if independent reviewers and multi-site users find them low burden, interpretable, useful, and transportable; weak elements should be revised, split, or retired. The target is **minimum sufficient interoperability**, not maximum standardization.

## Key Points

- Outcome harmonization is more interpretable when studies also share a lightweight context-and-provenance layer: identifiers, exposure, data-source lineage, units, derivation rules, and version history.
- OPRC complements rather than replaces FAIR, W3C PROV, common data elements, IOC/STROBE-SIIS, and core outcome-set processes.
- PR-MDS v0.3 is a pre-consensus candidate whose value must be demonstrated through external review, retrospective mapping, independent reuse, and multi-site validation before any stable-standard claim.

## 1. A Young Field Can Still Design Its Connective Tissue

Pickleball has rapidly become a multidisciplinary research object. Reviews synthesize health and well-being [1] and mental health [2]. Injury research includes emergency-department surveillance [3,4], a large nationwide player survey [5], and studies outside the United States [6]. Other work has quantified physical-activity intensity [7], tested pickleball interventions [8,9], examined social capital and loneliness [10,11], explored older players' experiences [12], and applied computer vision to sport-specific movement [13]. Court-based movement testing has also been used in research on falls [14].

This diversity is scientifically valuable, but it creates a coordination problem. Studies can use the same label for different constructs or different labels for similar constructs. "Experience" may mean years since first play, months of regular participation, weekly hours, or an informal skill category. Injury studies may report emergency-department presentations, all complaints, time-loss injuries, or overuse conditions without a common exposure denominator. A device-generated event label may look equivalent to a human-coded event while being produced through a completely different pipeline. Each study can be internally valid while still being difficult to combine with the next one.

The problem is not that pickleball lacks a universal outcome set. It is that later outcome harmonization, replication, and secondary reuse become harder when the surrounding context of each observation is not consistently preserved.

The proposal in this article is therefore narrower than "standardize pickleball research." It is to make a small amount of **connective context** interoperable while preserving diversity in theories, outcomes, instruments, designs, and analyses.

## 2. Context and Provenance Are Different but Complementary

The term **provenance** should not be used as a catch-all for all study metadata. In data systems, provenance describes how an entity was generated, transformed, attributed, or derived. W3C PROV formalizes provenance through relations among entities, activities, and agents [15]. A value such as a shot classification is therefore not fully interpretable without knowing whether it was directly observed, self-reported, device measured, video coded, algorithm derived, or analytically calculated, and—when derived—which source variables, software, versions, and transformations produced it.

**Context** answers different questions: who or what was studied, under which protocol, at which site, during what type and amount of participation, under which units and environmental conditions. Context and provenance overlap, but they are not interchangeable.

OPRC therefore defines a **context-and-provenance layer** rather than claiming that participant descriptors or exposure variables are provenance themselves. The structural claim is:

> **Outcome harmonization is difficult to interpret without a shared context-and-provenance layer.**

This claim does not require outcome research to wait. Injury definitions, core outcomes, and intervention measures can be developed in parallel. The argument is simply that a common outcome is more reusable when its source, exposure, denominator, derivation, and version are also explicit.

## 3. OPRC Complements Existing Standards

The Open Pickleball Research Commons (OPRC) is not intended to replace mature standards. Its role is to connect them to a young, cross-domain sport-science field through a lightweight implementation layer.

**Table 1. Existing frameworks and the proposed OPRC role**

| Framework | Primary function | What it standardizes | Relationship to OPRC |
|---|---|---|---|
| W3C PROV [15] | General provenance representation | Relations among entities, activities, and agents | OPRC can map sport-research lineage fields to a lightweight subset; it does not replace PROV |
| FAIR principles [16] | Data stewardship principles | Findability, accessibility, interoperability, and reuse | OPRC supplies domain-level implementation artifacts that can support FAIR practice |
| Common Data Elements [17] | Consistent collection across studies | Precisely defined fields and allowable values | PR-MDS candidate fields can mature into CDE-like elements after consensus and validation |
| IOC/STROBE-SIIS [18] | Sports injury and illness surveillance/reporting | Definitions, exposure, burden, severity, reporting | OPRC should reuse these concepts for injury modules rather than invent competing definitions |
| Core outcome-set process / COMET [19] | Consensus on outcomes to measure and report | Required outcomes in a defined area | OPRC v0.3 does not define a pickleball core outcome set and should not pre-empt one |
| OPRC / PR-MDS | Cross-domain connective layer | Context, provenance, exposure, identifiers, derivation, versioning | Candidate implementation for pickleball; requires external testing before stable status |

This distinction matters. A reporting guideline tells authors what to report. A core outcome set identifies outcomes that should be measured. A common data element precisely defines a recurring field. A provenance model represents lineage. A minimum data set can provide a practical subset that makes independently designed datasets easier to interpret together. These tools solve overlapping but non-identical problems.

The design goal should therefore be **minimum sufficient interoperability**: enough shared structure to connect studies, but not so much that heterogeneous research is forced into a single paradigm.

## 4. PR-MDS v0.3: A Pre-Consensus Candidate Layer

PR-MDS v0.3 is a candidate minimum data layer, not an established international standard. Its first intended users are **prospective and retrospective court-based observational, surveillance, and intervention studies** that need a small amount of shared context across domains.

### 4.1 Core-selection rule

A variable belongs in the candidate core only when it meets all four provisional criteria: (1) it is useful across multiple study designs or domains; (2) it materially improves interpretation, linkage, or exposure description; (3) it can be collected with low burden in ordinary sport settings; and (4) it can be defined with acceptable privacy and international portability. Candidate status means that these judgments remain hypotheses until external reviewers and pilot users test them.

### 4.2 Study and record context

The candidate study/record core includes a stable `record_id`, `study_id`, `protocol_version`, `site_id`, `collection_date`, and country code. These fields identify the observation and the protocol context under which it was created. Public releases may generalize dates or sites when disclosure risk requires it, provided that the transformation is documented.

### 4.3 Participant context

The universal participant core is intentionally small: a pseudonymous `participant_id`, age representation, pickleball-experience duration, and rating-system/value pairs when a structured rating is used. Exact age may be retained in controlled data while a derived age band is released publicly. A rating value without its rating system is not considered interpretable.

`dominant_hand`, prior racket-sport experience, sex-related variables, gender-related variables, disability, socioeconomic position, and other descriptors are **not universal v0.3 core fields**. They are placed in domain or jurisdiction-sensitive modules because their relevance and governance differ by research question. This is not a claim that they are unimportant. Injury, physiology, biomechanics, or equity studies may reasonably treat some of them as strongly recommended or required within the relevant module.

### 4.4 Session and exposure context

The candidate exposure layer includes `session_id`, session type, play format, indoor/outdoor setting, session duration, active-play duration when available, number of games, and an **exposure measurement method** indicating whether exposure was directly timed, device derived, retrospectively reported, scheduled, or otherwise estimated. Exposure matters because injury burden, physical-activity dose, learning, fatigue, and opportunity for social contact all depend on a denominator or dose. The IOC consensus similarly emphasizes exposure as fundamental to sports injury and illness interpretation [18].

### 4.5 Provenance and derivation

PR-MDS v0.3 uses one controlled provenance classification across the human-readable specification, dictionary, and validation schema:

- `DIRECT_OBSERVATION`
- `SELF_REPORT`
- `DEVICE_MEASURED`
- `VIDEO_CODED`
- `ADMINISTRATIVE_RECORD`
- `ALGORITHM_DERIVED`
- `ANALYTIC_DERIVED`
- `MIXED`

Derived variables should also preserve source field(s), algorithm or formula, software/model name and version where relevant, unit, and pipeline or derivation version. This is intentionally lighter than a full W3C PROV graph, but it can be mapped to richer provenance systems when needed.

### 4.6 Machine validation

A CSV dictionary remains useful for inspection, but v0.3 also supplies a JSON Schema so that record identifiers, enumerated values, conditional derivation metadata, and basic formats can be validated automatically (Additional files 3-5). The schema is not itself evidence that the selected fields are scientifically correct; it only prevents machine-readable definitions from silently diverging from the written specification.

A dataset should therefore be described only as **"PR-MDS v0.3 mapped"** or **"pilot-compatible"**. Certification language should not be used.

## 5. Demonstration Corpus, Not Evidence Synthesis

The current 28-record collection is retained only as a **demonstration corpus** for the mapping architecture (Additional file 1). It is not used to estimate the prevalence of research topics or to support treatment-effect claims.

The corpus was initially identified through broad discovery searches and coded at abstract level with AI assistance. Every record remains labeled `AI_ASSISTED_SEED` and `single_coded`. Additional file 2 defines the coding rules and now distinguishes `sample_size` from `sample_size_unit` so that participants, cases, injury events, publications, or other analytic units are not silently conflated.

A four-paper stress test was then used to ask a narrower engineering question: can the candidate layer represent substantially different study types without changing field meaning? The test covered (1) a nationwide injury survey [5], (2) an activity-intensity study comparing singles and doubles [7], (3) a randomized older-adult intervention [9], and (4) a computer-vision/kinematic study [13]. The exercise exposed predictable gaps: publication abstracts often did not report protocol version, precise exposure measurement methods, or derivation metadata; some studies required domain-specific variables beyond the universal core; and existing outcomes could be represented without forcing them into common categories.

This is useful for schema debugging but does **not** establish content validity. Formal evidence mapping would require reproducible multi-database searches, duplicate screening, full-text verification, shared-sample linkage, independent coding, and documented agreement.

## 6. Validation Must Precede Standard-Setting

The principal weakness of any founder-designed schema is legitimacy. OPRC explicitly recognizes that a useful candidate can still fail if outsiders find it burdensome, ambiguous, or unnecessary.

**Table 2. Promotion gates for PR-MDS and other OPRC components**

| Gate | Evidence required | Example outcomes | Decision |
|---|---|---|---|
| Structured external review | Independent sport epidemiology, data-standard, methods, and pickleball-domain review | necessity, ambiguity, omissions, overlap with existing standards | revise before field testing |
| Retrospective mapping | Multiple heterogeneous published or existing datasets | mapping coverage, ambiguity count, unmappable fields, time-to-map | retain, simplify, demote, split, or remove |
| Prospective feasibility | Independent study sites use the candidate core | missingness, burden, completion time, implementation failures | revise or continue |
| Reliability and semantic consistency | Independent coders/sites apply definitions | categorical agreement, interpretation conflicts, unit/derivation consistency | clarify or retire weak fields |
| Transportability | Use across countries, languages, skill levels, equipment, and settings | local exceptions, privacy conflicts, translation problems | localize, modularize, or reject universal status |
| Public governance | Transparent proposal, interests, adjudication, and release rules | accepted/rejected changes with rationale and audit trail | stable release only after independent oversight |

For v0.3, **human external review completed = 0** and **independent prospective pilot sites completed = 0**. The appropriate status is therefore *pre-consensus candidate*. These zeros should be treated as state variables, not hidden weaknesses.

## 7. Governance Must Reduce Founder Dependence

A repository is not automatically a commons. The current author is the founder and maintainer of OPRC, creating an obvious non-financial relationship to the proposal. Stable governance should therefore be designed to reduce unilateral founder control.

The proposed path is modest. Candidate changes should be submitted publicly with a rationale, affected variables, backwards-compatibility consequences, and supporting evidence. Stable-release decisions should require independent reviewers representing more than one domain and institution. Competing interests should be declared for decision participants. Rejected proposals and minority concerns should remain visible. Deprecated fields should not disappear silently; their replacement or retirement should remain in the version history. Authorship and contributor recognition should follow contribution rather than repository ownership.

The eventual success criterion is not that the founder can explain the system. It is that independent groups can use, criticize, modify, or decline it without the founder's assistance.

Four predictable failure modes should remain explicit: **premature lock-in**, **founder capture**, **scope inflation**, and **performative openness**. A v1.0 claim would be premature until multi-site use and external governance exist.

## 8. The Proposal Is Falsifiable

OPRC should not be judged by repository size, GitHub stars, or the number of candidate fields. It should be judged by whether the connective layer reduces real coordination costs.

Useful evaluation outcomes include applicable-field completion, missingness, mapping time, number and type of ambiguous mappings, inter-rater disagreement, success of cross-site linkage, reproducibility of derived variables, independent secondary uses, and whether successive versions measurably reduce burden without reducing interpretability.

PR-MDS should undergo major revision if independent users repeatedly require conflicting meanings, if important interpretation is not improved, if the same interoperability can be achieved with fewer fields, or if privacy and jurisdictional constraints make a purportedly universal field impractical. A field should be removed when persistence is explained mainly by path dependence rather than demonstrated utility.

This is also why OPRC should not declare a mandatory pickleball core outcome set. Outcome selection needs its own stakeholder process—including players, clinicians, coaches, researchers, and relevant communities—consistent with established core outcome-set methodology [19]. A context-and-provenance layer can support such work without pre-empting it.

## 9. Why Pickleball Is a Useful Test Case

The value of this proposal does not require pickleball to be uniquely important. It is useful as a bounded case in which injury surveillance, late-life sport adoption, open-skill exercise, social participation, biomechanics, and low-cost analytics are developing simultaneously.

Emerging sports may have a short period in which scholarship is growing but conventions remain unsettled. If a minimal context-and-provenance layer proves useful here, the transferable lesson is methodological: it may be cheaper to design connective infrastructure prospectively than to harmonize incompatible datasets retrospectively.

## 10. Conclusions

Outcome harmonization is not enough when the surrounding context of an observation is unclear. For pickleball research, a defensible early target is a small, versioned layer that preserves identifiers, participant and session context, exposure, data-source provenance, units, and derivation history across otherwise diverse studies.

OPRC and PR-MDS v0.3 offer one testable implementation. They explicitly complement established provenance, stewardship, injury-reporting, common-data-element, and core-outcome frameworks rather than replacing them. Their current status is pre-consensus. Stable status should be earned through external review, retrospective mapping, independent use, low burden, semantic reliability, transportability, and public governance.

The desired endpoint is deliberately limited: researchers should remain free to use different theories, outcomes, instruments, and analyses while making enough context interoperable that their findings can be interpreted within a wider evidence ecosystem.

## Use of Generative AI and Automated Assistance

OpenAI ChatGPT was used to assist with literature organization, schema-constrained demonstration-corpus coding, manuscript structuring, language revision, and consistency checks. It was not treated as an author, independent screener, external reviewer, or source of evidence. Bibliographic records and claims cited in the manuscript were reviewed by the author. The demonstration-corpus extraction remains abstract-level, AI-assisted, and not comprehensively full-text verified; this status is explicitly encoded in the supplementary file. The author selected the argument, finalized classifications, revised the manuscript, and accepts responsibility for the work. Figure 1 is generated deterministically from author-reviewed vector-diagram code rather than by generative image synthesis.

## List of Abbreviations

**CDE:** common data element  
**FAIR:** Findable, Accessible, Interoperable, and Reusable  
**IOC:** International Olympic Committee  
**OPRC:** Open Pickleball Research Commons  
**PR-MDS:** Pickleball Research Minimum Data Set  
**STROBE-SIIS:** Strengthening the Reporting of Observational Studies in Epidemiology—Sports Injury and Illness Surveillance  
**W3C PROV:** World Wide Web Consortium Provenance Data Model family

## Declarations

### Ethics Approval and Consent to Participate

Not applicable.

### Consent for Publication

Not applicable.

### Availability of Data and Materials

The 28-record demonstration corpus (Additional file 1), its coding manual (Additional file 2), the candidate PR-MDS v0.3 specification (Additional file 3), machine-readable dictionary (Additional file 4), and validation schema with stress-test examples (Additional file 5) support this Current Opinion. A frozen version-specific archival record will be deposited in Zenodo; the reserved DOI and dataset citation should be inserted before final journal submission. No identifiable participant-level data are included.

### Competing Interests

Kento Sasano is the founder and current maintainer of the Open Pickleball Research Commons described in this article. He declares no financial competing interests related to this work.

### Funding

No specific funding was received for this work.

### Authors' Contributions

KS conceptualized the article and OPRC framework; designed the candidate PR-MDS and demonstration architecture; reviewed and interpreted the literature; prepared the manuscript and supplementary materials; and approved the final manuscript.

### Acknowledgements

Not applicable.

## Additional Files

**Additional file 1 (.csv): OPRC Demonstration Corpus v0.3.** Twenty-eight study-level records used only to stress-test the mapping architecture. The corpus is AI-assisted, abstract-level, single-coded, and non-systematic.

**Additional file 2 (.txt): OPRC Demonstration Corpus Codebook v0.3.** Definitions for study design, domains, sample-size units, missingness, verification status, and coding provenance.

**Additional file 3 (.txt): PR-MDS Specification v0.3.** Human-readable pre-consensus candidate specification, core-selection rule, modules, provenance classes, and compatibility statement.

**Additional file 4 (.csv): PR-MDS Dictionary v0.3.** Machine-readable candidate variables, requirements, formats, definitions, provenance expectations, and module assignment.

**Additional file 5 (.json): PR-MDS JSON Schema and Stress-Test Examples v0.3.** Machine-validation rules and example records derived from four heterogeneous publication types; this tests schema behavior rather than scientific validity.

## References

1. Stroesser K, Mulcaster A, Andrews DM. Pickleball participation and the health and well-being of adults—a scoping review. J Phys Act Health. 2024;21(9):847-60. doi:10.1123/jpah.2024-0092.
2. Cerezuela JL, Lirola MJ, Cangas AJ. Pickleball and mental health in adults: a systematic review. Front Psychol. 2023;14:1137047. doi:10.3389/fpsyg.2023.1137047.
3. Forrester MB. Pickleball-related injuries treated in emergency departments. J Emerg Med. 2020;58(2):275-9. doi:10.1016/j.jemermed.2019.09.016.
4. Weiss H, Dougherty J, DiMaggio C. Non-fatal senior pickleball and tennis-related injuries treated in United States emergency departments, 2010-2019. Inj Epidemiol. 2021;8(1):34. doi:10.1186/s40621-021-00327-9.
5. Owoeye OBA, Yemm T, Blechle R, Wayne M, Kennedy D, Mourad W, et al. Understanding injury patterns and predictors in pickleball players: a nationwide study of 1,758 participants. Sports Med Open. 2025;11(1):100. doi:10.1186/s40798-025-00900-2.
6. Jeong B, Lee KJ, Nam SH, Im S, Lee RS, Heo J, et al. Injury risk and epidemiology of pickleball players in South Korea: a cross-sectional study. Front Public Health. 2025;13:1617291. doi:10.3389/fpubh.2025.1617291.
7. Webber SC, Anderson S, Biccum L, Jin S, Khawashki S, Tittlemier BJ. Physical activity intensity of singles and doubles pickleball in older adults. J Aging Phys Act. 2023;31(3):365-70. doi:10.1123/japa.2022-0194.
8. Wray P, Ward CK, Nelson C, Sulzer SH, Dakin CJ, Thompson BJ, et al. Pickleball for inactive mid-life and older adults in rural Utah: a feasibility study. Int J Environ Res Public Health. 2021;18(16):8374. doi:10.3390/ijerph18168374.
9. Zeng Z, Zheng X, Sit CHP, Wong SHS, Sum RKW, Yang Y. Effects of pickleball on pre-frailty, physical fitness, 24-hour movement behaviors, and quality of life in older adults: a randomized controlled trial. Int J Nurs Stud. 2026;180:105549. doi:10.1016/j.ijnurstu.2026.105549.
10. Kim ACH, Ryu J, Lee C, Kim KM, Heo J. Sport participation and happiness among older adults: a mediating role of social capital. J Happiness Stud. 2021;22(4):1623-41. doi:10.1007/s10902-020-00288-8.
11. Kurth JD, Casper JM, Sciamanna CN, Conroy DE, Silvis M, Hawkley L, et al. Association of pickleball participation with decreased perceived loneliness and social isolation: results of a national survey. J Prim Care Community Health. 2025;16:21501319251385855. doi:10.1177/21501319251385855.
12. Heo J, Ryu J. Maintaining active lifestyle through pickleball: a qualitative exploration of older pickleball players. Int J Aging Hum Dev. 2024;98(4):469-83. doi:10.1177/00914150231208012.
13. Edriss S, Romagnoli C, Maurizi M, Caprioli L, Bonaiuto V, Annino G. Pose estimation for pickleball players' kinematic analysis through MediaPipe-based deep learning: a pilot study. J Sports Sci. 2025;43(17):1860-70. doi:10.1080/02640414.2025.2524283.
14. Myers B, Hanks J. Hip strength, change of direction, and falls in recreational pickleball players. Int J Sports Phys Ther. 2024;19(9):1116-25. doi:10.26603/001c.122490.
15. Lebo T, Sahoo S, McGuinness D, editors. PROV-O: the PROV ontology. W3C Recommendation. World Wide Web Consortium; 2013. Available from: https://www.w3.org/TR/prov-o/.
16. Wilkinson MD, Dumontier M, Aalbersberg IJJ, Appleton G, Axton M, Baak A, et al. The FAIR Guiding Principles for scientific data management and stewardship. Sci Data. 2016;3:160018. doi:10.1038/sdata.2016.18.
17. National Library of Medicine. Common Data Elements: Standardizing Data Collection. Bethesda: NLM; updated resource. Available from: https://www.nlm.nih.gov/oet/ed/cde/tutorial/03-100.html.
18. Bahr R, Clarsen B, Derman W, Dvorak J, Emery CA, Finch CF, et al. International Olympic Committee consensus statement: methods for recording and reporting of epidemiological data on injury and illness in sport 2020, including STROBE-SIIS. Br J Sports Med. 2020;54(7):372-89. doi:10.1136/bjsports-2019-101969.
19. Williamson PR, Altman DG, Bagley H, Barnes KL, Blazeby JM, Brookes ST, et al. The COMET Handbook: version 1.0. Trials. 2017;18 Suppl 3:280. doi:10.1186/s13063-017-1978-4.
20. Warmenhoven J, Shrier I, Bullock GS, Holcombe AO, Nimphius S, Menaspa P, et al. Unifying to advance understanding: collaborative, community-driven and open approaches for better science in sport. Sports Med. 2026;56(4):845-59. doi:10.1007/s40279-026-02394-8.
