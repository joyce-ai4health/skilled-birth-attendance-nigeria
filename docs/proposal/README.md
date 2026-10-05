# Research Proposal

## Project Title

Predicting Non-Use of Skilled Birth Attendance in Nigeria Using Pre-Delivery Information: Evidence from the 2024 Nigeria Demographic and Health Survey

## Author 

- Intern Name(s): Joyce Ebruphiyo Etata
- Programme: Dataraflow  Internship
- Date: October 2026

---

## Abstract

*To be completed after the main proposal. Target: 200–300 words.*

---


## 1. Introduction / Background

Maternal health remains an important public-health priority because pregnancy and childbirth can involve complications that require timely recognition and appropriate care. One important component of safe childbirth is access to skilled health personnel who have the competencies required to provide appropriate care during labour and delivery and to identify, manage or refer women and newborns when complications occur. Skilled birth attendance is therefore recognised internationally as an important indicator of maternal healthcare coverage and is included as Sustainable Development Goal (SDG) indicator 3.1.2 (World Health Organization [WHO], n.d.).

Despite the importance of skilled care during childbirth, access remains uneven in Nigeria. According to the 2024 Nigeria Demographic and Health Survey (NDHS), among live births in the two years before the survey, 46% were assisted by a skilled provider, most commonly a nurse or midwife. During the same period, 43% of live births occurred in a health facility, while 56% occurred at home (National Population Commission [NPC] & ICF, 2025). These national figures also conceal substantial socioeconomic inequalities. Home delivery was reported for 82% of births among women with no education and 82% among women in the poorest households (NPC & ICF, 2025). These patterns demonstrate that access to skilled childbirth care remains an important maternal-health challenge in Nigeria.

Previous Nigerian research has identified several characteristics associated with skilled birth attendance, including maternal education, household wealth, geographical location, urban or rural residence, antenatal care, healthcare accessibility, media exposure and women's participation in healthcare decision-making (Fagbamigbe & Oyedele, 2022; Solanke & Rahman, 2018).

This distinction between association and prediction is important. Association studies can help identify relationships between maternal, household and community characteristics and skilled birth attendance. A prediction study has a different objective: to determine how well available information can distinguish between individuals who will and will not experience a specified outcome. In the context of skilled birth attendance, a useful prediction framework could potentially identify women at greater risk of giving birth without skilled attendance early enough for the information to support targeted maternal-health interventions or further assessment.

The timing of predictor information is particularly important for such a model. A model intended for use before childbirth should not depend on information that becomes available only during or after the delivery being predicted. Variables such as the actual place of delivery, delivery complications or newborn outcomes may be strongly related to skilled birth attendance but would not represent realistic pre-delivery information for the same birth. Even antenatal-care variables require careful consideration because the information available depends on the point during pregnancy at which prediction is intended to occur. Clearly defining the prediction point and restricting predictors accordingly can therefore help reduce the risk of data leakage and produce a more realistic assessment of predictive performance.

The 2024 NDHS provides an opportunity to investigate this question using recent nationally representative Nigerian data. The survey contains information on maternal and reproductive health, socioeconomic circumstances, healthcare utilisation, women's empowerment and other demographic and health characteristics (NPC & ICF, 2025). However, the final analytical population, outcome construction, candidate predictor set and missing-data profile for the proposed study will be determined only after the relevant NDHS datasets and documentation have been systematically audited. This proposal therefore does not assume analytical results that have not yet been produced.

This study proposes to develop and evaluate models for predicting non-use of skilled birth attendance in Nigeria using information that could reasonably be available before childbirth. The research will distinguish prediction from statistical association, compare an interpretable baseline with appropriate machine-learning approaches, and evaluate discrimination, class-specific performance and calibration. Model-interpretation methods will be used to examine influential predictive characteristics without treating predictive importance as evidence of causality. The study will also consider the clustered structure of the NDHS and, where supported by the available data, examine predictive performance across important geographical and socioeconomic groups.

The study is predictive rather than causal and will not attempt to establish that identified characteristics cause non-use of skilled birth attendance. It is also intended as a research framework rather than a clinical decision tool. Its expected contributions include a clearly defined pre-delivery prediction framework, evidence on model discrimination and calibration, assessment of performance across relevant population groups where sample sizes permit, and a reproducible analytical pipeline for working with the 2024 NDHS while respecting DHS data-use requirements.

---

## 2. Related Work & Literature Review

### 2.1 Skilled Birth Attendance and Maternal Healthcare Utilisation

Skilled birth attendance is an important component of maternal healthcare because access to appropriately trained health professionals during childbirth can support the recognition and management of complications. In Nigeria, previous research has consistently shown that the use of skilled birth attendants is influenced by a combination of individual, household, healthcare-access, geographical and community characteristics.

Nigeria-specific studies using Demographic and Health Survey data have repeatedly identified maternal education, household wealth, place of residence, geographical region, healthcare accessibility, antenatal care, media exposure, parity and women's participation in healthcare decision-making as important factors associated with skilled birth attendance. The recurrence of these characteristics across studies suggests that non-use of skilled birth attendance cannot be adequately understood through a single individual-level factor. Instead, maternal healthcare utilisation reflects a combination of socioeconomic circumstances, healthcare access and the broader environment in which women live.

Solanke and Rahman (2018), for example, examined assistance during delivery among rural Nigerian women using the 2013 Nigeria Demographic and Health Survey. Their multilevel analysis demonstrated the importance of considering both individual and community characteristics. Maternal education, parity, religion, participation in healthcare decision-making, access to mass media and means of transportation were among the relevant individual-level factors, while community literacy, poverty, perceived distance to healthcare and geographical region were also important. The study therefore demonstrates that maternal healthcare utilisation may be influenced not only by a woman's individual circumstances but also by the community in which she lives.

