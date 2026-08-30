# Standardize Provenance Before Outcomes: A Research Commons for Cumulative Pickleball Science

**Article type:** Current Opinion  
**Author:** Kento Sasano  
**Affiliation:** Faculty of Environmental, Life, Natural Science and Technology, Okayama University, 3-1-1 Tsushima-naka, Kita-ku, Okayama 700-8530, Japan  
**Corresponding author:** Kento Sasano; office@sasano.org

## Abstract

Pickleball research now spans injury epidemiology, exercise and health, aging, psychosocial outcomes, biomechanics, and technology. This breadth creates a brief coordination window: the field can build shared research infrastructure before incompatible conventions become entrenched. This Current Opinion argues that an emerging sport should standardize provenance, exposure, identifiers, and versioning before attempting field-wide harmonization of outcomes. It proposes the Open Pickleball Research Commons (OPRC), an open, modular, and versioned scaffold linking a Living Evidence Map, the Pickleball Research Minimum Data Set (PR-MDS), candidate field protocols, and shared benchmark modules. PR-MDS is deliberately not a core outcome set, reporting guideline, or universal protocol. It defines the minimum descriptive context needed to interpret and connect otherwise heterogeneous studies while leaving theories, outcomes, instruments, and analyses study-specific. A frozen 28-record Evidence Map is used only as an engineering proof of concept; because its seed coding was AI-assisted, abstract-level, and single-coded, it is not treated as a systematic review or evidence of topic prevalence. OPRC is therefore a falsifiable infrastructure proposal, not a claim of standard-setting authority. Components should advance only if independent testing demonstrates low burden, reliable interpretation, cross-site usefulness, and transparent governance; weak components should be revised or retired. The appropriate target is minimum sufficient interoperability, not maximum standardization.

## Key Points

- Before field-wide outcome harmonization, emerging sport research needs shared identifiers, provenance, exposure definitions, and versioning.
- OPRC links a Living Evidence Map, a minimal data layer, candidate protocols, and benchmarks without prescribing study-specific theories or outcomes.
- OPRC should be judged by independent reuse, validation, and public change control; candidate components that fail should be revised or retired.

## 1. Pickleball Has a Brief Coordination Window

Pickleball has moved rapidly from recreation into a multidisciplinary research object. Reviews now synthesize health and well-being [1] and mental health [2]. Injury research includes emergency-department surveillance [3,4], a large nationwide player survey [5], and studies outside the United States [6]. Other work has quantified physical-activity intensity [7], tested pickleball interventions [8,9], examined social capital and loneliness [10,11], explored older players' experiences [12], and applied computer vision to sport-specific movement [13]. A court-based change-of-direction test has also been used in research on falls [14].

This breadth is welcome, but it creates a coordination problem. Two studies can both report "experience" while using months, years, informal skill labels, or incompatible rating systems. Injury studies can count emergency-department presentations, all complaints, time-loss injuries, or overuse conditions without comparable exposure denominators. Social studies can measure loneliness or belonging without distinguishing selection into the sport from social effects of participation. Technology studies can report performance on private datasets with labels that cannot be compared across systems. Each decision may be reasonable within one study; the cumulative cost becomes visible only when evidence must be compared, pooled, replicated, or reused.

Sport science is already moving toward more collaborative, community-driven, and open approaches [15]. The FAIR principles similarly emphasize that data and metadata become more useful when they are findable, accessible, interoperable, and reusable [16]. Pickleball offers a tractable case because its evidence base is still young enough to build connective infrastructure prospectively rather than reconstruct it after decades of fragmentation.

The opportunity is not to impose a single method. It is to agree on enough descriptive context that different methods remain interpretable together.

## 2. Standardize Provenance Before Outcomes

The phrase "standardize provenance before outcomes" describes methodological priority, not a chronological ban on outcome research. Pickleball studies should continue to investigate injury, health, performance, and social outcomes. The narrower claim is that a field-wide effort to harmonize outcomes will be fragile if researchers cannot first identify what was observed, in whom, under which protocol, from which source, and under what amount and format of exposure.

This ordering matters because several kinds of standardization solve different problems. A reporting guideline specifies what a manuscript should report; the International Olympic Committee consensus and STROBE-SIIS, for example, address injury and illness definitions, exposure, and reporting in sport [17]. A core outcome set identifies outcomes that should be measured and reported in a defined research area [18]. A minimum data set can instead provide a small cross-study data layer. An evidence map organizes where evidence exists and how it has been studied. Conflating these instruments risks either overloading a minimum data set or presenting an early repository as a consensus standard.

