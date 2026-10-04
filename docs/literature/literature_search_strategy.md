# Literature Search Strategy

## Purpose

The literature search was conducted to identify research relevant to the proposed study:

**Predicting Non-Use of Skilled Birth Attendance in Nigeria Using Pre-Delivery Information: Evidence from the 2024 Nigeria Demographic and Health Survey.**

The purpose of the search was to establish what is already known about skilled birth attendance, identify relevant statistical and machine-learning approaches, examine limitations in previous research, and develop an evidence-based research gap.

This was a **targeted literature search conducted for the development of a research proposal**, rather than a systematic review. The search therefore aimed to identify a focused set of highly relevant studies rather than exhaustively retrieve every publication on skilled birth attendance.

---

## Search Topics

The literature search focused on the following areas:

- Skilled birth attendance in Nigeria
- Determinants of skilled birth attendance
- Nigeria Demographic and Health Survey (NDHS)
- Skilled versus unskilled birth attendance
- Machine learning and skilled birth attendance
- Machine learning using DHS data
- Explainable machine learning in maternal health
- Pre-delivery prediction and predictor timing
- Model calibration and validation
- Class imbalance and prediction-model evaluation
- Clustered data and prediction-model validation
- Regional, community and socioeconomic differences in maternal healthcare utilisation

---

## Information Sources

Relevant studies and methodological publications were identified through targeted searches of academic and publisher sources available during the literature review.

The main sources used included:

- PubMed
- Google Scholar
- Publisher and journal websites
- The DHS Program
- Reference lists and citations from relevant studies

When a potentially relevant study was identified, the original article or publisher record was prioritised for verification rather than relying only on secondary summaries.

---

## Search Terms

Searches used combinations and variations of terms such as:

- `"skilled birth attendance" Nigeria`
- `"skilled birth attendant" Nigeria DHS`
- `"skilled birth attendance" NDHS`
- `"unskilled birth attendants" Nigeria`
- `"maternal healthcare utilisation" Nigeria DHS`
- `"skilled birth attendance" "machine learning"`
- `"skilled birth attendance" prediction`
- `"Demographic and Health Survey" "machine learning" maternal health`
- `"Nigeria DHS" "machine learning"`
- `"explainable machine learning" maternal health`
- `"SHAP" maternal health DHS`
- `"prediction model" calibration`
- `"precision recall" imbalanced classification`
- `"clustered data" prediction model validation`
- `"TRIPOD-Cluster"`
- `"community-level" skilled birth attendance Nigeria`
- `"women's autonomy" skilled birth attendance Nigeria`

Search terms were refined during the review when relevant terminology, authors or related studies were identified.

---

## Study Selection Criteria

### Inclusion Criteria

Studies were considered for inclusion when they met one or more of the following criteria:

- Examined skilled birth attendance, delivery assistance or closely related maternal-healthcare utilisation.
- Focused on Nigeria or provided evidence relevant to Nigeria or Sub-Saharan Africa.
- Used Nigeria DHS, other DHS datasets or comparable nationally representative survey data.
- Investigated demographic, socioeconomic, healthcare-access, geographical or community factors related to skilled birth attendance.
- Applied machine-learning methods to skilled birth attendance or closely related maternal-health outcomes.
- Examined model interpretation, calibration, validation, class imbalance or clustered prediction data in a way relevant to the proposed methodology.
- Provided evidence relevant to predictor timing, model evaluation or subgroup performance.

Peer-reviewed original research was prioritised for the main literature review. Methodological papers and authoritative survey documentation were also used where necessary to support the proposed analytical approach.

### Exclusion Criteria

Studies were generally excluded when they:

- Had little or no relevance to skilled birth attendance, maternal healthcare or the proposed prediction problem.
- Did not provide sufficient methodological or outcome information for the purpose of the review.
- Were secondary summaries when the original research article could be located.
- Could not be sufficiently verified from an original or reliable publication source.
- Duplicated evidence already represented more directly by a more relevant study.