Fagbamigbe and Oyedele (2022) further examined trends, inequalities and drivers of change in skilled birth attendant utilisation across five Nigeria DHS rounds from 1990 to 2018. Skilled birth attendant use remained relatively low despite improvement over time. Their multivariate decomposition analysis showed that 11.5% of the change between 2003 and 2018 was attributable to differences in population characteristics, while 88.5% was attributable to differences in the effects of those characteristics. Women's participation in healthcare decision-making and rural population characteristics were among the important contributors to changes in skilled birth attendant utilisation.

More recent Nigeria-specific evidence also indicates substantial inequalities in skilled birth attendance. In a recent preprint, Unegbu (2026), using the 2018 NDHS, reported a weighted skilled birth attendance prevalence of 44.9%, with considerable regional variation. Skilled birth attendance ranged from 17.7% in the North West to 85.6% in the South West. These geographical differences reinforce the importance of considering regional context when studying skilled birth attendance in Nigeria.

Taken together, these studies provide substantial evidence about factors associated with skilled birth attendance. However, much of the Nigeria-specific literature has primarily addressed an explanatory question— which characteristics are associated with skilled birth attendance? — rather than a predictive question concerning whether women at risk of non-use can be identified before childbirth.

### 2.2 Machine Learning for Predicting Skilled Birth Attendance

Recent research has increasingly explored whether machine-learning methods can be used to predict skilled birth attendance and related maternal-health outcomes using DHS data. These studies extend conventional association-based analyses by developing predictive models and evaluating how accurately they distinguish between women with different maternal healthcare outcomes.

Taye et al. (2025) applied a Random Forest classifier to DHS data from a weighted sample of 198,707 women across 27 sub-Saharan African countries, including Nigeria. The study reported strong predictive performance, with a ROC-AUC of 92%, accuracy of 92%, precision of 93%, recall of 96% and F1-score of 93% in the abstract. SHAP was used to interpret the model and identify influential predictors. These included facility delivery, maternal education, household wealth, urban residence, healthcare accessibility, media exposure and internet use.

Memon et al. (2025) adopted a broader model-comparison approach using the 2016 Uganda DHS. Seven supervised learning algorithms were compared, including logistic regression, Random Forest, Gradient Boosting, XGBoost, LightGBM, Decision Tree and CatBoost. XGBoost produced the highest ROC-AUC of 0.7473. Importantly, the study also examined performance for women who did not use skilled birth attendance, with XGBoost achieving a recall of 0.73 for this group. This demonstrates the importance of considering performance for the population of greatest public-health interest rather than relying solely on overall accuracy.

Explainable machine learning has also been applied to skilled birth attendance in Burkina Faso. Miah (2026) used the 2021 Burkina Faso DHS and compared five machine-learning models. Random Forest achieved the strongest reported discrimination, with an AUROC of 0.71. The study also incorporated feature selection, SHAP-based interpretation and spatial analysis, illustrating how prediction can be combined with explainability and geographical investigation.

Nigeria-specific machine-learning evidence is also emerging for related maternal-health service-utilisation outcomes. Sani et al. (2026), for example, applied seven machine-learning algorithms to predict institutional delivery dropout among Nigerian women using the 2018 NDHS. Although institutional delivery dropout is not identical to non-use of skilled birth attendance, the study is methodologically relevant because it demonstrates the application of machine learning and SHAP interpretation to a related maternal-health service-utilisation problem in Nigeria.

Consequently, the contribution of the proposed research cannot be based simply on the application of machine learning to Nigerian maternal-health data. A more specific methodological and substantive gap must be considered.

### 2.3 Predictor Timing and the Need for a Pre-Delivery Framework

An important methodological issue identified from the reviewed prediction studies concerns when predictor information becomes available.

For a model intended to identify women at risk before childbirth, predictors should represent information that would realistically be known at the intended prediction point. Using information generated during or after the outcome event can introduce data leakage and may result in an unrealistically optimistic assessment of predictive performance.

This issue is illustrated by Taye et al. (2025), whose model included facility delivery among the important predictors of skilled birth attendance. Although place of delivery may be strongly associated with skilled attendance, the actual place where a woman gives birth would not be known before the same delivery. It would therefore not be appropriate as a predictor in a model intended to identify risk before childbirth.

Other variables also require careful consideration. Delivery complications and newborn outcomes, for example, occur during or after childbirth and would therefore not be suitable for a pre-delivery model predicting the same delivery.

Antenatal-care variables require a more nuanced approach. ANC occurs before childbirth and may provide valuable predictive information. However, the suitability of variables such as the total number of ANC visits depends on the intended prediction point. A woman's final number of ANC visits would not be available early in pregnancy because some visits may not yet have occurred.

Similarly, previous place-of-delivery information may be appropriate if it refers to an earlier birth but inappropriate if it refers to the same birth being predicted. Therefore, variable labels alone are insufficient for determining predictor eligibility; the timing and meaning of each variable must be examined carefully.

The proposed research will consequently define a clear pre-delivery prediction point before final predictor selection. Candidate variables will be evaluated not only according to their statistical relevance but also according to whether the information could realistically have been known by that prediction point. Variables containing information from the index delivery or from events occurring after the prediction point will be excluded from the primary prediction model.

### 2.4 Model Evaluation, Calibration and Explainability

The reviewed machine-learning literature demonstrates that model performance can be evaluated using several complementary measures, including accuracy, precision, recall, F1-score and ROC-AUC. These measures provide different information about predictive performance and should not be treated as interchangeable.