**Table 1. What OPRC adds - and what it does not replace**

| Element | Primary function | Explicit boundary |
|---|---|---|
| PR-MDS | Shares identifiers, provenance, participant context, and exposure descriptors across study types | Not a core outcome set, reporting checklist, certification scheme, or universal protocol |
| Core outcome set | Identifies outcomes that should be measured in a defined research area | Not proposed for pickleball by OPRC v0.1; would require a separate stakeholder process |
| Reporting guideline | Specifies information that authors should report for a study design or domain | Not replaced by PR-MDS; relevant guidance such as STROBE-SIIS still applies |
| Living Evidence Map | Tracks studies, designs, domains, measures, and verification status over time | Not a pooled analysis or systematic review unless systematic search, screening, and verification are completed |

The proposed target is therefore **minimum sufficient interoperability**. Scientific diversity should remain in theories, outcomes, instruments, designs, and analyses. Avoidable incompatibility should be reduced in identifiers, exposure, source provenance, units, derivation rules, and version history.

## 3. OPRC: Four Components, One Narrow Purpose

The Open Pickleball Research Commons is an open, modular, and versioned research scaffold. It is not an official federation standard, accreditation body, or claim that one research group should govern the field. Its narrow purpose is to make independently designed pickleball studies easier to interpret and connect.

OPRC has four linked components (Fig. 1). The **Living Evidence Map** tracks studies, constructs, methods, and verification status. **PR-MDS** supplies a minimal common data layer. **Candidate field protocols** preserve task scripts, raw observations, instruments, units, and assessor rules so that measurements can be tested rather than merely named. **Research and benchmark modules** support domain-specific work, including injury, physical function, social connection, match analysis, and computer vision.

These components are joined by a validation cycle. Evidence mapping identifies recurring constructs and gaps. Candidate fields, protocols, or labels are proposed. Independent users test feasibility and interpretation. Multi-site studies assess reliability, validity, and transportability. Public governance then retains, revises, splits, or retires components. Stable releases are archived with persistent identifiers, while new evidence returns to the map.

**[Insert Figure 1 near here]**

**Figure 1. OPRC architecture and validation cycle.**  
Panel A shows how a Living Evidence Map, PR-MDS, candidate protocols, and domain benchmarks provide shared connective tissue while theories, outcomes, instruments, and analyses remain study-specific. Panel B shows the promotion path from candidate proposal through independent pilot use, multi-site validation, and public governance. A component can be stabilized, revised, split, or retired; publication in an early version does not guarantee promotion.

## 4. PR-MDS as a Minimum Interoperable Layer

PR-MDS v0.1 is a candidate specification for field testing, not an established international standard. Its design rule is **minimum common core, extensible modules**.

The provenance core includes record and study identifiers, protocol version, site, collection date, country, and data-source type. These fields distinguish, for example, a self-reported injury from a clinical record, a manually coded shot from an algorithmic inference, and a measured heart rate from a transcribed value. Provenance is part of the scientific meaning of an observation, not administrative decoration.

The participant core currently includes a pseudonymous identifier, age band, dominant hand, pickleball experience, the name and value of any skill-rating system, and prior racket or paddle-sport experience. A rating value should never be separated from its rating system. Demographic variables such as sex, gender, disability, and socioeconomic position may be essential for particular questions, but their definitions, sensitivity, and legal handling vary. Their placement outside the universal v0.1 core is provisional rather than a claim that they are unimportant; field testing should determine which belong in future core or domain modules.

The session and exposure core includes session type, play format, indoor or outdoor setting, session duration, active-play duration when available, and games played. This layer is especially important because exposure is a denominator for injury burden, physical-activity dose, learning, fatigue, social-contact opportunity, and performance change. The IOC consensus likewise treats athlete exposure as fundamental to interpreting sports injury and illness data [17].

Specialized modules can add match, rally, shot, position, injury, pain, physical-function, social-network, or device variables. The modular design prevents a public-health study from being forced to collect shot-level kinematics and prevents a computer-vision dataset from being forced to administer a psychosocial battery. Both can still preserve enough provenance and exposure context for later reuse.

A dataset should therefore be described as **"PR-MDS v0.1 mapped"** or **"pilot-compatible,"** not "certified." Compatibility should report the version used, unmapped fields, missingness, deviations, and derivation rules.

## 5. A Living Evidence Map Without False Completeness

A static review can become outdated quickly in an emerging field, while an uncurated bibliography becomes difficult to audit. The Living Evidence Map is intended to preserve citable snapshots while allowing new records, corrections, duplicate links, and coding decisions to be added transparently.