---

## Study Screening and Selection

Potential studies were initially assessed using their titles and abstracts.

Studies that appeared relevant were examined in greater detail to determine their relationship to the proposed research.

Particular attention was given to:

- Country and study setting
- Dataset and DHS survey year
- Study population and sample size
- Outcome definition
- Statistical or machine-learning methods
- Predictors or associated factors
- Model-evaluation metrics
- Predictor timing
- Potential data leakage
- Calibration
- Validation approach
- Explainability methods
- Community or geographical effects
- Subgroup performance
- Strengths and limitations
- Relevance to the proposed research

A final set of **12 studies** was selected for detailed review because, collectively, they provided evidence on Nigeria-specific skilled birth attendance, DHS-based maternal-health research, machine-learning prediction, predictor timing, geographical and socioeconomic differences, and methodological issues relevant to the proposed study.

---

## Verification Process

The selected studies were checked individually before being used to support the proposal.

Where available, verification was based on the original full-text publication, journal webpage, DOI record or other authoritative publication source.

For each main study, the review recorded and checked relevant information including:

- Authors
- Publication year
- Paper title
- Publication status
- Country or countries studied
- Dataset and survey year
- Sample size where reported
- Research objective
- Outcome
- Methods or models
- Important predictors or associated factors
- Evaluation metrics where applicable
- Main findings
- Limitations
- Relevance to the proposed research
- Full citation and DOI

Particular attention was given to the preliminary studies identified during topic development, including the Sub-Saharan African machine-learning study by Taye et al., the Uganda interpretable machine-learning study, and the Burkina Faso machine-learning study.

---

## Approach to Establishing the Research Gap

The research gap was developed by comparing the selected studies rather than assuming that a gap existed.

The comparison examined:

- Whether Nigeria was studied independently or as part of a pooled multi-country dataset
- Which NDHS or DHS survey years were used
- Whether the 2023–24 Nigeria DHS was used
- Whether the research focused on statistical association or prediction
- Whether machine-learning models were compared
- Whether predictors represented information realistically available before childbirth
- Whether variables that could introduce data leakage were included
- Whether calibration was evaluated
- Whether the clustered structure of DHS data was considered
- Whether predictive performance was assessed across geographical or socioeconomic groups
- Whether explainability methods were used

This comparison showed that the proposed contribution should not be based simply on the use of machine learning. Instead, the research gap identified from the reviewed literature concerns the combination of a **Nigeria-specific prediction problem, recent 2023–24 NDHS data, a clearly defined pre-delivery prediction framework, careful control of predictor timing, evaluation of probability calibration, consideration of clustered survey data, and assessment of performance across relevant population groups**.

---

## Limitations of the Literature Search

This literature search was designed to support a research proposal and was not conducted as a formal systematic review.

Therefore:

- The search was targeted rather than exhaustive.
- Formal systematic-review procedures such as duplicate independent screening were not used.
- A PRISMA flow diagram was not produced.
- No claim is made that every publication relevant to skilled birth attendance was identified.

To reduce the risk of unsupported conclusions, claims about the research gap were therefore framed cautiously. The proposal refers to what was identified **among the studies reviewed** rather than claiming that no similar research exists anywhere in the literature.

---

## Search Outcome

The literature-search and verification process resulted in:

- 12 studies selected for detailed review
- Nigeria-specific evidence on skilled birth attendance and its associated factors
- Machine-learning studies relevant to skilled birth attendance
- Evidence concerning individual, household, community and geographical factors
- Identification of predictor-timing and potential data-leakage concerns
- Methodological evidence supporting discrimination, calibration and class-specific evaluation
- Methodological evidence concerning prediction models developed or validated using clustered data
- An evidence-based research gap for the proposed study

Detailed notes for the selected studies and the cross-study synthesis are maintained within `docs/literature/`.