For the proposed research, performance among women who do not use skilled birth attendance is particularly important. A model could achieve high overall accuracy while performing poorly in identifying this group, particularly when the outcome classes are imbalanced. Evaluation should therefore include class-specific measures such as precision, recall and F1-score in addition to overall discrimination.

Precision-recall analysis may also be informative when evaluating an imbalanced binary outcome because it focuses directly on performance for the positive class. Saito and Rehmsmeier (2015) demonstrated that precision-recall plots can provide more informative assessments than ROC plots when evaluating binary classifiers on strongly imbalanced datasets. Therefore, PR-AUC will be considered alongside ROC-AUC where appropriate.

Calibration represents another important dimension of prediction-model evaluation. Whereas discrimination assesses how well a model distinguishes between individuals with different outcomes, calibration concerns the agreement between predicted probabilities and observed outcomes. A model can discriminate well while still producing poorly calibrated probabilities; consequently, both discrimination and calibration are important when evaluating prediction models (Efthimiou et al., 2024).

The reviewed skilled birth attendance prediction studies did not evaluate calibration consistently. The proposed research will therefore explicitly assess calibration alongside discrimination and class-specific performance rather than relying on accuracy or ROC-AUC alone.

Explainability is also important when applying machine-learning methods to maternal-health research. Several of the reviewed studies used SHAP to identify characteristics contributing to model predictions. Such approaches can help clarify how complex models arrive at their predictions and identify influential variables.

However, predictive importance should not automatically be interpreted as evidence of causality. A characteristic may contribute strongly to prediction without causing non-use of skilled birth attendance. Explainability results in the proposed study will therefore be interpreted as predictive relationships rather than causal effects.


## 3. Problem Statement

Skilled attendance during childbirth remains an important maternal-health challenge in Nigeria. According to the 2024 Nigeria Demographic and Health Survey, only 46% of live births in the two years before the survey were assisted by a skilled provider (National Population Commission [NPC] & ICF, 2025). Substantial geographical and socioeconomic inequalities in childbirth care also remain. Identifying women who may be at greater risk of giving birth without skilled attendance before delivery could therefore provide useful evidence for targeted maternal-health planning and intervention.

Previous Nigeria-specific studies have identified demographic, socioeconomic, healthcare-access and community characteristics associated with skilled birth attendance. Machine-learning studies have also demonstrated the potential to predict skilled birth attendance using DHS data. However, much of the Nigeria-specific evidence reviewed is association-focused, while some prediction studies have included information that would not realistically be available before the childbirth being predicted. Among the prediction studies reviewed, calibration, clustered validation and assessment of performance across population groups have also not been addressed consistently.

Among the studies reviewed, limited evidence was identified of a Nigeria-specific prediction study using the 2023–24 NDHS to predict non-use of skilled birth attendance within a clearly defined pre-delivery framework. The problem is therefore whether information available before childbirth can predict non-skilled attendance in Nigeria with useful discrimination and calibration compared with an interpretable baseline, and whether predictive performance is consistent across geopolitical zones, urban and rural residence, and household wealth groups.

Formally, let **X** represent eligible maternal, household and contextual characteristics available by the defined pre-delivery prediction point, and let **Y** indicate skilled birth attendance for the index birth, where **Y = 1** represents skilled attendance and **Y = 0** represents non-skilled attendance. The study will estimate **P(Y = 0 | X)** and evaluate the resulting predictions using discrimination, calibration and relevant subgroup-performance measures.

---
## 4. Research Questions and Hypotheses

### 4.1 Research Questions

The study will address the following research questions:

**RQ1:** Which maternal, household and contextual characteristics available within the defined pre-delivery framework are associated with non-use of skilled birth attendance in Nigeria?

**RQ2:** How well can prediction models using eligible pre-delivery information predict non-use of skilled birth attendance, in terms of discrimination, class-specific performance and calibration, compared with an interpretable logistic regression baseline?

**RQ3:** Does predictive performance vary across geopolitical zones, urban and rural residence, and household wealth groups?

### 4.2 Hypotheses

The following hypotheses will guide the analysis:

**H1:** Maternal, household and contextual characteristics are significantly associated with non-use of skilled birth attendance in Nigeria. Based on previous Nigerian research, lower maternal education, lower household wealth and rural residence are expected to be associated with greater odds of non-use.

**H2:** Predictive performance will differ between the logistic regression baseline and the evaluated machine-learning models when assessed using discrimination, class-specific performance and calibration.

**H3:** Model performance will vary across geopolitical zones, urban and rural residence, and household wealth groups.

The hypotheses concern statistical associations and predictive performance. They are not intended to establish causal relationships.

---

## 5. Research Objectives

### 5.1 General Objective

To develop and evaluate a late-pregnancy, pre-delivery prediction framework for identifying non-use of skilled birth attendance in Nigeria using the 2023–24 Nigeria Demographic and Health Survey.

### 5.2 Specific Objectives

The specific objectives are to:

1. Define the eligible study population and construct the skilled birth attendance outcome using the 2023–24 NDHS documentation and the skilled-provider definition applicable to the survey.

2. Examine survey-weighted associations between eligible maternal, household and contextual characteristics and non-use of skilled birth attendance.

3. Develop and compare an interpretable logistic regression baseline with appropriate machine-learning models for predicting non-use of skilled birth attendance using information eligible within the defined late-pregnancy, pre-delivery framework.

4. Evaluate model performance using discrimination, class-specific performance and calibration, and assess performance across geopolitical zones, urban and rural residence, and household wealth groups where subgroup sample sizes permit reliable evaluation.