The current frozen seed contains 28 scholarly records. Its purpose was to test whether the proposed schema could represent heterogeneous designs and expose practical metadata problems. It did: data-collection country was sometimes absent from abstracts; weighted national estimates could be mistaken for sample sizes; skill and exposure variables were inconsistently reported; and closely related injury outcomes used non-equivalent definitions.

The seed should not be used to estimate the true distribution of pickleball research. It was identified through broad discovery searches, coded at abstract level with AI assistance, and not independently double-coded. Every record is therefore marked `AI_ASSISTED_SEED` and `single_coded`. Formal evidence-mapping claims require reproducible multi-database searches, duplicate screening, full-text verification, shared-sample linkage, independent coding, and documented agreement.

This boundary is not a weakness to conceal; it is a governance feature. A living map should display the verification state of each record so that automation accelerates organization without masquerading as independent scholarly judgment.

## 6. Validation and Governance Are Part of the Method

A repository is not automatically a commons. GitHub can store files, but scientific legitimacy requires external use, understandable documentation, public change control, versioned decisions, and the ability to remove weak components.

**Table 2. Validation gates for candidate OPRC components**

| Gate | What should be tested | Possible decision |
|---|---|---|
| Feasibility | Completion time, missingness, burden, ambiguity, and implementation failures | Retain, simplify, demote to a module, or remove |
| Reliability | Inter-rater agreement, test-retest stability, assessor effects, and coding consistency | Clarify definitions, restrict intended use, or retire |
| Validity and utility | Construct or criterion validity, discrimination, sensitivity, and contribution to interpretation or reuse | Promote only for supported uses; avoid unsupported score meaning |
| Transportability | Performance across sites, skill levels, countries, languages, equipment, and community settings | Localize, split modules, or reject universal status |
| Governance | Independent review, declared interests, public rationale, backwards compatibility, and archived releases | Stabilize, revise, fork, or deprecate with an audit trail |

Four failure modes deserve explicit attention. First, **premature lock-in** can freeze weak definitions simply because they were proposed early. Second, **founder capture** can turn an open repository into a project that outsiders can view but cannot meaningfully change. Third, **scope inflation** can make a minimum core burdensome enough that no ordinary study adopts it. Fourth, **performative openness** can privilege English-language, well-resourced contributors or encourage unsafe release of identifiable video and health data.

Safeguards should therefore include public proposals for field changes, independent reviewers before stable releases, declared competing interests, semantic versioning, deprecation rather than silent replacement, multilingual testing, and "open where possible, protected where necessary" data governance. Before any v1.0 claim, OPRC should have documented use by multiple independent sites and a governance process in which the originating author does not have unilateral control.

## 7. The Proposal Should Be Falsifiable

OPRC should not be judged by the number of repository files, GitHub stars, or fields accumulated. It should be judged by whether independent researchers can use it without the founder's assistance and whether it lowers real coordination costs.

Useful evaluation outcomes include the proportion of applicable core fields that can be completed, time required to map an existing dataset, disagreement over definitions, success of cross-site data linkage, reproducibility of derived variables, number of independent secondary uses, and whether documented revisions reduce burden or ambiguity. No universal numerical threshold should be declared in advance; each validation study should predefine thresholds appropriate to the intended use.

The proposal would need major revision if the core produces high missingness, if independent coders cannot apply it reliably, if multi-site users repeatedly require incompatible local meanings, or if the same interoperability can be achieved with less burden. A component should be retired when it persists mainly because it is already present.

This is also why OPRC should not begin with a mandatory pickleball core outcome set. Outcome selection requires its own stakeholder process, including players, clinicians, coaches, researchers, and relevant communities [18]. A provenance-and-exposure layer is a lower-burden starting point that can later support, but should not pre-empt, such consensus work.

## 8. Why Pickleball Is More Than a Niche Example

The value of this proposal does not depend on pickleball being uniquely important. Pickleball is useful as a bounded case in which researchers can study late-life sport adoption, open-skill exercise, injury, social interaction, low-cost analytics, and intergenerational recreation while also observing the formation of a scientific field.

If the infrastructure proves useful, its transferable lesson is simple: emerging sports may have a short period in which participation, technology, and scholarship are growing but conventions remain unsettled. Building a minimal data layer, living evidence architecture, and public validation process during that period may be cheaper and more inclusive than retrospective harmonization.

## 9. Conclusions

Pickleball research is young enough that coordination can still be designed rather than repaired. The most defensible first step is not a universal protocol or mandatory outcome set. It is a minimal, versioned layer that preserves identifiers, provenance, exposure, and derivation context across otherwise diverse studies.