5. Interpret the characteristics contributing to model predictions using appropriate explainability methods, treating identified patterns as predictive relationships rather than evidence of causal effects.

## 6. Methodology

### 6.1 Research Design

This study will use a quantitative, secondary-data research design based on the 2023–24 Nigeria Demographic and Health Survey (NDHS). The analysis will contain three related but distinct components: descriptive and association analysis, predictive modelling, and model interpretation.

The descriptive and association component will characterise the eligible study population and examine survey-weighted relationships between eligible maternal, household and contextual characteristics and non-use of skilled birth attendance. These analyses will describe statistical associations and will not be interpreted as establishing causal effects.

The predictive component will evaluate whether information eligible within the defined late-pregnancy, pre-delivery framework can predict non-use of skilled birth attendance. An interpretable logistic regression model will provide the baseline against which appropriate machine-learning models will be compared.

The model-interpretation component will examine characteristics contributing to model predictions using appropriate explainability methods. Predictor importance and model explanations will be interpreted as predictive relationships rather than evidence that a characteristic causes non-use of skilled birth attendance.

The study is therefore observational and predictive rather than experimental or causal. No intervention will be assigned, and the resulting model will not be presented as a clinical decision tool.

### 6.2 Data Source, Study Population and Sampling

The study will use secondary data from the **2023–24 Nigeria Demographic and Health Survey (NDHS)** obtained through authorised access from The DHS Program. The primary analytical file is expected to be the **Births Recode (BR)**, which contains birth-level records, subject to confirmation during the data audit. Additional recode information will be used only where necessary, appropriate and compatible with the DHS file structure.

The 2023–24 NDHS used a stratified two-stage sampling design. The 36 states and the Federal Capital Territory were stratified by urban and rural residence, producing 74 sampling strata. In the first stage, 1,400 enumeration-area clusters were selected, comprising 701 urban and 699 rural clusters. In the second stage, 30 households were systematically selected from each cluster, producing an intended sample of approximately 42,000 households. Data collection was successfully completed in 1,380 clusters. Twenty selected clusters could not be visited because of deteriorating security conditions during fieldwork, including 10 clusters in Zamfara State (National Population Commission [NPC] & ICF, 2025).

The primary analysis will focus on the **most recent live birth within the two years preceding the survey** for each eligible woman. This reference period aligns the study with the recent-birth skilled-attendance context reported in the 2024 NDHS and ensures that each woman contributes no more than one index delivery to the primary prediction analysis.

For multiple births arising from the same most recent delivery, the handling of the index birth will follow the structure of the NDHS birth records and official recode documentation. The specific rule used to avoid arbitrary duplication of maternal-level information will be documented during the data audit before analysis begins.

Analyses using a broader reference period or alternative birth-record structure may be considered as sensitivity analyses if justified after the data audit.

Draft inclusion criteria are women represented in the relevant NDHS recode data who had at least one live birth during the two-year reference period and whose index birth has sufficient information to determine skilled birth attendance. Records with missing or indeterminate outcome information will not automatically be classified as non-skilled attendance. Final inclusion and exclusion criteria, analytical sample size and missing-data profile will be documented after the data audit.

The exact authorised dataset filename/version and date of download will be recorded from the DHS files during the audit rather than inferred in advance. The data were obtained from **The DHS Program** under its data-access terms for the approved research purpose. Respondent-level DHS microdata will not be redistributed, uploaded to the public project repository or used in attempts to identify respondents.

Survey weights, strata and cluster identifiers will be incorporated where appropriate for population description and association analyses. The clustered survey structure will also be considered when designing the model-validation strategy.

Important data limitations include the cross-sectional survey design, reliance on self-reported and retrospectively recalled information, and the fact that some covariates are measured at interview rather than at the time of the index pregnancy. The 20 selected clusters that were inaccessible because of security conditions were not observed. The survey also necessarily represents eligible women who were alive, available and successfully interviewed; women who died before the survey or were otherwise not interviewed are not represented in the respondent data. These coverage, survivor and measurement limitations will be considered when interpreting the findings.

### 6.3 Outcome Definition

The primary outcome will be **non-use of skilled birth attendance** for the index birth.

The outcome will be constructed from the 2023–24 NDHS questions identifying the person or persons who assisted during delivery. Under the 2024 NDHS reporting definition, a skilled provider includes a **doctor or nurse/midwife** (NPC & ICF, 2025).

The binary outcome will be coded as:

- **Y = 0:** birth not assisted by a skilled provider — the primary class of interest.
- **Y = 1:** birth assisted by a skilled provider.

Thus, although skilled attendance is coded as Y = 1, the prediction target of primary interest is **non-skilled attendance (Y = 0)**.

Where more than one type of attendant is reported, classification will follow the applicable 2023–24 NDHS indicator definition and questionnaire/recode documentation rather than an independently created provider hierarchy.

Responses that are missing, indeterminate or recorded as “don't know,” where applicable, will **not** automatically be classified as non-skilled attendance. Their frequency will first be reported, and affected records will be excluded from the primary outcome analysis unless the official NDHS documentation supports another treatment.

The exact recode variables and coding rules used to construct the outcome will be documented during the data audit and verified against the official NDHS questionnaire and recode documentation before analysis.

### 6.4 Pre-Delivery Prediction Point and Candidate Predictors

The primary prediction framework will use a **late-pregnancy, pre-delivery prediction point**. Conceptually, the model is intended to use information that could reasonably be available before the onset of the index delivery rather than information generated during or after childbirth.

The NDHS does not necessarily provide the exact date at which every candidate characteristic became available during pregnancy. Therefore, “late pregnancy” cannot be treated as a precisely observed gestational cut-off for every predictor. Instead, predictor eligibility will be determined through a documented timing audit based on the meaning and measurement of each NDHS variable.

Each potential predictor will be classified into one of three categories.

**Eligible predictors** will be characteristics that can reasonably represent information known before delivery. Potential domains include maternal demographic characteristics, education, reproductive history available before the index delivery, household socioeconomic context, geographical characteristics, healthcare accessibility, media exposure and ANC information whose timing is compatible with the prediction framework.

**Excluded predictors** will include information arising from the index delivery or afterward. Examples include the actual place of the index delivery, attendant information used to define the outcome, mode of delivery, delivery complications, whether the child was alive at interview, child's age at interview, child's sex, birth weight or reported size at birth, and newborn outcomes. These variables will not be used as predictors in the primary model because they would not be known before the index delivery or could introduce outcome leakage.

**Timing-dependent or borderline predictors** will be assessed individually. ANC variables are particularly important in this category. Measures such as timing of ANC initiation or provider characteristics may contain information available before delivery, whereas a final count of ANC contacts may summarise care accumulated over the pregnancy. Pregnancy wantedness also requires careful interpretation because, although it concerns the period before conception or pregnancy, it is reported retrospectively after the pregnancy outcome. Such variables will be included only when their interpretation and timing are compatible with the intended prediction framework.

Women's decision-making and autonomy variables will also be audited for structural missingness and questionnaire eligibility. Where a variable was asked only of particular groups, such as women currently married or in union, it will not be treated as ordinary missing data. Its suitability for the primary prediction model will be determined according to its population coverage and whether its inclusion would unnecessarily restrict the analytical population.

The primary predictor set will prioritise temporal defensibility and avoidance of leakage. Where justified after the audit, sensitivity analyses may examine how predictive performance changes when selected timing-dependent variables are added. Any such analysis will be clearly distinguished from the primary model.

The final predictor set will not be determined solely by statistical association or feature importance. Variable meaning, measurement timing, missingness, availability, questionnaire eligibility and leakage risk will all be reviewed before inclusion.

Household wealth, residence and some other contextual characteristics present an additional temporal limitation because DHS measures them at interview, which may occur after the index birth. They may still provide useful contextual information but cannot automatically be treated as prospectively measured pregnancy-time characteristics. Their use will therefore be documented explicitly and this temporal limitation will be acknowledged when interpreting the results.

A predictor audit will record each candidate variable, its substantive meaning, measurement timing, proposed role and final classification as eligible, excluded or timing-dependent before model development begins.

### 6.5 Data Preprocessing and Feature Engineering

Data preprocessing will be conducted only after the outcome, analytical population and predictor-timing audit have been finalised. Initial checks will assess variable types, coding consistency, missingness, implausible values and outcome-class distribution.

Categorical variables will be encoded in a form appropriate for each model, while continuous or ordinal variables will be transformed or scaled only where required. Missing-data handling will depend on the amount, pattern and meaning of missingness identified during the audit. Structural missingness will be distinguished from ordinary missing data.

All preprocessing steps that learn information from the data, including imputation, scaling, encoding and any data-driven feature selection, will be fitted using training data only and subsequently applied to validation or test data to prevent information leakage.

Feature engineering will be limited to variables that are substantively interpretable and temporally compatible with the pre-delivery framework.

### 6.6 Candidate Models

Logistic regression will be used as the primary interpretable baseline. It will be compared with a small set of appropriate supervised machine-learning classifiers, expected to include tree-based ensemble methods such as Random Forest and gradient-boosting approaches.

The final model set and hyperparameter search space will be specified before comparative modelling and will reflect the analytical sample size, outcome-class distribution and computational feasibility identified during the data audit. Model selection will be based on validation performance rather than performance on the final test data.

### 6.7 Validation and Experimental Protocol

The data will be separated into model-development and final-evaluation components using a reproducible procedure that prevents the final test data from influencing model fitting, preprocessing, feature selection or hyperparameter tuning.

Because NDHS respondents are sampled within geographical clusters, the validation strategy will account for clustering where feasible rather than assuming that all observations are independent. The final validation approach will be specified after examining the number and distribution of eligible observations across clusters.

Where appropriate, sensitivity analyses will examine whether reasonable alternative predictor or analytical choices materially change model performance.

If a known leakage variable such as place of delivery is deliberately included in an additional comparison model for methodological illustration, that analysis will be clearly labelled as a **leakage-ablation or sensitivity analysis**. It will not be used for primary model development, model selection or substantive conclusions.

### 6.8 Evaluation Metrics

Model performance will be evaluated using complementary measures rather than accuracy alone.

Discrimination will be assessed using ROC-AUC and, where informative for the observed class distribution, precision-recall AUC. Class-specific precision, recall and F1-score will be reported with particular attention to the primary class of interest: non-use of skilled birth attendance.

Calibration will be evaluated using appropriate graphical and numerical measures to assess agreement between predicted probabilities and observed outcomes. Classification thresholds will not be selected using the final test set.

Where feasible, uncertainty around key performance estimates will also be reported using an appropriate resampling or interval-estimation approach that is compatible with the final validation design.

### 6.9 Model Interpretation

The final selected model or models will be interpreted using methods appropriate to the fitted algorithm, such as logistic-regression coefficients, permutation importance or SHAP where justified.

Interpretation will focus on characteristics contributing to prediction. Feature importance, model coefficients and SHAP values will not be described as evidence of causal effects.

### 6.10 Subgroup Performance Assessment