OPRC offers one testable implementation through a Living Evidence Map, PR-MDS, candidate protocols, and benchmark modules. Its components should earn stable status through independent use, low burden, reliability, validity, transportability, and public governance. Adoption should follow usefulness, and failure should be allowed to remove weak components.

The desired endpoint is modest but consequential: a study should be able to use its own theory, outcomes, and methods while making its core context interoperable with a wider pickleball evidence ecosystem.

## Use of Generative AI and Automated Assistance

OpenAI ChatGPT was used to assist with literature organization, schema-constrained seed coding, manuscript structuring, and language revision. It was not treated as an author, independent screener, verifier, or source of evidence. The author selected the argument, reviewed the cited sources and extracted fields, revised the text, and accepts full responsibility for the accuracy, originality, interpretation, and references. AI-assisted Evidence Map records are explicitly labeled as single-coded. Figure 1 was generated deterministically from author-reviewed vector-diagram code rather than by generative image synthesis.

## List of Abbreviations

**AI:** artificial intelligence  
**OPRC:** Open Pickleball Research Commons  
**PB-Bench:** proposed Pickleball Benchmark  
**PR-MDS:** Pickleball Research Minimum Data Set  
**STROBE-SIIS:** Strengthening the Reporting of Observational Studies in Epidemiology - Sports Injury and Illness Surveillance

## Declarations

### Ethics Approval and Consent to Participate

Not applicable.

### Consent for Publication

Not applicable.

### Availability of Data and Materials

The proof-of-concept Evidence Map, coding manual, candidate PR-MDS specification and dictionary, and field measurement protocol supporting this Current Opinion are included as additional files. A frozen, version-specific archival record will be deposited in Zenodo; the reserved DOI and dataset citation will be inserted before final journal submission. No identifiable participant-level data are included.

### Competing Interests

Kento Sasano declares that he has no competing interests.

### Funding

No specific funding was received for this work.

### Authors' Contributions

KS conceptualized the article and OPRC framework; designed the PR-MDS, Evidence Map schema, and research agenda; reviewed and interpreted the literature; prepared the figure and supplementary materials; drafted and revised the manuscript; and approved the final manuscript.

### Acknowledgements

Not applicable.

## Additional Files

**Additional file 1 (.csv): Proof-of-concept Pickleball Evidence Map v0.1.** Study-level seed corpus used to test the mapping schema. Coding is AI-assisted, abstract-level, and single-coded; the file is not a systematic review or independently verified evidence synthesis.

**Additional file 2 (.txt): Pickleball Evidence Map Coding Manual v0.1.** Definitions for study design, domains, missingness, verification status, and coding provenance.

**Additional file 3 (.txt): Pickleball Research Minimum Data Set (PR-MDS) v0.1.** Human-readable candidate specification, compatibility statement, and validation questions.

**Additional file 4 (.csv): PR-MDS v0.1 machine-readable variable dictionary.** Core variables, requirements, formats, definitions, and provenance expectations.

**Additional file 5 (.txt): Pickleball Field Measurement Protocol v0.1.** Candidate low-cost court-based measurement battery and validation requirements.

## References

1. Stroesser K, Mulcaster A, Andrews DM. Pickleball participation and the health and well-being of adults-a scoping review. J Phys Act Health. 2024;21(9):847-60. doi:10.1123/jpah.2024-0092.
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
15. Warmenhoven J, Shrier I, Bullock GS, Holcombe AO, Nimphius S, Menaspa P, et al. Unifying to advance understanding: collaborative, community-driven and open approaches for better science in sport. Sports Med. 2026;56(4):845-59. doi:10.1007/s40279-026-02394-8.
16. Wilkinson MD, Dumontier M, Aalbersberg IJJ, Appleton G, Axton M, Baak A, et al. The FAIR Guiding Principles for scientific data management and stewardship. Sci Data. 2016;3:160018. doi:10.1038/sdata.2016.18.
17. Bahr R, Clarsen B, Derman W, Dvorak J, Emery CA, Finch CF, et al. International Olympic Committee consensus statement: methods for recording and reporting of epidemiological data on injury and illness in sport 2020, including STROBE-SIIS. Br J Sports Med. 2020;54(7):372-89. doi:10.1136/bjsports-2019-101969.
18. Williamson PR, Altman DG, Bagley H, Barnes KL, Blazeby JM, Brookes ST, et al. The COMET Handbook: version 1.0. Trials. 2017;18 Suppl 3:280. doi:10.1186/s13063-017-1978-4.