Where subgroup sample sizes and outcome frequencies permit reliable evaluation, predictive performance will be examined across:

- geopolitical zones;
- urban and rural residence; and
- household wealth groups.

Discrimination, calibration and relevant class-specific metrics will be compared across these groups. Subgroup findings will be interpreted cautiously, particularly where sample sizes or outcome frequencies are small.

### 6.11 Ethical Considerations and Approvals

The study will use de-identified secondary data obtained through authorised access from The DHS Program. No attempt will be made to identify individual respondents.

DHS respondent-level microdata will not be redistributed or committed to the public GitHub repository. The data will be used only for the approved research purpose and handled in accordance with applicable DHS data-use requirements.

Any additional institutional, internship-specific or supervisory ethical requirements will be confirmed before analysis begins.

### 6.12 Reproducibility and Code/Data Release

The analytical workflow will be documented in a version-controlled repository. Reproducible code will be provided for data preparation, outcome construction, predictor auditing, modelling, evaluation and generation of reported tables and figures.

Random seeds, software dependencies, data-processing decisions and major modelling decisions will be documented where applicable. The repository may contain code, documentation and non-identifiable derived outputs that comply with DHS requirements, but it will not contain respondent-level DHS microdata.

The exact authorised dataset filename/version and download date will be added to the project documentation after the data audit.

## 7. Significance and Expected Contribution

This study is expected to contribute to maternal-health research in Nigeria by examining whether information available before childbirth can be used to identify women at greater risk of giving birth without skilled attendance. Rather than focusing only on characteristics statistically associated with skilled birth attendance, the study will evaluate their usefulness within a clearly defined prediction framework.

A key contribution is expected to be the development of a **late-pregnancy, pre-delivery prediction framework** that explicitly considers when predictor information becomes available. Candidate variables will be audited for temporal eligibility, and information arising from the index delivery or afterward will be excluded from the primary prediction model. This approach is intended to reduce data leakage (see Section 8 for limitations on predictor timing) and provide a more realistic assessment of predictive performance.

The study will also provide evidence based on the **2023–24 Nigeria Demographic and Health Survey**, allowing the prediction problem to be examined using recent nationally representative Nigerian data. An interpretable logistic regression baseline will be compared with appropriate machine-learning approaches, with performance assessed using discrimination, class-specific measures and calibration rather than accuracy alone.

A further contribution will be the assessment of whether predictive performance is consistent across important population groups. Where sample sizes and outcome frequencies permit reliable evaluation, performance will be examined across geopolitical zones, urban and rural residence, and household wealth groups. This will help determine whether overall model performance conceals weaker performance within particular sections of the population.

Model-interpretation methods will also be used to identify characteristics contributing to model predictions. These findings will be interpreted as predictive relationships rather than causal effects, consistent with the predictive rather than causal objective of the study.

The project will additionally contribute a transparent and reproducible analytical workflow. Code, predictor-audit decisions, data-processing procedures, modelling decisions and evaluation steps will be documented. Respondent-level DHS microdata will not be shared or committed to the public repository, in accordance with applicable DHS data-use requirements.

The findings may be of interest to researchers working on maternal-health prediction, who would gain a documented, leakage-aware workflow for comparison; to analysts and programme planners interested in population-level patterns of risk of non-skilled attendance; and to future research on setting-specific prediction using routine health-facility data. The contribution is primarily methodological and population-level. Some DHS characteristics, such as the household wealth index, are not routinely collected in clinical settings; therefore, translating any resulting model into practice would require further development and external validation using predictors available in the intended operational setting.

Overall, the study is expected to provide methodological and public-health evidence on the feasibility, limitations and performance of predicting non-use of skilled birth attendance before delivery in Nigeria. Its expected contributions include a clearly defined pre-delivery prediction framework, evaluation of discrimination and calibration, assessment of performance across relevant population groups, interpretable prediction results and a reproducible analytical workflow. The resulting framework is intended to support future research and population-level maternal-health planning rather than serve as a clinical diagnostic or individual treatment tool.

## 8. Limitations and Scope

### 8.1 Scope

This study will examine non-use of skilled birth attendance for the most recent live birth within the two years preceding the 2023–24 NDHS among eligible women in Nigeria. It will include survey-weighted association analysis, prediction using information eligible within the defined late-pregnancy, pre-delivery framework, and interpretation of characteristics contributing to model predictions.

The study will not investigate maternal or neonatal mortality, quality of childbirth care, or facility-level and health-system characteristics that are not captured by the NDHS data used in the analysis. It will not estimate causal effects, develop or evaluate a clinical decision tool, or use predictions to label individual women.

### 8.2 Limitations

**Cross-sectional and self-reported data.** The NDHS is cross-sectional, and relevant information is reported retrospectively by respondents. The data may therefore be affected by recall or reporting bias. Statistical associations and predictive importance will not be interpreted as causal effects.

**Predictor timing.** The NDHS does not provide a precise time stamp within pregnancy for every candidate characteristic. Consequently, the late-pregnancy prediction point is an operational framework rather than an exactly observed gestational cut-off. Some characteristics, including household wealth and residence, are measured at the time of interview, which may occur after the index birth. Predictor timing will therefore be audited and documented explicitly.

**Coverage and survivor effects.** Twenty selected clusters, including 10 in Zamfara State, could not be visited because of security conditions. Their absence may affect representation of populations in the affected areas. In addition, the respondent data represent eligible women who were alive, available and successfully interviewed; women who died before the survey or were otherwise not interviewed are not represented.

**Outcome definition.** The 2024 NDHS definition used in this study classifies doctors and nurses/midwives as skilled providers. Skilled-provider definitions may differ across countries, surveys or time periods; therefore, comparisons with other studies will be made cautiously.

**Single survey and lack of external validation.** Model development and internal evaluation will use a single NDHS round. Performance in another time period, dataset or operational setting will therefore remain unknown until external validation is conducted. Subgroup performance estimates may also be imprecise where subgroup sample sizes or outcome frequencies are small; uncertainty will be reported where feasible.

**Limited practical transferability.** Some NDHS predictors, such as the household wealth index, are survey-derived measures that may not be routinely available during antenatal care. The proposed model should therefore be regarded as a population-level research model rather than a ready-to-deploy clinical tool. Practical implementation would require further development and external validation using predictors available in the intended operational setting.

### 8.3 Responsible Interpretation

Predictions will be treated as statistical patterns in population data rather than judgements about individual women. Model coefficients, feature importance and explainability results will be interpreted as predictive relationships and will not be presented as evidence that the identified characteristics cause non-use of skilled birth attendance.

## 9. Implementation Plan and Repository Structure

The research will be implemented as a reproducible, staged data-science workflow. Each stage will build on the previous stage so that decisions concerning the analytical population, outcome, predictor eligibility, preprocessing, modelling and evaluation are documented before the corresponding analysis is performed.

### 9.1 Implementation Plan

The proposed implementation will proceed through the following stages:

1. **Data audit and documentation**  
   Review the authorised 2023–24 NDHS files, questionnaire and recode documentation. Confirm the analytical file, reference period, eligible study population, outcome variables, survey-design variables, missingness and relevant maternal, household and contextual variables.

2. **Outcome and predictor audit**  
   Construct the skilled birth attendance outcome according to the applicable 2024 NDHS definition. Candidate predictors will be reviewed for substantive relevance, questionnaire coverage, measurement timing and potential data leakage. Each candidate variable will be documented as eligible, excluded or timing-dependent.

3. **Data preparation and descriptive analysis**  
   Apply the final eligibility criteria, prepare the analytical dataset and conduct data-quality checks. Survey-weighted descriptive statistics and association analyses will be produced before predictive modelling.

4. **Predictive modelling**  
   Develop an interpretable logistic regression baseline and compare it with the selected machine-learning models. Preprocessing, model fitting and hyperparameter tuning will follow the validation protocol described in Section 6.

5. **Model evaluation and interpretation**  
   Evaluate discrimination, class-specific performance and calibration. Appropriate interpretation methods will be used to examine influential predictive characteristics without making causal claims.

6. **Subgroup and sensitivity analyses**  
   Where sample sizes and outcome frequencies permit, assess predictive performance across geopolitical zones, urban and rural residence, and household wealth groups. Relevant sensitivity analyses will be conducted where justified by the predictor audit and modelling results.

7. **Reporting and reproducibility**  
   Produce final tables, figures and documentation; record modelling and analytical decisions; update the research log; and prepare the research report and presentation materials. Code and permissible derived outputs will be maintained in the repository, while respondent-level DHS microdata will remain outside the public repository.

### 9.2 Repository Structure

The project is organised in a version-controlled GitHub repository that separates restricted data, research documentation, analytical code and permissible outputs. The current repository structure is:

    project-root/
    │
    ├── data/
    │   ├── raw/
    │   ├── interim/
    │   └── processed/
    │
    ├── docs/
    │   ├── data_dictionary/
    │   ├── literature/
    │   ├── methodology/
    │   └── proposal/
    │
    ├── models/
    ├── notebooks/
    ├── reports/
    │   └── figures/
    ├── src/
    ├── tables/
    │
    ├── .gitignore
    ├── CITATION.cff
    ├── README.md
    ├── RESEARCH_LOG.md
    └── requirements.txt

The `docs/` directory contains the main research documentation. The proposal is maintained in `docs/proposal/`, literature-review materials in `docs/literature/`, methodology documentation in `docs/methodology/`, and project data-dictionary materials in `docs/data_dictionary/`.

The `notebooks/` and `src/` directories will contain analytical notebooks and reusable code as the project progresses. Model artefacts will be organised under `models/`, figures under `reports/figures/`, and permissible tabular outputs under `tables/`.

The `data/` directory provides local organisational locations for raw, interim and processed data. Restricted DHS respondent-level data will not be committed to the public repository. The `.gitignore` file will be maintained to prevent restricted or local data files from being uploaded accidentally.

`README.md` provides the project overview, `RESEARCH_LOG.md` records research progress and methodological decisions, `requirements.txt` documents software dependencies, and `CITATION.cff` provides repository citation information.

The structure may be refined as implementation progresses, but substantial changes will be documented to maintain a clear and reproducible analytical trail.


### 9.3 Data Protection and Version Control

The `data/raw/` directory is intended as a local organisational location for authorised DHS respondent-level microdata and other source data that require restricted handling. DHS respondent-level microdata will not be committed to the public GitHub repository. Appropriate `.gitignore` rules will be maintained to prevent restricted DHS files and other local data from being uploaded accidentally.

Version control will be used for code, documentation and permissible analytical outputs. Commits will record meaningful stages of the research so that changes to the analytical workflow and documentation can be traced over time.

The repository may contain reproducible code, documentation, data dictionaries, predictor-audit records, figures, tables and other non-identifiable outputs where permitted. It will not contain respondent-level DHS microdata or other material prohibited by applicable DHS data-use requirements.

The repository will therefore support transparency and reproducibility while protecting restricted survey data.

## 10. Timeline

The research will be completed in phases, with later analytical stages building on decisions established during the data audit and predictor review. The proposed timeline may be adjusted where necessary based on data quality, modelling requirements and mentor feedback.

| Phase | Main Activities | Expected Output |
|---|---|---|
| **Week 1: Research Proposal and Literature Review** | Finalise the research problem, literature review, research gap, research questions, objectives, proposed methodology and references. | Completed first draft of research proposal and documented literature review. |
| **Week 2: Data Audit and Study Population** | Review the authorised 2023–24 NDHS files and documentation; confirm the analytical file, reference period, inclusion and exclusion criteria, outcome construction, survey-design variables, sample size and missingness. | Data-audit report, confirmed analytical population and documented outcome definition. |
| **Week 3: Predictor Audit and Data Preparation** | Review candidate predictors for relevance, timing, questionnaire coverage and leakage risk; classify variables as eligible, excluded or timing-dependent; clean and prepare the analytical data. | Predictor audit, data dictionary and analysis-ready workflow. |
| **Week 4: Descriptive and Association Analysis** | Produce survey-weighted descriptive statistics and examine associations between eligible characteristics and non-use of skilled birth attendance. | Descriptive tables, figures and association-analysis results. |
| **Week 5: Baseline and Machine-Learning Modelling** | Develop the logistic regression baseline and selected machine-learning models; conduct training and hyperparameter tuning using the predefined validation protocol. | Fitted candidate models and documented modelling workflow. |
| **Week 6: Model Evaluation and Interpretation** | Evaluate discrimination, class-specific performance and calibration; compare candidate models and apply appropriate model-interpretation methods. | Model-comparison results, calibration assessment and interpretation outputs. |
| **Week 7: Subgroup and Sensitivity Analyses** | Assess model performance across geopolitical zones, urban/rural residence and household wealth groups where feasible; conduct justified sensitivity analyses. | Subgroup-performance and sensitivity-analysis results. |
| **Week 8: Final Reporting and Reproducibility** | Consolidate findings, limitations and implications; finalise tables and figures; review reproducibility documentation; complete the report and presentation materials. | Final research report, reproducible code and documentation, and presentation materials. |

Progress and methodological decisions will be documented throughout the project in `RESEARCH_LOG.md`. Any changes to the proposed timeline or analytical plan will be recorded with their rationale.

---

## 11. References

Efthimiou, O., Seo, M., Chalkou, K., Debray, T., Egger, M., & Salanti, G. (2024). Developing clinical prediction models: A step-by-step guide. *BMJ, 386*, e078276. https://doi.org/10.1136/bmj-2023-078276

Fagbamigbe, A. F., & Oyedele, O. K. (2022). Multivariate decomposition of trends, inequalities and predictors of skilled birth attendants utilisation in Nigeria (1990–2018): A cross-sectional analysis of change drivers. *BMJ Open, 12*(4), e051791. https://doi.org/10.1136/bmjopen-2021-051791

Federal Ministry of Health and Social Welfare of Nigeria, National Population Commission, & ICF. (2025). *Nigeria Demographic and Health Survey 2024*. Federal Ministry of Health and Social Welfare, National Population Commission, and ICF.

Memon, S. M. Z., Wamala, R., & Kabano, I. H. (2025). Identifying predictors of utilization of skilled birth attendance in Uganda through interpretable machine learning. *International Journal of Environmental Research and Public Health, 22*(11), 1691. https://doi.org/10.3390/ijerph22111691

Miah, M. S. (2026). Explainable machine learning analysis of factors associated with skilled birth attendance in Burkina Faso. *Scientific Reports*. https://doi.org/10.1038/s41598-026-72356-7

Oyedele, O. K., Fagbamigbe, A. F., Akinyemi, O. J., & Adebowale, A. S. (2023). Coverage-level and predictors of maternity continuum of care in Nigeria: Implications for maternal, newborn and child health programming. *BMC Pregnancy and Childbirth, 23*, 36. https://doi.org/10.1186/s12884-023-05372-4

Saito, T., & Rehmsmeier, M. (2015). The precision-recall plot is more informative than the ROC plot when evaluating binary classifiers on imbalanced datasets. *PLOS ONE, 10*(3), e0118432. https://doi.org/10.1371/journal.pone.0118432

Sani, J., Alhur, A. A., & Ahmed, M. M. (2026). Machine learning-based prediction of institutional delivery dropout (IDD) among Nigerian women: An exploratory study using SHAP interpretability. *Journal of Epidemiology and Global Health, 16*, 28. https://doi.org/10.1007/s44197-026-00525-y

Solanke, B. L., & Rahman, S. A. (2018). Multilevel analysis of factors associated with assistance during delivery in rural Nigeria: Implications for reducing rural-urban inequity in skilled care at delivery. *BMC Pregnancy and Childbirth, 18*, 438. https://doi.org/10.1186/s12884-018-2074-9

Taye, E. A., Woubet, E. Y., Hailie, G. Y., Arage, F. G., Zerihun, T. E., Zegeye, A. T., Zeleke, T. C., & Kassaw, A. T. (2025). Application of the random forest algorithm to predict skilled birth attendance and identify determinants among reproductive-age women in 27 Sub-Saharan African countries: Machine learning analysis. *BMC Public Health, 25*, 901. https://doi.org/10.1186/s12889-025-22007-9

Unegbu, U. L. (2026). Determinants of skilled birth attendance in Nigeria: A population-based analysis of the 2018 Demographic and Health Survey [Preprint]. *medRxiv*. https://doi.org/10.64898/2026.04.23.26350432

World Health Organization. (2018). *Definition of skilled health personnel providing care during childbirth: The 2018 joint statement by WHO, UNFPA, UNICEF, ICM, ICN, FIGO and IPA*. World Health Organization.

