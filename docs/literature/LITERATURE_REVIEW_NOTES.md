# Literature Review Notes


## Research Topic

Predicting Non-Use of Skilled Birth Attendance in Nigeria Using Pre-Delivery Information: Evidence from the 2024 Nigeria Demographic and Health Survey

## Purpose

This document records the research papers reviewed for this project.

For each study, I will document what the study investigated, the data and methods used, the main findings, my understanding of the study, and how it relates to my proposed research.

The literature review will help me:

- Understand what research has already been conducted on skilled birth attendance.
- Identify studies that have used machine learning for skilled birth attendance and related maternal-health problems.
- Compare the datasets, predictors, methods, and evaluation approaches used in previous studies.
- Identify whether predictors used in previous studies were available before delivery.
- Understand the strengths and limitations of previous research.
- Develop and support the research gap for this project.

## Literature Review Target

A total of 8–12 key studies will be reviewed, in line with the project Research Guide.

Each study will be reviewed using the following structure:

### Study [Number]: [Author(s), Year]

#### Paper Title
[Title]

#### Country / Study Setting
[Country or countries]

#### Dataset
[Dataset and survey year]

#### Purpose of the Study
[What the researchers wanted to investigate]

#### Methods Used
[Statistical or machine-learning methods]

#### Main Findings
[Main results reported by the researchers]

#### My Understanding
[My explanation of what the study means in simple terms]

#### Relevance to My Research
[How the study relates to my research]

#### Differences From My Research
[What my proposed research will do differently]

#### Limitations / Research Gap Identified
[Important limitations or gaps relevant to my project]

#### Important Variables Used
[Important predictors used in the study]

#### Pre-Delivery Variables Only?
[Yes / No]

If no, document variables that would not reasonably be known before childbirth.

#### Model Evaluation
- Accuracy:
- Precision:
- Recall:
- F1-score:
- ROC-AUC:
- PR-AUC:
- Calibration:
- Cross-validation:
- Other:

#### Verification Checklist
- [ ] Original paper located
- [ ] Abstract reviewed
- [ ] Dataset and sample verified
- [ ] Methods verified
- [ ] Results verified
- [ ] Limitations reviewed
- [ ] Full citation verified

#### Paper Link / DOI
[Link to original publication]

---

## Reviewed Studies

## Study 1: Taye et al. (2025)

### Paper Title

Application of the Random Forest Algorithm to Predict Skilled Birth Attendance and Identify Determinants Among Reproductive-Age Women in 27 Sub-Saharan African Countries: Machine Learning Analysis

### Publication Status

Peer-reviewed research article published in BMC Public Health.

### Source Reviewed

Full text reviewed.

### Country / Study Setting

27 Sub-Saharan African countries, including Nigeria.

### Dataset

The study used Demographic and Health Survey (DHS) data from surveys conducted between 2016 and 2024 across 27 Sub-Saharan African countries.

The analysis included 198,707 reproductive-age women.

The study reported that 71% of the women received assistance from a skilled birth attendant during their last childbirth.

### Purpose of the Study

The study aimed to use machine learning to predict skilled birth attendance among reproductive-age women in 27 Sub-Saharan African countries and identify the factors that contributed most strongly to the predictions.

### Methods Used

The researchers used a Random Forest classifier as the main machine-learning model.

SHAP (SHapley Additive exPlanations) was used to explain the model's predictions and identify influential predictors.

Data preprocessing included:

- K-nearest-neighbour (KNN) imputation with k = 5 for missing values
- SMOTE to address class imbalance
- One-hot encoding for categorical variables
- Min-Max scaling
- Recursive Feature Elimination (RFE) for feature selection

RFE was used to select the top 13 features from the available predictors.

The model generated predictions on a test set, and a probability threshold of 0.5 was used to classify the outcome.

Model performance was evaluated primarily using:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC

### Main Findings

The Random Forest model showed strong reported discrimination.

The reported performance was:

- ROC-AUC: 92%
- Accuracy: 92%
- Precision: 93%
- Recall: 96%
- F1-score: 93% in the abstract and conclusion

SHAP analysis identified important predictors including:

- Facility/place of delivery
- Maternal education
- Household wealth
- Urban/rural residence
- Distance and other barriers to healthcare
- Media exposure
- Internet use

Healthcare-access barriers such as difficulty obtaining permission to visit a health facility, difficulty obtaining money for treatment, and not wanting to attend a health facility alone also influenced the model's predictions.

Note: The article contains an inconsistency in the reported F1-score. The abstract and conclusion report an F1-score of 93%, while the discussion reports 94%. For these literature notes, the 93% value from the abstract and conclusion is retained, while the discrepancy is documented.

### My Understanding

In simple terms, the researchers combined DHS information from women across 27 Sub-Saharan African countries and trained a Random Forest model to recognise patterns associated with skilled birth attendance.

The model performed strongly according to the discrimination measures reported by the researchers.

SHAP was then used to explain which characteristics had the greatest influence on the model's predictions.

The study shows that machine learning can be applied to DHS data to investigate skilled birth attendance and that explainability methods can help show which characteristics are influencing predictions.

However, strong predictive performance alone does not mean that every predictor is suitable for my proposed research.

The most important example is facility/place of delivery. This was one of the strongest predictors in the study, but the actual place where a woman gives birth would not be known before the birth being predicted.

### Relevance to My Research

This study is highly relevant to my research because it examines the same general outcome, skilled birth attendance, and uses DHS data and machine-learning methods.

Nigeria was included among the 27 countries.

The study provides evidence that Random Forest and SHAP can be applied to skilled birth attendance research using DHS data.

It also identifies several characteristics that I may investigate as potential predictors, including:

- Maternal education
- Household wealth
- Residence
- Healthcare-access barriers
- Media exposure
- Internet use

However, these variables will not automatically be included in my model. Their exact definitions and timing will first be checked against the 2023–24 NDHS documentation.

### Differences From My Research

The study pooled data from 27 Sub-Saharan African countries rather than developing a Nigeria-specific model.

My proposed research will focus specifically on Nigeria using the 2023–24 Nigeria DHS.

A major difference is predictor timing.

The Taye et al. model included facility/place of delivery, which was one of its most influential predictors.

For my proposed research, I intend to restrict the main prediction model to information that could reasonably have been known before the delivery being predicted.

Therefore, the actual place of delivery will not be used as a predictor of skilled birth attendance for that same delivery.

My research also intends to assess calibration and model performance across important geographical and socioeconomic groups, in addition to discrimination and explainability.

### Limitations / Research Gap Identified

The authors reported several limitations, including:

- DHS information is partly self-reported and may be affected by reporting or recall bias.
- The cross-sectional nature of the data limits causal interpretation.
- Survey years differed across the 27 countries.
- Some local or contextual factors may not have been available in the DHS data.

For my proposed research, additional methodological issues are important.

First, the study pooled 27 countries. Therefore, its model does not provide a Nigeria-specific prediction model based solely on the latest Nigeria DHS.

Second, facility/place of delivery was used as a predictor even though this information would not be available before the same childbirth. This makes it unsuitable for my intended pre-delivery prediction setting and raises an important predictor-timing/data-leakage concern for my project.

Third, the reported model evaluation focused on discrimination and classification metrics such as ROC-AUC, accuracy, precision, recall and F1-score.

A probability-calibration assessment was not reported in the full article.

This is relevant to my research because if a model is intended to estimate a woman's probability of non-use of skilled birth attendance, I want to examine not only whether the model separates higher-risk from lower-risk women but also whether its predicted probabilities correspond reasonably to observed outcomes.

### Important Variables / Factors Identified

Important predictors identified by the model included:

- Facility/place of delivery
- Maternal education
- Household wealth
- Urban/rural residence
- Distance to healthcare facilities
- Healthcare-access barriers
- Media exposure
- Internet use

### Pre-Delivery Variables Only?

No.

The model included facility/place of delivery.

This is not a valid pre-delivery predictor for the same birth because the actual delivery location is known at or after the time of delivery.

Several other important predictors could potentially be available before childbirth, including:

- Maternal education
- Household wealth
- Residence
- Healthcare-access barriers
- Media exposure
- Internet use

However, the exact DHS variable definitions and timing will need to be checked before inclusion in my proposed model.

### Model Evaluation

- Main model: Random Forest
- Explainability: SHAP
- Missing-data handling: KNN imputation
- Class-imbalance handling: SMOTE
- Feature selection: Recursive Feature Elimination
- Selected features: Top 13 predictors
- Accuracy: 92%
- Precision: 93%
- Recall: 96%
- F1-score: 93% in the abstract and conclusion; 94% reported in the discussion
- ROC-AUC: 92%
- PR-AUC: Not reported
- Calibration: Not reported
- Probability threshold: 0.5
- Subgroup performance evaluation: Not reported as a main model-evaluation component

### Verification Checklist

- [x] Original paper located
- [x] Full text reviewed
- [x] Authors verified
- [x] Publication details verified
- [x] Countries and DHS survey period verified
- [x] Sample size verified
- [x] Outcome verified
- [x] Data-preprocessing methods verified
- [x] Machine-learning method verified
- [x] Model-evaluation metrics verified
- [x] Main results verified
- [x] SHAP predictors verified
- [x] Calibration reporting checked
- [x] Limitations reviewed
- [x] Full citation verified

### Full Citation

Taye, E. A., Woubet, E. Y., Hailie, G. Y., Arage, F. G., Zerihun, T. E., Zegeye, A. T., Zeleke, T. C., & Kassaw, A. T. (2025). Application of the random forest algorithm to predict skilled birth attendance and identify determinants among reproductive-age women in 27 Sub-Saharan African countries: Machine learning analysis. BMC Public Health, 25, 901.

### DOI / Original Publication

https://doi.org/10.1186/s12889-025-22007-9
---

## Study 2: Memon et al. (2025)

### Paper Title

Identifying Predictors of Utilization of Skilled Birth Attendance in Uganda Through Interpretable Machine Learning

### Publication Status

Peer-reviewed research article published in the International Journal of Environmental Research and Public Health.

### Source Reviewed

Full text reviewed.

### Country / Study Setting

Uganda.

### Dataset

The study used data from the 2016 Uganda Demographic and Health Survey (UDHS).

The analysis included 9,611 women aged 15–49 years who had given birth during the five years preceding the survey.

A total of 40 features were initially used in the analysis.

The outcome was skilled birth attendant use during the woman's most recent delivery.

Overall:

- 74.73% of the women used skilled birth attendance.
- 25.27% did not use skilled birth attendance.

### Purpose of the Study

The study aimed to develop interpretable machine-learning models to predict skilled birth attendance among women in Uganda.

The researchers also wanted to identify the sociodemographic, economic, healthcare-access and obstetric characteristics that were most influential in predicting skilled birth attendance.

### Methods Used

The researchers compared seven supervised learning models:

- Logistic Regression
- Decision Tree
- Random Forest
- Gradient Boosting
- XGBoost
- LightGBM
- CatBoost

The data were split into:

- 80% training data
- 20% testing data

Hyperparameters were optimized using Bayesian optimization with 5-fold cross-validation on the training data.

Class imbalance was handled using cost-sensitive learning/class weighting, giving greater importance to women who did not use skilled birth attendance.

Missing data were handled using K-nearest-neighbour (KNN) imputation.

Nine of the 40 features had missing data, ranging from approximately 0.03% to 2.8%.

Health insurance was removed because almost all women were in the same category, making it a near-zero variance feature.

The researchers examined multicollinearity and used Elastic Net as part of the feature-selection process.

SHAP (SHapley Additive Explanations) was used to interpret predictions from the best-performing model and identify influential predictors.

The explanatory variables were organised using Andersen's Healthcare Utilization Model into:

- Predisposing factors
- Enabling factors
- Need factors

### Main Findings

XGBoost was selected as the best-performing model overall.

Its test-set performance was:

- Precision: 0.40
- Recall: 0.73
- F1-score: 0.52
- Accuracy: 0.66
- ROC-AUC: 0.7473

The researchers placed particular emphasis on identifying women who did not use skilled birth attendance.

The reported precision, recall and F1-score therefore focused on the minority class of women without SBA.

Other models performed relatively similarly.

Their reported ROC-AUC values were:

- Logistic Regression: 0.7364
- Random Forest: 0.7413
- Gradient Boosting: 0.7442
- XGBoost: 0.7473
- LightGBM: 0.7424
- Decision Tree: 0.7121
- CatBoost: 0.7464

SHAP analysis identified the most influential predictors of skilled birth attendance as including:

- Maternal education
- Number of antenatal care visits
- Urban/rural residence
- Region
- Perceived distance to a healthcare facility

Other characteristics, including partner's education and some household/media-related factors, also contributed to predictions.

### My Understanding

In simple terms, the researchers used information from Ugandan women in the 2016 DHS to train several machine-learning models to identify women who were more or less likely to use skilled birth attendance.

They compared seven different models instead of relying on only one.

XGBoost performed best overall, although its performance was moderate rather than extremely high.

Its ROC-AUC of about 0.75 means that the model had some ability to distinguish women who used skilled birth attendance from those who did not, but the prediction problem was still challenging.

The researchers were particularly interested in correctly identifying women who did not receive skilled birth attendance because this was the smaller and more important public-health group.

They therefore used class weighting to make the models pay more attention to women without SBA.

SHAP was then used to explain why the XGBoost model made its predictions.

Education, ANC attendance, residence, region and distance to healthcare were among the most influential characteristics.

### Relevance to My Research

This study is highly relevant to my research because it uses DHS data, machine learning and explainability to investigate skilled birth attendance.

It is particularly useful because its modelling objective focused on identifying women who did not use skilled birth attendance.

That is closely related to my proposed outcome of predicting non-use of skilled birth attendance.

The study also demonstrates the value of comparing several machine-learning models rather than selecting one algorithm in advance.

Its use of SHAP is relevant to my plan to make model predictions interpretable.

Several important predictors identified in the study could potentially be available before childbirth, including:

- Maternal education
- ANC attendance
- Residence
- Region
- Perceived distance to healthcare
- Partner's education

These variables provide useful evidence for characteristics I should investigate when reviewing the 2023–24 NDHS.

### Differences From My Research

The study focused on Uganda using the 2016 UDHS.

My proposed research will focus specifically on Nigeria using the 2023–24 NDHS.

The study predicted skilled birth attendance using a broad set of DHS variables.

My research will apply a stricter predictor-timing rule by including only information that could reasonably have been available before the delivery being predicted.

My research also intends to assess probability calibration and model performance across important geographical and socioeconomic groups.

These were not reported as main evaluation components in this study.

### Predictor-Timing Considerations

This study is useful for my pre-delivery research because many of its strongest predictors could potentially be known before childbirth.

Examples include:

- Education
- Residence
- Region
- Perceived distance to healthcare
- Partner's education

Antenatal care information also occurs before childbirth, but its suitability depends on the exact prediction point.

For example, the total number of ANC visits cannot be known early in pregnancy.

If my prediction point is defined later in pregnancy but before delivery, ANC utilisation up to that point could potentially be appropriate.

Therefore, I will not automatically copy the ANC variables used in this study.

Their timing will be assessed against the prediction point chosen for my research.

### Validation and Survey-Design Considerations

The researchers used an 80/20 train-test split.

Bayesian hyperparameter optimization with 5-fold cross-validation was performed using the training data.

The article describes the 2016 UDHS as using a two-stage stratified sampling design.

However, the machine-learning methods section does not describe a cluster-aware train-test split in which DHS sampling clusters were kept together when dividing observations between training and testing sets.

The article also does not clearly describe incorporating DHS survey weights into machine-learning model fitting or performance evaluation.

Therefore, I should not state that cluster-aware validation or survey weighting was performed unless additional information from the authors confirms it.

This is relevant to my proposed research because women sampled from the same DHS cluster may share geographical and community characteristics.

I will therefore need to consider carefully how DHS survey design and clustering should be handled in my own modelling and validation strategy.

### Limitations / Research Gap Identified

The study used cross-sectional DHS data, so its results should not be interpreted as establishing causal relationships.

It focused on Uganda rather than Nigeria.

The Uganda DHS data were from 2016, whereas my proposed study will use the newer 2023–24 Nigeria DHS.

Although the study used a held-out test set and cross-validation for hyperparameter optimization, cluster-aware validation was not described.

Survey-weighted machine-learning model fitting or evaluation was also not clearly described.

The reported evaluation focused mainly on discrimination and classification measures such as ROC-AUC, accuracy, precision, recall and F1-score.

A probability-calibration analysis was not reported in the full article.

Subgroup-specific predictive performance across important socioeconomic or geographical groups was also not reported as a main evaluation component.

These issues are relevant to my proposed research because I intend to evaluate not only discrimination but also calibration and whether predictive performance differs across important Nigerian groups.

### Important Variables / Factors Identified

Important predictors identified through SHAP included:

- Maternal education
- Number of ANC visits
- Urban/rural residence
- Region
- Perceived distance to healthcare facility
- Partner's education
- Household and media-related characteristics

### Pre-Delivery Variables Only?

The study was not specifically designed around a strict pre-delivery prediction point.

However, many of its influential variables could potentially be known before childbirth.

These include:

- Maternal education
- Residence
- Region
- Distance to healthcare
- Partner's education

ANC information may also be appropriate depending on when the prediction is intended to occur.

Therefore, each candidate predictor will need to be checked against its exact DHS definition and timing before being included in my proposed model.

### Model Evaluation

- Sample size: 9,611 women
- Initial features: 40
- Models compared: 7
- Train/test split: 80/20
- Hyperparameter tuning: Bayesian optimization
- Cross-validation: 5-fold cross-validation during hyperparameter tuning
- Class-imbalance handling: Cost-sensitive learning/class weighting
- Missing-data handling: KNN imputation
- Feature selection: Elastic Net
- Explainability: SHAP
- Best-performing model: XGBoost
- Precision: 0.40
- Recall: 0.73
- F1-score: 0.52
- Accuracy: 0.66
- ROC-AUC: 0.7473
- PR-AUC: Not reported
- Calibration: Not reported
- Cluster-aware train/test splitting: Not described
- Survey-weighted ML fitting/evaluation: Not clearly described
- Subgroup performance evaluation: Not reported as a main model-evaluation component

### Verification Checklist

- [x] Original paper located
- [x] Full text reviewed
- [x] Authors verified
- [x] Publication details verified
- [x] Dataset and survey year verified
- [x] Sample size verified
- [x] Number of features verified
- [x] Outcome definition verified
- [x] Models compared verified
- [x] Train/test split verified
- [x] Cross-validation approach verified
- [x] Class-imbalance method verified
- [x] Missing-data method verified
- [x] Feature-selection method verified
- [x] Performance metrics verified
- [x] SHAP predictors verified
- [x] Calibration reporting checked
- [x] Survey-design reporting checked
- [x] Limitations reviewed
- [x] Full citation verified

### Full Citation

Memon, S. M. Z., Wamala, R., & Kabano, I. H. (2025). Identifying predictors of utilization of skilled birth attendance in Uganda through interpretable machine learning. International Journal of Environmental Research and Public Health, 22(11), 1691.

### DOI / Original Publication

https://doi.org/10.3390/ijerph22111691
---

## Study 3: Miah (2026)

### Paper Title

Explainable Machine Learning Analysis of Factors Associated with Skilled Birth Attendance in Burkina Faso

### Publication Status

Peer-reviewed research article published in Scientific Reports.

### Source Reviewed

Full text reviewed.

### Country / Study Setting

Burkina Faso.

### Dataset

The study used data from the 2021 Burkina Faso Demographic and Health Survey (BF-DHS).

The analysis included 5,111 women aged 15–49 years.

The study used nationally representative DHS data to investigate skilled birth attendance.

### Purpose of the Study

The study aimed to use explainable machine learning to:

- Predict skilled birth attendance.
- Identify important predictors of skilled birth attendance.
- Examine geographical differences in skilled birth attendance.
- Examine urban-rural inequalities in predicted skilled birth attendance.

The study therefore combined machine-learning prediction, explainability and geographical analysis.

### Methods Used

The researcher compared five machine-learning models:

- Random Forest (RF)
- Decision Tree (DT)
- K-Nearest Neighbours (KNN)
- Logistic Regression (LR)
- Support Vector Machine (SVM)

Boruta feature selection was used to identify relevant predictors.

SMOTE was used to address class imbalance.

Model performance was evaluated using several measures, including:

- Accuracy
- Precision
- Recall
- F1-score
- Matthews Correlation Coefficient (MCC)
- Cohen's kappa
- Area Under the Receiver Operating Characteristic Curve (AUROC)

SHAP (SHapley Additive exPlanations) was used to interpret the model's predictions and identify influential predictors.

Decision Curve Analysis (DCA) was also used to assess the potential usefulness of the model across different decision thresholds.

Spatial mapping was used to examine geographical patterns and inequalities in predicted skilled birth attendance across Burkina Faso.

### Main Findings

Random Forest was the best-performing model among the five machine-learning models.

The Random Forest model achieved:

- AUROC: 0.71

The researcher described this as moderate discrimination.

Important predictors identified included:

- Province
- Four or more antenatal care visits
- Maternal age at first birth of 20 years or older
- Age at first sexual intercourse of 18 years or older
- Sexual activity
- Household wealth
- Religion

SHAP analysis was used to show how these characteristics influenced the model's predictions.

The spatial analysis also identified geographical inequalities.

Higher predicted probabilities of skilled birth attendance were observed in some central and western provinces, while lower predicted probabilities were observed in areas including:

- Sahel
- Sud-Ouest
- Est

The study also reported greater inequalities in rural areas.

### My Understanding

In simple terms, the researcher used information about women from the 2021 Burkina Faso DHS to train several machine-learning models to recognise patterns associated with skilled birth attendance.

Five different models were compared.

Random Forest performed best, but its AUROC of 0.71 shows that its ability to separate women who received skilled birth attendance from those who did not was moderate rather than extremely strong.

The researcher then used SHAP to understand which characteristics influenced the Random Forest predictions.

The study also went beyond reporting one national prediction result by mapping predicted skilled birth attendance across different geographical areas.

This showed that skilled birth attendance was not evenly distributed across Burkina Faso.

This paper helped me understand that machine learning can be combined with explainability and geographical analysis to investigate both prediction and inequalities in maternal healthcare.

### Relevance to My Research

This study is highly relevant to my research because it uses DHS data, machine learning and SHAP to investigate skilled birth attendance.

It demonstrates the usefulness of comparing several machine-learning models rather than relying on a single algorithm.

The study is also particularly relevant because it examined geographical and urban-rural inequalities.

This supports my interest in investigating whether patterns or predictive performance differ across geographical and socioeconomic groups in Nigeria.

Several predictors identified in the study could potentially provide information before childbirth, including:

- Province or geographical location
- Household wealth
- Religion
- Maternal age at first birth
- Previous reproductive history

Antenatal care is also potentially available before childbirth, although its suitability depends on the exact prediction point.

### Differences From My Research

The study focused on Burkina Faso using the 2021 Burkina Faso DHS.

My proposed research will focus specifically on Nigeria using the 2023–24 Nigeria DHS.

The Burkina Faso study used several machine-learning models, SHAP and spatial analysis.

My research will also focus specifically on the timing of predictors.

The main prediction model will be restricted to information that could reasonably have been available before the delivery being predicted.

I also intend to assess probability calibration in addition to discrimination.

Another difference is that my proposed study intends to investigate model performance across important Nigerian geographical and socioeconomic groups, rather than only describing geographical differences in predicted probabilities.

Therefore, geographical mapping and subgroup predictive performance should not be treated as the same thing.

### Predictor-Timing Considerations

This study was not specifically designed around a strict pre-delivery prediction point.

Some of its important predictors could potentially be known before childbirth.

These include:

- Geographical location
- Household wealth
- Religion
- Maternal age at first birth
- Previous reproductive history

However, antenatal care requires careful consideration.

The study identified four or more ANC visits as an important predictor.

The final total number of ANC visits cannot be known early in pregnancy.

Therefore, whether ANC visit count is an appropriate predictor in my research depends on when the prediction is intended to be made.

If prediction occurs late in pregnancy before delivery, ANC information accumulated up to that point may potentially be appropriate.

If prediction is intended earlier in pregnancy, later ANC visits would not yet be available.

This reinforces the need to define my prediction point before selecting the final predictors.

### Validation and Evaluation Considerations

The study evaluated several aspects of model performance.

Discrimination and classification performance were assessed using:

- Accuracy
- Precision
- Recall
- F1-score
- MCC
- Cohen's kappa
- AUROC

The study also used Decision Curve Analysis to examine potential clinical or decision usefulness across different thresholds.

SHAP was used for model explainability.

Spatial mapping was used to examine geographical variation.

However, probability calibration was not reported as a model-evaluation component.

This distinction is important.

Decision Curve Analysis and calibration do not measure the same thing.

Decision Curve Analysis evaluates whether using a prediction model at different thresholds may provide useful decision value.

Calibration evaluates whether predicted probabilities correspond appropriately to observed outcome frequencies.

Therefore, the presence of Decision Curve Analysis does not mean that model calibration was assessed.

### Limitations / Research Gap Identified

The study used cross-sectional DHS data, so the findings should not automatically be interpreted as causal relationships.

The study focused on Burkina Faso rather than Nigeria.

It used the 2021 Burkina Faso DHS, whereas my proposed study will use the newer 2023–24 Nigeria DHS.

Although the study incorporated machine-learning comparison, SHAP, Decision Curve Analysis and geographical analysis, probability calibration was not reported as part of model evaluation.

The study examined geographical inequalities in predicted skilled birth attendance, but this is different from evaluating whether the prediction model performs equally well across geographical or socioeconomic subgroups.

For example, a map may show that predicted SBA probabilities are lower in one region than another without telling us whether the model is equally accurate or equally well calibrated in both regions.

This distinction is relevant to my proposed research because I intend to examine predictive performance across important Nigerian groups.

### Important Variables / Factors Identified

Important predictors included:

- Province
- Four or more ANC visits
- Maternal age at first birth of 20 years or older
- Age at first sexual intercourse of 18 years or older
- Sexual activity
- Household wealth
- Religion

### Pre-Delivery Variables Only?

The study was not specifically designed to use only pre-delivery predictors.

Several important characteristics could potentially be available before childbirth, including:

- Province
- Household wealth
- Religion
- Maternal reproductive history

Other variables require more careful timing assessment.

In particular, total ANC visits depend on the stage of pregnancy at which prediction is intended to occur.

Therefore, I will verify the exact definition and timing of each candidate variable before including it in my proposed prediction model.

### Model Evaluation

- Sample size: 5,111 women
- Dataset: 2021 Burkina Faso DHS
- Models compared: 5
- Models: Random Forest, Decision Tree, KNN, Logistic Regression and SVM
- Feature selection: Boruta
- Class-imbalance handling: SMOTE
- Best-performing model: Random Forest
- AUROC: 0.71
- Accuracy: Evaluated
- Precision: Evaluated
- Recall: Evaluated
- F1-score: Evaluated
- Matthews Correlation Coefficient: Evaluated
- Cohen's kappa: Evaluated
- Explainability: SHAP
- Decision Curve Analysis: Yes
- Spatial analysis: Yes
- Urban-rural inequality analysis: Yes
- Calibration: Not reported as a model-evaluation component
- Subgroup predictive performance evaluation: Not reported as a main evaluation component

### Verification Checklist

- [x] Original paper located
- [x] Full text reviewed
- [x] DOI verified
- [x] Author verified
- [x] Publication details verified
- [x] Country verified
- [x] DHS survey year verified
- [x] Sample size verified
- [x] Models compared verified
- [x] Feature-selection method verified
- [x] Class-imbalance method verified
- [x] Model-evaluation measures verified
- [x] Best-performing model verified
- [x] AUROC verified
- [x] SHAP analysis verified
- [x] Decision Curve Analysis verified
- [x] Spatial analysis verified
- [x] Calibration reporting checked
- [x] Main predictors verified
- [x] Full citation verified

### Full Citation

Miah, M. S. (2026). Explainable machine learning analysis of factors associated with skilled birth attendance in Burkina Faso. Scientific Reports.

### DOI / Original Publication

https://doi.org/10.1038/s41598-026-72356-7
---

## Study 4: Sani et al. (2026)

### Paper Title

Machine Learning-Based Prediction of Institutional Delivery Dropout (IDD) Among Nigerian Women: An Exploratory Study Using SHAP Interpretability

### Publication Status

Peer-reviewed research article published in the Journal of Epidemiology and Global Health.

### Source Reviewed

Full text reviewed.

### Country / Study Setting

Nigeria.

The study used nationally representative data covering all six geopolitical zones of Nigeria.

### Dataset

The study used data from the 2018 Nigeria Demographic and Health Survey (NDHS).

The researchers used the Individual Recode (IR) file.

The study population consisted of women aged 15–49 years who:

- Had experienced a live birth within the five years preceding the survey.
- Had attended at least one antenatal care visit during that pregnancy.
- Had information available on place of delivery.

The analysis was restricted to one observation per woman, corresponding to her most recent live birth.

The article's abstract and Results section report a sample of 16,100 women.

However, the Methods section reports that after exclusions, the final unweighted analytic sample was 16,000 women.

This inconsistency in the reported sample size is documented in these literature notes rather than resolved without further information from the authors.

### Outcome

The outcome was institutional delivery dropout (IDD).

IDD was defined as:

Delivery outside a recognised health facility despite having attended at least one antenatal care visit.

The outcome was coded as:

- 1 = Institutional delivery dropout
- 0 = Institutional delivery

This outcome is related to my research but is not the same as skilled birth attendance.

My research focuses on whether a skilled provider attended the delivery, whereas this study focuses on whether the delivery occurred inside or outside a health facility after ANC attendance.

### Purpose of the Study

The study aimed to use machine learning to predict institutional delivery dropout among Nigerian women who had already accessed antenatal care.

The researchers also aimed to identify the sociodemographic characteristics that contributed most strongly to the predictions.

The study therefore focused specifically on the discontinuity between:

ANC attendance → place of delivery.

### Methods Used

The researchers compared seven supervised machine-learning models:

- Logistic Regression
- Support Vector Machine
- K-Nearest Neighbours
- Decision Tree
- Random Forest
- Gradient Boosting
- XGBoost

Ten sociodemographic predictors were retained for the final machine-learning models.

Feature selection involved:

- Cramér's V for assessing relationships/multicollinearity among categorical predictors.
- Recursive Feature Elimination (RFE) using a Random Forest estimator.

The dataset was divided into:

- 80% training data
- 20% test data

The split was stratified by the institutional delivery dropout outcome.

Stratified 5-fold cross-validation was used during model training.

The models were intentionally fitted using default hyperparameters rather than systematic hyperparameter optimisation because the study was designed as an exploratory baseline comparison.

Stratified bootstrapping with 1,000 resamples was used to calculate 95% confidence intervals for test-set performance.

SHAP was used to explain feature contributions.

Although Gradient Boosting had the strongest overall predictive performance, SHAP values were calculated using the Random Forest model because the researchers considered it suitable for feature-level interpretation.

### Survey Design and Weighting

The 2018 NDHS used a multistage stratified cluster sampling design.

The researchers used DHS sampling weights for descriptive and bivariate epidemiological analyses.

However, the machine-learning models themselves were intentionally not survey-weighted.

The authors explained that the ML objective was predictive performance rather than producing nationally representative population estimates.

The reported train-test split was stratified by the outcome variable.

A cluster-aware split that kept women from the same DHS sampling cluster together was not described.

### Main Findings

Institutional delivery dropout was common among the study population.

The Results section reports that approximately 48% of women delivered outside a health facility despite having attended at least one ANC visit.

Gradient Boosting showed the strongest overall discrimination.

Reported Gradient Boosting performance included approximately:

- Accuracy: 0.737
- Precision: 0.740
- F1-score: 0.755
- AUROC: approximately 0.82

The article contains some internal variation in the reported Gradient Boosting recall. The Results section reports approximately 0.740 in one location, while the Discussion reports approximately 0.769.

Support Vector Machine achieved:

- Accuracy: 0.740
- Recall: 0.780
- F1-score: 0.759

XGBoost also performed strongly, with:

- Precision: 0.741
- Accuracy: 0.727
- F1-score: 0.739
- AUROC: approximately 0.80

Logistic Regression achieved an AUROC of approximately 0.794.

Decision Tree had the lowest discrimination, with an AUROC of approximately 0.716.

### Calibration

Unlike several of the other machine-learning studies in my literature review, this study explicitly assessed probability calibration.

Calibration curves were presented for:

- Gradient Boosting
- Support Vector Machine
- XGBoost

The researchers reported that Gradient Boosting showed the closest agreement between predicted probabilities and observed outcomes.

XGBoost also showed relatively good calibration, while SVM showed somewhat greater underestimation at lower predicted probabilities.

The Methods section also states that Brier scores were used as part of calibration assessment.

This is particularly relevant to my proposed research because it shows that calibration has already been considered in recent Nigeria-specific maternal-health machine-learning research.

Therefore, I should not claim that calibration has never been evaluated in related Nigerian ML research.

### SHAP / Important Predictors

SHAP identified education as the strongest predictor of institutional delivery dropout.

Other influential characteristics included:

- Household wealth
- Religion
- Urban/rural residence
- Maternal age group
- Geopolitical region

The study found that women with higher education and greater household wealth generally had lower predicted dropout risk.

Geographical and urban-rural differences also contributed to model predictions.

### My Understanding

In simple terms, this study looked at Nigerian women who had already attended antenatal care and asked:

"Which women still went on to deliver outside a health facility?"

The researchers used seven different machine-learning models to predict this dropout between ANC attendance and institutional delivery.

Gradient Boosting performed best overall according to discrimination, while SVM had the highest recall.

SHAP was used to understand which characteristics were driving the predictions.

Education, wealth, religion, residence, age and geographical region were important.

This study is particularly important to my research because it demonstrates that machine learning and explainability have already been applied to a closely related maternal-health problem using Nigeria DHS data.

It also assessed calibration, which means my research gap cannot simply be that previous Nigeria-specific machine-learning studies did not examine calibration.

### Relevance to My Research

This study is highly relevant because it is:

- Nigeria-specific.
- Based on NDHS data.
- A maternal-health service-utilisation prediction study.
- Machine-learning based.
- Interpreted using SHAP.
- Evaluated using both discrimination and calibration.

It also uses characteristics that may be relevant to my own pre-delivery prediction model, including:

- Education
- Wealth
- Religion
- Residence
- Age
- Geopolitical region
- Healthcare-access difficulty

The study also provides an important methodological comparison for my project because it used an 80/20 split, stratified 5-fold cross-validation, bootstrapped confidence intervals, SHAP and calibration analysis.

### Differences From My Research

The most important difference is the outcome.

This study predicts:

Institutional delivery dropout.

This means delivery outside a health facility after ANC attendance.

My proposed study predicts:

Non-use of skilled birth attendance.

This means whether the delivery was attended by an appropriately skilled provider.

Facility delivery and skilled birth attendance are related, but they are not identical outcomes.

A woman could potentially deliver outside a conventional facility and still receive assistance from a skilled provider, or deliver within a facility under circumstances that require careful interpretation of the provider variable.

Another major difference is the study population.

The Sani et al. study included only women who had attended at least one ANC visit.

My proposed research is not currently restricted only to women who attended ANC.

The study also used the 2018 NDHS, whereas my research will use the newer 2023–24 NDHS.

### Predictor-Timing Considerations

This study is particularly useful for my pre-delivery approach because its predictors were mainly sociodemographic and contextual characteristics rather than information known only after childbirth.

Examples include:

- Maternal age
- Education
- Household wealth
- Employment
- Marital status
- Religion
- Healthcare-access difficulty
- Residence
- Geopolitical region

These characteristics could generally be known before childbirth.

The study also excluded delivery complications because of missingness and reporting issues.

However, my own predictor selection will still require checking the exact definition and timing of every 2023–24 NDHS variable.

### Validation and Survey-Design Considerations

The study used:

- An 80/20 stratified train-test split.
- Stratified 5-fold cross-validation.
- 1,000 bootstrap resamples for uncertainty estimates.

However, no external temporal or regional validation was performed.

The authors themselves identified the absence of external validation as a limitation.

The split was stratified by the outcome, but a DHS cluster-aware train-test split was not described.

Descriptive analyses used DHS sampling weights, while the machine-learning models intentionally did not use survey weights.

This is relevant to my research because I will need to decide whether standard random splitting is appropriate when women are nested within DHS geographical clusters.

### Limitations / Research Gap Identified

The study used cross-sectional 2018 NDHS data.

It therefore does not use the newer 2023–24 NDHS.

Its outcome was institutional delivery dropout rather than skilled birth attendance.

The analysis was also restricted to women who had already attended ANC.

The models used default hyperparameters rather than systematic hyperparameter optimisation.

No external validation using temporal or geographical partitions was performed.

Although the train-test split was stratified by the outcome, cluster-aware validation was not described.

The machine-learning models were intentionally not survey-weighted.

The study assessed calibration, so lack of calibration cannot be claimed as a universal gap across Nigeria-specific maternal-health machine-learning research.

However, the study did not develop a national prediction model specifically for non-use of skilled birth attendance using the 2023–24 NDHS and a clearly defined set of pre-delivery predictors.

### Important Variables / Factors Identified

Important predictors included:

- Maternal education
- Household wealth
- Religion
- Urban/rural residence
- Maternal age
- Geopolitical region
- Employment
- Marital status
- Perceived difficulty accessing healthcare

### Pre-Delivery Variables Only?

The predictors used in the final machine-learning models were primarily sociodemographic and contextual variables that could generally be available before delivery.

This makes the study particularly relevant to my proposed pre-delivery prediction framework.

However, the outcome itself was based on what happened at delivery, specifically whether the woman delivered in a health facility after attending ANC.

My research will still independently verify the timing and definition of every candidate predictor in the 2023–24 NDHS.

### Model Evaluation

- Dataset: 2018 Nigeria DHS
- DHS file: Individual Recode (IR)
- Reported sample: 16,100 in abstract/results; 16,000 in Methods
- Outcome: Institutional delivery dropout
- Models compared: 7
- Models: Logistic Regression, SVM, KNN, Decision Tree, Random Forest, Gradient Boosting and XGBoost
- Final predictors: 10
- Feature selection: Cramér's V + Recursive Feature Elimination
- Train/test split: 80/20
- Split stratified by outcome: Yes
- Cross-validation: Stratified 5-fold
- Hyperparameter optimisation: No; default hyperparameters used
- Bootstrap uncertainty estimation: 1,000 resamples
- Best overall model: Gradient Boosting
- Gradient Boosting AUROC: approximately 0.82
- Gradient Boosting F1-score: 0.755
- SVM accuracy: 0.740
- SVM recall: 0.780
- XGBoost AUROC: approximately 0.80
- Explainability: SHAP
- Calibration curves: Yes
- Brier score assessment: Stated in Methods
- Survey weights in descriptive analysis: Yes
- Survey weights in ML fitting: No
- Cluster-aware train/test split: Not described
- External validation: No
- Regional/temporal external validation: No

### Verification Checklist

- [x] Original paper located
- [x] Full text reviewed
- [x] Authors verified
- [x] Publication details verified
- [x] DOI verified
- [x] Country verified
- [x] NDHS survey year verified
- [x] DHS file type verified
- [x] Study population verified
- [x] Outcome definition verified
- [x] Sample-size inconsistency documented
- [x] Predictor variables verified
- [x] Models compared verified
- [x] Train/test split verified
- [x] Cross-validation verified
- [x] Hyperparameter approach verified
- [x] Performance metrics verified
- [x] SHAP analysis verified
- [x] Calibration assessment verified
- [x] Survey-weighting approach verified
- [x] External-validation status verified
- [x] Limitations reviewed
- [x] Full citation verified

### Full Citation

Sani, J., Alhur, A. A., & Ahmed, M. M. (2026). Machine learning-based prediction of institutional delivery dropout (IDD) among Nigerian women: An exploratory study using SHAP interpretability. Journal of Epidemiology and Global Health, 16, 28.

### DOI / Original Publication

https://doi.org/10.1007/s44197-026-00525-y

---

## Study 5: Solanke and Rahman (2018)

### Paper Title

Multilevel Analysis of Factors Associated with Assistance During Delivery in Rural Nigeria: Implications for Reducing Rural-Urban Inequity in Skilled Care at Delivery

### Publication Status

Peer-reviewed research article published in BMC Pregnancy and Childbirth.

### Source Reviewed

Full text reviewed.

### Country / Study Setting

Nigeria.

The study focused specifically on women living in rural areas of Nigeria.

### Dataset

The study used data from the 2013 Nigeria Demographic and Health Survey (NDHS).

The analysis included a weighted sample of 12,665 rural women.

The researchers focused on the women's most recent deliveries.

### Purpose of the Study

The study aimed to investigate the individual-level and community-level characteristics associated with skilled assistance during delivery among rural women in Nigeria.

The researchers were particularly interested in rural Nigeria because previous research had documented substantial rural-urban inequalities in skilled delivery care.

They argued that previous rural Nigerian studies had concentrated mainly on individual characteristics while giving less attention to community-level influences.

### Outcome

The outcome was assistance during delivery.

It was divided into two categories:

- Skilled assistance
- Unskilled assistance

Skilled assistance included delivery assistance from trained health professionals such as doctors, nurses and midwives.

This outcome is directly relevant to my research because my proposed study also focuses on skilled birth attendance.

### Methods Used

The researchers conducted a secondary analysis of the 2013 NDHS.

Mixed-effects logistic regression was used because women were nested within communities.

The analysis therefore examined characteristics at two levels:

#### Individual-Level Characteristics

These included:

- Maternal education
- Parity
- Age at first birth
- Religion
- Participation in healthcare decision-making
- Employment status
- Access to mass media
- Means of transportation

#### Community-Level Characteristics

These included:

- Community literacy level
- Community childcare burden
- Proportion of women employed outside agriculture
- Community-level perception of distance to a health facility as a problem
- Community poverty level
- Geographical region

The multilevel approach allowed the researchers to examine whether differences in skilled assistance were related not only to women's personal characteristics but also to characteristics of the communities where they lived.

### Main Findings

Only 23.0% of the rural women received skilled assistance during their most recent delivery.

Approximately 77.0% received unskilled assistance.

The study found that both individual-level and community-level characteristics were associated with skilled assistance during delivery.

Important individual-level factors included:

- Maternal education
- Parity
- Religion
- Participation in healthcare decision-making

Important community-level factors included:

- Community poverty level
- Community literacy level

The findings showed that skilled birth attendance among rural Nigerian women was influenced by both women's personal circumstances and the broader communities in which they lived.

### My Understanding

In simple terms, the researchers wanted to understand why some women living in rural Nigeria received skilled help during childbirth while many others did not.

They found that only about 23 out of every 100 rural women in their study received skilled assistance.

The researchers did not look only at each woman's personal characteristics.

They also examined the type of community in which she lived.

For example, a woman's education and number of previous births could matter, but the poverty and literacy level of the community could also influence her chances of receiving skilled assistance.

This helped me understand that non-use of skilled birth attendance may not be explained only by characteristics of individual women.

The wider social and community environment may also be important.

### Relevance to My Research

This study is highly relevant to my research because it:

- Focuses specifically on Nigeria.
- Uses NDHS data.
- Examines skilled assistance during childbirth.
- Investigates both individual and community characteristics.

The study provides evidence that characteristics such as education, parity, religion, decision-making and community socioeconomic conditions may be relevant when investigating skilled birth attendance in Nigeria.

It also reinforces the importance of geographical and community context.

This is relevant to my proposed research because women in the NDHS are sampled within geographical clusters and may share environmental and socioeconomic characteristics.

### Differences From My Research

The study used the 2013 NDHS.

My proposed research will use the much newer 2023–24 NDHS.

The study also focused only on rural Nigerian women.

My proposed study will examine Nigeria nationally and include both rural and urban populations, subject to the final eligibility criteria established from the NDHS documentation.

Another major difference is the analytical objective.

Solanke and Rahman primarily investigated factors statistically associated with skilled assistance using mixed-effects logistic regression.

My research will focus on prediction.

I want to investigate how well information available before childbirth can identify women at higher risk of non-use of skilled birth attendance.

My research will therefore evaluate predictive performance rather than relying only on measures of statistical association.

### Predictor-Timing Considerations

This study is particularly useful because many of the characteristics it examined could reasonably be known before childbirth.

Examples include:

- Maternal education
- Parity
- Age at first birth
- Religion
- Healthcare decision-making
- Employment
- Media exposure
- Transportation
- Community literacy
- Community poverty
- Region

These characteristics are potentially suitable for consideration in a pre-delivery prediction framework.

However, I will still verify the exact definitions and timing of corresponding variables in the 2023–24 NDHS before including them in my model.

### Limitations / Research Gap Identified

The study used cross-sectional DHS data, so the relationships identified should be interpreted as associations rather than evidence of causation.

It used the 2013 NDHS, meaning that the data are substantially older than the 2023–24 NDHS that I intend to use.

The study was restricted to rural women and therefore did not develop a national model covering both rural and urban Nigerian women.

The study used mixed-effects logistic regression to identify associated factors rather than developing and evaluating machine-learning prediction models.

It therefore did not report prediction metrics such as:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- PR-AUC

Probability calibration was also not part of the study because it was not designed as a prediction-model evaluation study.

The study nevertheless provides important evidence that community-level characteristics and clustering should not be ignored when analysing skilled birth attendance in Nigeria.

### Important Variables / Factors Identified

Important factors associated with skilled assistance included:

- Maternal education
- Parity
- Religion
- Participation in healthcare decision-making
- Community poverty level
- Community literacy level

Other characteristics examined included:

- Age at first birth
- Employment status
- Media exposure
- Means of transportation
- Community childcare burden
- Community employment characteristics
- Community-level distance-to-facility problems
- Geographical region

### Pre-Delivery Variables Only?

The study was not specifically designed as a pre-delivery prediction study.

However, most of the individual and community characteristics examined could potentially be known before childbirth.

These include education, parity, religion, employment, healthcare decision-making, media exposure, transportation, community poverty, community literacy and geographical region.

This makes the study useful for identifying possible candidate predictor groups for my proposed research.

The exact corresponding variables in the 2023–24 NDHS will still need to be checked before inclusion.

### Model Evaluation

This was not a machine-learning prediction study.

- Dataset: 2013 Nigeria DHS
- Study population: Rural Nigerian women
- Weighted sample size: 12,665
- Outcome: Skilled versus unskilled assistance during delivery
- Skilled assistance prevalence: 23.0%
- Main analytical method: Mixed-effects logistic regression
- Individual-level characteristics: Yes
- Community-level characteristics: Yes
- Multilevel/community clustering considered: Yes
- Machine-learning model comparison: No
- Accuracy: Not applicable as a primary evaluation
- Precision: Not applicable as a primary evaluation
- Recall: Not applicable as a primary evaluation
- F1-score: Not applicable as a primary evaluation
- ROC-AUC: Not reported as a prediction-model evaluation
- PR-AUC: Not reported
- Calibration: Not a prediction-model evaluation component
- SHAP/explainable ML: No

### Verification Checklist

- [x] Original paper located
- [x] Full text reviewed
- [x] Authors verified
- [x] Publication details verified
- [x] DOI verified
- [x] Country verified
- [x] NDHS survey year verified
- [x] Rural study population verified
- [x] Weighted sample size verified
- [x] Outcome definition verified
- [x] Skilled-assistance prevalence verified
- [x] Individual-level variables verified
- [x] Community-level variables verified
- [x] Multilevel method verified
- [x] Main findings verified
- [x] Limitations reviewed
- [x] Full citation verified

### Full Citation

Solanke, B. L., & Rahman, S. A. (2018). Multilevel analysis of factors associated with assistance during delivery in rural Nigeria: Implications for reducing rural-urban inequity in skilled care at delivery. BMC Pregnancy and Childbirth, 18, 438.

### DOI / Original Publication

https://doi.org/10.1186/s12884-018-2074-9
---

## Study 6: Fagbamigbe and Oyedele (2022)

### Paper Title

Multivariate Decomposition of Trends, Inequalities and Predictors of Skilled Birth Attendants Utilisation in Nigeria (1990–2018): A Cross-Sectional Analysis of Change Drivers

### Publication Status

Peer-reviewed research article published in BMJ Open.

### Source Reviewed

Full text reviewed.

### Country / Study Setting

Nigeria.

The study covered women across the 36 states of Nigeria and the Federal Capital Territory.

### Dataset

The study used five waves of the Nigeria Demographic and Health Survey (NDHS):

- 1990 NDHS
- 2003 NDHS
- 2008 NDHS
- 2013 NDHS
- 2018 NDHS

The study population consisted of women aged 15–49 years who had at least one birth during the five years preceding each survey.

Across the five survey waves, the pooled analytical data contained 66,679 observations.

The researchers applied sampling weights and also constructed year-women weights to account for differences in the population of women across survey years.

### Purpose of the Study

The study aimed to investigate:

- Levels of skilled birth attendant utilisation in Nigeria.
- Trends in SBA utilisation over time.
- Inequalities in SBA utilisation.
- Factors associated with SBA utilisation.
- What contributed to changes in SBA utilisation over time.

A particularly important aim was to determine whether changes in SBA utilisation were mainly due to changes in women's characteristics or changes in how those characteristics were associated with SBA utilisation.

### Outcome

The main outcome was skilled birth attendant utilisation.

The researchers classified delivery assistance into:

- Skilled birth attendant used
- Skilled birth attendant not used

The outcome is directly relevant to my proposed research because I am also studying skilled birth attendance in Nigeria.

### Methods Used

The study used a cross-sectional analysis of five NDHS waves.

Chi-square tests for trend were used to examine changes in SBA utilisation across survey years.

The researchers used multivariate decomposition analysis (MDA) to investigate the drivers of change in SBA utilisation.

The decomposition separated changes into two broad components:

1. Endowment / characteristics component

This represents changes that may be explained by differences in the characteristics or composition of women over time.

2. Coefficient / effects component

This represents changes associated with differences in how those characteristics relate to SBA utilisation over time.

The decomposition was based on a logistic model.

The researchers used a normalisation approach to reduce bias associated with the choice of reference categories.

Multicollinearity was assessed using variance inflation factors (VIF).

The mean VIF was 1.97.

Analyses were performed using Stata 16.

### Variables Examined

The explanatory variables were organised into broad groups including demographic, health, economic and contextual/community characteristics.

Variables examined included characteristics such as:

- Maternal age
- Maternal education
- Marital status
- Employment
- Household wealth
- Healthcare decision-making
- Media access
- Place of residence
- Region
- Community socioeconomic characteristics
- Community rural population characteristics

### Main Findings

The study found that skilled birth attendant utilisation in Nigeria remained low and improved slowly over time.

SBA utilisation increased by approximately 12 percentage points between 2003 and 2018.

The authors concluded that SBA utilisation was increasing at a rate of less than 1% per year.

The multivariate decomposition showed that:

- 11.5% of the change in SBA utilisation between 2003 and 2018 was attributed to differences in characteristics/endowments.
- 88.5% was attributed to differences in coefficients/effects.

These percentages do NOT mean that 11.5% of women used SBA and 88.5% did not.

Instead, they describe the decomposition of the change in SBA utilisation over time.

Women's participation in healthcare decision-making was particularly important.

Compared with situations where the spouse alone made healthcare decisions, SBA utilisation increased substantially when women made their own healthcare decisions.

The study also found that living in states with a high proportion of rural residents was negatively associated with SBA utilisation.

### My Understanding

In simple terms, the researchers wanted to understand not only whether skilled birth attendance changed in Nigeria over time, but also WHY it changed.

They combined five different NDHS surveys covering a long period from 1990 to 2018.

They found that SBA utilisation improved, but the improvement was slow.

They then separated the change into two parts.

The first part asked:

"Did SBA use change because the characteristics of Nigerian women changed?"

For example, perhaps more women became educated or household circumstances changed.

The second part asked:

"Did SBA use change because the effect or relationship of those characteristics with SBA utilisation changed?"

The researchers found that only 11.5% of the change was attributed to differences in characteristics, while 88.5% was attributed to differences in effects.

This study also showed me that women's ability to participate in healthcare decisions and the characteristics of the communities where women live can be important for skilled birth attendance.

### Relevance to My Research

This study is highly relevant because it:

- Focuses specifically on Nigeria.
- Uses multiple waves of NDHS data.
- Examines the same general outcome of skilled birth attendance.
- Provides evidence about long-term trends.
- Examines socioeconomic and geographical inequalities.
- Considers survey weighting.
- Identifies characteristics that may be relevant to SBA utilisation.

The study provides useful historical context for my proposed research.

It shows that skilled birth attendance has been a persistent maternal-health challenge in Nigeria across several NDHS survey periods.

It also provides evidence that characteristics such as education, wealth, residence, healthcare decision-making and community context may be important when selecting candidate predictors.

### Differences From My Research

The study used NDHS surveys from 1990 through 2018.

My proposed research will use the newer 2023–24 NDHS.

The primary objective of Fagbamigbe and Oyedele was to understand trends, inequalities and drivers of changes in SBA utilisation over time.

My primary objective is prediction.

I want to investigate whether information available before childbirth can identify women at higher risk of non-use of skilled birth attendance.

The study used multivariate decomposition and regression-based methods rather than machine-learning prediction models.

Therefore, it did not compare predictive algorithms or evaluate their ability to predict individual-level non-use of SBA.

### Predictor-Timing Considerations

Many of the characteristics examined in this study could potentially be known before childbirth.

Examples include:

- Maternal age
- Education
- Household wealth
- Employment
- Healthcare decision-making
- Residence
- Region
- Media access
- Community socioeconomic characteristics

These characteristics may therefore provide useful evidence when I develop my candidate predictor list.

However, I will still verify the exact definition and timing of corresponding variables in the 2023–24 NDHS before including them in my model.

### Survey-Design Considerations

An important strength of this study is that the researchers accounted for the survey structure in their descriptive and decomposition analyses.

Sampling weights supplied with the NDHS data were used.

The researchers also calculated year-women weights to account for differences in the population sizes of women across the survey years.

This is relevant to my research because it reinforces the need to think carefully about how the complex NDHS survey design should be handled.

### Limitations / Research Gap Identified

The study used cross-sectional survey data, so associations should not be interpreted as causal effects.

The data were also subject to possible recall bias.

Although the study covered five survey waves, the newest survey included was the 2018 NDHS.

It therefore does not provide evidence from the 2023–24 NDHS.

The primary goal was explaining trends and changes at the population level rather than predicting individual women's risk of non-use of skilled birth attendance.

The study did not compare machine-learning prediction models.

It also did not evaluate prediction-model performance using measures such as:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- PR-AUC
- Calibration

These measures were not required for the study's explanatory/decomposition objective.

### Important Variables / Factors Identified

Important factors examined or highlighted included:

- Maternal education
- Household wealth
- Healthcare decision-making
- Place of residence
- Geographical region
- Media access
- Employment
- Community socioeconomic conditions
- State-level rural population characteristics

Women's healthcare decision-making autonomy was particularly important in explaining positive changes in SBA utilisation.

Living in states with high rural populations was associated with poorer SBA utilisation.

### Pre-Delivery Variables Only?

The study was not specifically designed as a pre-delivery prediction study.

However, many of the important characteristics examined could potentially be available before childbirth.

These include:

- Maternal education
- Wealth
- Residence
- Region
- Employment
- Healthcare decision-making
- Media access
- Community characteristics

Therefore, the study provides useful evidence for potential pre-delivery predictor groups.

The exact 2023–24 NDHS variables will still need to be checked individually before inclusion.

### Model Evaluation

This was not a machine-learning prediction study.

- Country: Nigeria
- NDHS waves: 1990, 2003, 2008, 2013 and 2018
- Pooled observations: 66,679
- Outcome: Skilled birth attendant utilisation
- Main analysis: Multivariate decomposition analysis
- Trend analysis: Yes
- Individual characteristics examined: Yes
- Community/contextual characteristics examined: Yes
- Sampling weights used: Yes
- Year-women weights used: Yes
- Multicollinearity assessed: Yes
- Mean VIF: 1.97
- Statistical software: Stata 16
- Machine-learning models: No
- Accuracy: Not applicable as a prediction-model evaluation
- Precision: Not applicable as a prediction-model evaluation
- Recall: Not applicable as a prediction-model evaluation
- F1-score: Not applicable as a prediction-model evaluation
- ROC-AUC: Not reported as a prediction-model evaluation
- PR-AUC: Not reported
- Calibration: Not a prediction-model evaluation component
- Explainable ML/SHAP: No

### Verification Checklist

- [x] Original paper located
- [x] Full text reviewed
- [x] Authors verified
- [x] Publication details verified
- [x] DOI verified
- [x] Country verified
- [x] NDHS survey years verified
- [x] Study population verified
- [x] Pooled observations verified
- [x] Outcome verified
- [x] Trend-analysis method verified
- [x] Multivariate decomposition method verified
- [x] Weighting approach verified
- [x] Main findings verified
- [x] 11.5% / 88.5% interpretation verified
- [x] Limitations reviewed
- [x] Full citation verified

### Full Citation

Fagbamigbe, A. F., & Oyedele, O. K. (2022). Multivariate decomposition of trends, inequalities and predictors of skilled birth attendants utilisation in Nigeria (1990–2018): A cross-sectional analysis of change drivers. BMJ Open, 12(4), e051791.

### DOI / Original Publication

https://doi.org/10.1136/bmjopen-2021-051791

---
## Study 7: Unegbu (2026)

### Paper Title

Determinants of Skilled Birth Attendance in Nigeria: A Population-Based Analysis of the 2018 Demographic and Health Survey

### Publication Status

Preprint published on medRxiv.

This study has not yet been peer reviewed.

### Source Reviewed

Full text reviewed.

### Country / Study Setting

Nigeria.

The study used nationally representative data from the 2018 Nigeria Demographic and Health Survey.

### Dataset

The study used the 2018 Nigeria Demographic and Health Survey (NDHS).

The Individual Recode (IR) file was used.

The original IR file contained 41,821 women aged 15–49 years.

The analysis was restricted to women who had a live birth during the five years preceding the survey.

There were 21,792 eligible women with a recent birth.

Women with missing information on antenatal care visits were excluded:

- Eligible women with a recent birth: 21,792
- Missing ANC information excluded: 327
- Final analytic sample: 21,465 women

Survey weights were applied in the analysis.

### Purpose of the Study

The study aimed to identify independent determinants of skilled birth attendance among Nigerian women using nationally representative 2018 NDHS data.

The researcher also aimed to examine how much the relationships between important characteristics and SBA changed after adjustment for other socioeconomic and demographic factors.

The objectives included:

- Estimating the prevalence of skilled birth attendance.
- Examining crude associations between sociodemographic factors and SBA.
- Identifying independent predictors after adjustment.
- Quantifying the amount of confounding affecting important associations.

### Outcome

The primary outcome was skilled birth attendance.

A delivery was classified as having skilled birth attendance when assistance was provided by:

- A doctor
- A nurse/midwife
- An auxiliary midwife

The DHS variables used were:

- m3a_1
- m3b_1
- m3c_1

Deliveries attended only by traditional birth attendants, relatives or no attendant were classified as not having skilled birth attendance.

This outcome is directly relevant to my proposed research.

### Predictors Examined

Seven explanatory variables were included:

- Maternal education
- Household wealth
- Urban/rural residence
- Geopolitical region
- Maternal age
- Parity
- Number of antenatal care visits

These variables were selected based on theoretical and previous empirical evidence.

### Methods Used

The study used a cross-sectional secondary analysis of the 2018 NDHS.

Survey-weighted multivariable logistic regression was used to estimate adjusted odds ratios for skilled birth attendance.

The analysis compared crude and adjusted odds ratios to examine the extent to which observed relationships were affected by confounding.

Multicollinearity was assessed using Variance Inflation Factors (VIF).

The maximum VIF was 5.52 for age-group dummy variables.

The study reported that the other predictors had VIF values below 3 and no meaningful multicollinearity was identified.

### Main Findings

The weighted prevalence of skilled birth attendance was 44.9%.

There were large geographical differences.

SBA prevalence ranged from:

- 17.7% in the North West
- 85.6% in the South West

Large socioeconomic differences were also observed.

For education:

- No education: 15.7% SBA
- Higher education: 92.3% SBA

For household wealth:

- Poorest quintile: 12.2% SBA
- Richest quintile: 87.2% SBA

After adjustment for the other predictors, several characteristics remained independently associated with skilled birth attendance.

Higher maternal education showed a strong association:

- Higher education: AOR = 7.01
- 95% CI: 5.68–8.67

Household wealth also showed a strong gradient:

- Richest versus poorest: AOR = 6.27
- 95% CI: 5.27–7.46

Antenatal care was strongly associated with SBA:

- Four or more ANC visits: AOR = 3.80
- 95% CI: 3.51–4.11

Geographical region remained important after adjustment.

Compared with the North West:

- North Central: AOR = 3.54
- North East: AOR = 1.68
- South East: AOR = 6.55
- South South: AOR = 1.74
- South West: AOR = 6.37

Parity was negatively associated with skilled birth attendance.

Compared with women with one child:

- 2–3 children: AOR = 0.63
- 4–5 children: AOR = 0.57
- 6 or more children: AOR = 0.48

### Confounding Findings

One important contribution of the study was its explicit examination of confounding.

The researcher compared crude and adjusted estimates and found that some apparently very strong relationships became substantially smaller after other characteristics were taken into account.

For example:

- Approximately 89.0% of the crude education effect was attributed to correlated socioeconomic factors.
- Approximately 87.1% of the crude wealth effect was attributed to correlated factors.
- The ANC association showed approximately 56.3% attenuation.

The researcher interpreted ANC utilisation as a particularly actionable determinant because its association remained strong after adjustment.

### My Understanding

In simple terms, this study asked why some Nigerian women had skilled assistance during childbirth while others did not.

The researcher used data from more than 21,000 Nigerian women in the 2018 NDHS.

Only about 45 out of every 100 women received skilled birth attendance.

There were very large differences across Nigeria.

For example, skilled birth attendance was much lower in the North West than in the South West.

Education and wealth were also strongly related to skilled attendance.

However, one of the most useful things I learned from this study is that variables can be related to one another.

For example, education may appear extremely important when examined alone, but women with higher education may also be wealthier, live in different regions or have better access to healthcare.

After the researchers adjusted for these overlapping characteristics, education and wealth were still important, but their effects became smaller.

ANC attendance remained strongly associated with skilled birth attendance after adjustment.

This reinforces the importance of considering relationships among predictors rather than interpreting each variable separately.

### Relevance to My Research

This study is highly relevant to my research because it:

- Focuses specifically on Nigeria.
- Uses NDHS data.
- Examines skilled birth attendance directly.
- Uses a nationally representative sample.
- Applies survey weighting.
- Examines geographical and socioeconomic inequalities.
- Identifies characteristics potentially relevant to my prediction model.

It is particularly useful because its outcome closely matches the outcome I intend to investigate.

The study also provides a useful benchmark from the 2018 NDHS against which findings from the newer 2023–24 NDHS can eventually be considered.

### Differences From My Research

This study used the 2018 NDHS.

My proposed research will use the newer 2023–24 NDHS.

The study focused on identifying independent statistical associations using survey-weighted logistic regression.

My proposed research focuses primarily on prediction.

I want to determine how well information available before childbirth can identify women at higher risk of non-use of skilled birth attendance.

I intend to compare predictive models and evaluate their performance using appropriate discrimination and calibration measures.

Another important difference is publication status.

This study is currently a preprint and has not yet undergone peer review.

Therefore, although it provides useful recent evidence, its findings should be interpreted with appropriate caution.

### Predictor-Timing Considerations

Most of the variables examined could potentially be known before childbirth.

These include:

- Maternal education
- Household wealth
- Residence
- Region
- Maternal age
- Parity

ANC attendance requires more careful consideration.

The study used a variable indicating whether the woman attended four or more ANC visits.

Although ANC occurs before delivery, the final total number of visits is only known later in pregnancy.

Whether this variable is appropriate for my research therefore depends on my defined prediction point.

If I intend to make predictions before a woman has had the opportunity to complete four ANC visits, using the final ANC count would introduce future information.

Therefore, I will define my prediction point before deciding how ANC information should be represented.

### Survey-Design Considerations

The study used survey-weighted analysis to account for the NDHS sampling design.

This is important because the NDHS is based on a complex sampling structure rather than a simple random sample of Nigerian women.

The study therefore provides useful methodological evidence for considering survey design in my proposed analysis.

However, my research will involve prediction modelling, so I will need to determine separately how survey weights, geographical clusters and validation should be handled in a machine-learning setting.

### Limitations / Research Gap Identified

The study used cross-sectional data, so the reported associations should not automatically be interpreted as causal relationships.

The NDHS variables are partly self-reported and may therefore be affected by recall or reporting bias.

The analysis used the 2018 NDHS rather than the newer 2023–24 NDHS.

The study used seven selected predictors and survey-weighted logistic regression rather than comparing multiple machine-learning prediction models.

It therefore did not evaluate prediction performance using measures such as:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- PR-AUC
- Probability calibration

These were not required for the study's explanatory objective.

The study also did not evaluate whether a prediction model performs differently across geographical or socioeconomic subgroups.

Finally, the study is currently a preprint and has not yet undergone peer review.

### Important Variables / Factors Identified

Important independent determinants included:

- Maternal education
- Household wealth
- Antenatal care attendance
- Geopolitical region
- Maternal age
- Parity
- Urban/rural residence

The study particularly highlighted:

- Education
- Wealth
- ANC utilisation
- Regional inequality

### Pre-Delivery Variables Only?

Most of the seven predictors could potentially be available before childbirth.

These include:

- Education
- Wealth
- Residence
- Region
- Maternal age
- Parity

ANC information could also be available before delivery, but the use of the final number of ANC visits depends on the prediction point.

Therefore, I will not automatically use the final ANC count as a predictor without first defining when my model is intended to make its prediction.

### Model Evaluation

This was not a machine-learning prediction study.

- Country: Nigeria
- Dataset: 2018 NDHS
- DHS file: Individual Recode
- Eligible recent-birth sample: 21,792
- Missing ANC exclusions: 327
- Final analytic sample: 21,465
- Outcome: Skilled birth attendance
- Weighted SBA prevalence: 44.9%
- North West SBA prevalence: 17.7%
- South West SBA prevalence: 85.6%
- Number of explanatory variables: 7
- Main analytical method: Survey-weighted multivariable logistic regression
- Confounding analysis: Yes
- Multicollinearity assessment: Yes
- Maximum VIF: 5.52
- Machine-learning comparison: No
- Accuracy: Not applicable as a prediction-model evaluation
- Precision: Not applicable as a prediction-model evaluation
- Recall: Not applicable as a prediction-model evaluation
- F1-score: Not applicable as a prediction-model evaluation
- ROC-AUC: Not reported as a prediction-model evaluation
- PR-AUC: Not reported
- Calibration: Not a prediction-model evaluation component
- SHAP/explainable ML: No

### Verification Checklist

- [x] Original preprint located
- [x] Full text reviewed
- [x] Author verified
- [x] Publication status verified
- [x] DOI verified
- [x] Country verified
- [x] NDHS survey year verified
- [x] DHS file verified
- [x] Eligibility criteria verified
- [x] Sample size verified
- [x] Outcome definition verified
- [x] Predictors verified
- [x] Survey-weighted method verified
- [x] SBA prevalence verified
- [x] Regional prevalence figures verified
- [x] Adjusted odds ratios verified
- [x] Confounding results verified
- [x] Multicollinearity assessment verified
- [x] Limitations reviewed
- [x] Full citation verified

### Full Citation

Unegbu, U. L. (2026). Determinants of skilled birth attendance in Nigeria: A population-based analysis of the 2018 Demographic and Health Survey. medRxiv [Preprint].

### DOI / Original Publication

https://doi.org/10.64898/2026.04.23.26350432

---

## Study 8: Ogbo et al. (2020)

### Paper Title

Prevalence, Trends, and Drivers of the Utilization of Unskilled Birth Attendants during Democratic Governance in Nigeria from 1999 to 2018

### Publication Status

Peer-reviewed research article published in the International Journal of Environmental Research and Public Health.

### Source Reviewed

Full text reviewed.

### Country / Study Setting

Nigeria.

The study used nationally representative Nigeria Demographic and Health Survey data covering the period from 1999 to 2018.

### Dataset

The study used five Nigeria Demographic and Health Survey rounds:

- 1999 NDHS: 3,552 participants
- 2003 NDHS: 6,029 participants
- 2008 NDHS: 28,647 participants
- 2013 NDHS: 31,482 participants
- 2018 NDHS: 34,193 participants

Across the five survey rounds, the study included a weighted total of 103,903 participants.

The NDHS used a two-stage stratified sampling design.

### Purpose of the Study

The study aimed to examine the prevalence, trends and factors associated with the utilisation of unskilled birth attendants in Nigeria during the period of democratic governance from 1999 to 2018.

The researchers distinguished between:

- Traditional birth attendants (TBAs)
- Other unskilled birth attendants
- Skilled birth attendants

This allowed them to investigate not only whether women received skilled care but also the type of unskilled assistance women received during childbirth.

The study did not attempt to establish a causal relationship between democratic governance or government policies and birth-attendant use. Instead, the researchers examined trends occurring during the period of democratic governance.

### Outcome

The main outcomes were delivery assisted by:

1. Traditional birth attendants
2. Other unskilled birth attendants

Skilled birth-attendant-assisted delivery was used as the reference category in the multinomial regression analysis.

Skilled birth assistance included assistance from:

- Doctors
- Nurses/midwives
- Auxiliary nurses/midwives

Other unskilled birth attendants included:

- Community health extension workers
- Relatives
- Friends
- No assistance

Traditional birth attendants were examined separately.

This distinction is important for my research because the definition of non-use of skilled birth attendance should be based on the provider categories used in the 2023–24 NDHS rather than simply treating all delivery settings or attendants as equivalent.

### Methods Used

The researchers conducted secondary analyses of nationally representative NDHS data.

Descriptive analyses were used to examine the prevalence and trends of different types of delivery assistance over time.

Percentage-point changes with 95% confidence intervals were calculated to examine changes in TBA-assisted and other-unskilled-attendant-assisted deliveries.

Multivariable multinomial logistic regression was used to investigate factors associated with the use of:

- Traditional birth attendants
- Other unskilled birth attendants

Skilled birth-attendant-assisted delivery was the reference outcome.

The explanatory variables were organised using an adapted Andersen behavioural model into:

- Community-level factors
- Predisposing factors
- Enabling factors
- Need factors

The multivariable analysis was conducted using a four-stage modelling approach.

### Factors Examined

Factors examined included:

#### Community-Level Factors

- Urban/rural residence
- Geopolitical region

#### Sociodemographic / Predisposing Factors

- Maternal age
- Maternal education
- Paternal education
- Maternal employment
- Household wealth
- Media exposure

#### Health-Service / Enabling Factors

- Antenatal care attendance
- Proximity to health facilities
- Ability to obtain money for healthcare
- Women's autonomy and household decision-making

#### Reproductive / Need Factors

The study also considered maternal and reproductive characteristics, including birth interval.

### Main Findings

The use of traditional birth attendants remained almost unchanged over the study period.

TBA-assisted delivery was:

- 20.7% in 1999
- 20.5% in 2018

The difference was not statistically significant.

In contrast, the use of other unskilled birth attendants declined significantly.

It decreased from:

- 45.5% in 2003
- 36.2% in 2018

The study also reported some improvement in skilled birth attendance, from approximately:

- 38.1% in 2013
- 43.3% in 2018

Several characteristics were associated with lower odds of using unskilled birth attendants, including:

- Higher maternal education
- Higher paternal education
- Maternal employment
- Greater household wealth
- Media exposure
- Older maternal age
- Four or more ANC visits
- Better proximity to healthcare facilities
- Ability to obtain money for healthcare
- Greater female autonomy

Characteristics associated with higher odds of unskilled-birth-attendant use included:

- Rural residence
- Some geopolitical regions
- Younger maternal age
- Longer birth interval

### My Understanding

In simple terms, the researchers wanted to understand who was assisting Nigerian women during childbirth and whether this changed between 1999 and 2018.

One of the most important findings was that traditional birth-attendant use barely changed.

About 21 out of every 100 women used traditional birth attendants in both 1999 and 2018.

The use of other types of unskilled attendants decreased, but it was still common in 2018.

The researchers also found that women's social and economic circumstances mattered.

Women with more education, greater household wealth, adequate ANC attendance, better access to healthcare, media exposure and greater decision-making autonomy were generally less likely to use unskilled birth attendants.

Women living in rural areas and some geographical regions were more likely to use unskilled attendants.

This study helped me understand that non-use of skilled birth attendance in Nigeria is connected to several overlapping socioeconomic, geographical and healthcare-access factors.

### Relevance to My Research

This study is highly relevant to my research because it:

- Focuses specifically on Nigeria.
- Uses NDHS data.
- Examines delivery assistance.
- Directly distinguishes skilled from unskilled birth attendants.
- Covers multiple NDHS survey periods.
- Examines socioeconomic, geographical and healthcare-access factors.

My proposed research focuses on predicting non-use of skilled birth attendance.

Therefore, understanding the characteristics associated with the use of traditional and other unskilled attendants provides important background evidence about the population I am trying to identify.

The study also identifies several potential candidate predictor groups, including:

- Education
- Household wealth
- Residence
- Geopolitical region
- Healthcare access
- Media exposure
- Maternal age
- Women's autonomy

### Differences From My Research

This study examined trends and factors associated with different types of unskilled birth-attendant utilisation.

My proposed research will focus specifically on predicting non-use of skilled birth attendance using the 2023–24 NDHS.

The study's latest dataset was the 2018 NDHS.

My study therefore uses a newer national survey.

The study used multinomial logistic regression primarily to investigate statistical associations.

My research will focus on prediction and will compare predictive models and evaluate their performance.

Another important difference is predictor timing.

My main prediction model will be restricted to information that could reasonably be available before the delivery being predicted.

### Predictor-Timing Considerations

Many of the characteristics examined in this study could potentially be available before childbirth, including:

- Maternal education
- Paternal education
- Household wealth
- Maternal employment
- Residence
- Geopolitical region
- Media exposure
- Maternal age
- Healthcare-access characteristics
- Women's autonomy

ANC requires more careful consideration.

The study identified four or more ANC visits as associated with lower odds of using unskilled birth attendants.

Although ANC occurs before delivery, the final number of ANC visits is not known early in pregnancy.

Therefore, whether this information can be used in my prediction model depends on the prediction point I eventually define.

Birth interval also requires careful definition because it must be clear which births are being compared and whether the information would be known before the index delivery.

### Survey-Design Considerations

The study used nationally representative NDHS data obtained through a two-stage stratified sampling design.

The paper reports weighted counts and proportions in its analyses.

This reinforces the importance of considering the complex survey structure when analysing NDHS data.

For my prediction study, I will need to decide separately how survey weights, clusters and stratification should be handled during model development and validation.

### Limitations / Research Gap Identified

The study used repeated cross-sectional DHS surveys rather than following the same women over time.

DHS information is partly self-reported and may therefore be affected by recall or reporting bias.

The analysis was limited to variables available in the NDHS.

The most recent survey used was the 2018 NDHS.

Therefore, the study does not provide evidence from the newer 2023–24 NDHS.

The study focused on trends and statistical associations rather than developing a prospective-style prediction model.

It did not compare multiple machine-learning algorithms.

Prediction-model performance measures such as ROC-AUC, PR-AUC and probability calibration were not part of the study's primary analytical objective.

Another important issue for my research is outcome definition.

The study distinguished TBAs and other unskilled attendants from skilled attendants.

I will not simply copy these categories without checking the provider classifications used in the 2023–24 NDHS.

My outcome will be constructed according to the skilled-provider definition applicable to the 2023–24 NDHS.

### Important Variables / Factors Identified

Important factors included:

- Maternal education
- Paternal education
- Household wealth
- Maternal employment
- ANC attendance
- Urban/rural residence
- Geopolitical region
- Healthcare accessibility
- Maternal age
- Media exposure
- Women's autonomy
- Birth interval

### Pre-Delivery Variables Only?

The study was not specifically designed as a pre-delivery prediction study.

However, many of the characteristics examined could potentially be known before childbirth.

These include:

- Education
- Household wealth
- Employment
- Residence
- Region
- Healthcare access
- Maternal age
- Media exposure
- Women's autonomy

ANC and some reproductive-history variables require more careful timing assessment.

Therefore, each candidate variable will be checked against its exact definition in the 2023–24 NDHS and against the prediction point selected for my study.

### Model Evaluation

This was not a machine-learning prediction study.

- Country: Nigeria
- NDHS rounds: 1999, 2003, 2008, 2013 and 2018
- Total participants across surveys: 103,903
- Main outcomes: TBA-assisted and other-unskilled-attendant-assisted delivery
- Reference outcome: Skilled birth-attendant-assisted delivery
- Main analytical method: Multivariable multinomial logistic regression
- TBA use in 1999: 20.7%
- TBA use in 2018: 20.5%
- Other unskilled-attendant use in 2003: 45.5%
- Other unskilled-attendant use in 2018: 36.2%
- Skilled birth-attendant use in 2013: approximately 38.1%
- Skilled birth-attendant use in 2018: approximately 43.3%
- Machine-learning model comparison: No
- Accuracy: Not applicable as a prediction-model evaluation
- Precision: Not applicable as a prediction-model evaluation
- Recall: Not applicable as a prediction-model evaluation
- F1-score: Not applicable as a prediction-model evaluation
- ROC-AUC: Not reported as a prediction-model evaluation
- PR-AUC: Not reported
- Calibration: Not a prediction-model evaluation component
- SHAP/explainable ML: No

### Verification Checklist

- [x] Original paper located
- [x] Full text reviewed
- [x] Correct authors verified
- [x] Publication details verified
- [x] DOI verified
- [x] Country verified
- [x] NDHS survey rounds verified
- [x] Survey sample sizes verified
- [x] Total sample across survey rounds verified
- [x] Outcome categories verified
- [x] Skilled-attendant reference category verified
- [x] Methods verified
- [x] TBA prevalence figures verified
- [x] Other-unskilled-attendant prevalence figures verified
- [x] Important factors verified
- [x] Limitations reviewed
- [x] Full citation verified

### Full Citation

Ogbo, F. A., Trinh, F. F., Ahmed, K. Y., Senanayake, P., Rwabilimbo, A. G., Uwaibi, N. E., Agho, K. E., & Global Maternal and Child Health Research Collaboration (GloMACH). (2020). Prevalence, trends, and drivers of the utilization of unskilled birth attendants during democratic governance in Nigeria from 1999 to 2018. International Journal of Environmental Research and Public Health, 17(1), 372.

### DOI / Original Publication

https://doi.org/10.3390/ijerph17010372
---

## Study 9: Osborne et al. (2026)

### Paper Title

Hierarchical Machine Learning Models for Predicting Antenatal Care Utilisation Among Nigerian Women: Identifying Actionable Insights for Health Policy

### Publication Status

Peer-reviewed research article published in BioData Mining.

### Source Reviewed

Full text reviewed.

### Country / Study Setting

Nigeria.

The study used nationally representative data from the 2024 Nigeria Demographic and Health Survey.

### Dataset

The study used the 2024 Nigeria Demographic and Health Survey (NDHS).

The initial study population consisted of 17,986 women of reproductive age who had experienced a pregnancy.

After data cleaning, exclusion of missing or invalid ANC information, and application of the study eligibility criteria, the final analytical sample included:

- 13,955 women

The researchers examined ANC utilisation during the women's most recent pregnancies within the survey recall period.

This study is particularly important to my literature review because it confirms that machine-learning research using the new 2024 NDHS has already begun.

### Purpose of the Study

The study aimed to use machine learning to predict antenatal care utilisation among Nigerian women.

Rather than treating ANC utilisation as a simple yes/no outcome, the researchers recognised that maternal healthcare utilisation can occur in stages.

They therefore developed a hierarchical modelling framework that examined:

1. Whether a woman accessed ANC at all.
2. Among women who accessed ANC, whether they received adequate ANC.

The study also aimed to identify important socioeconomic, demographic, geographical and healthcare-access characteristics influencing ANC utilisation.

### Outcome

ANC utilisation was divided into three categories:

- No ANC: 0 visits
- Inadequate ANC: 1–7 visits
- Adequate ANC: 8 or more visits

The ≥8-visit definition was based on the WHO 2016 recommendation.

The authors noted that DHS records visits, while the WHO recommendation refers to contacts, so visits were used as a proxy for contacts.

For the hierarchical model, two binary prediction stages were constructed.

#### Stage 1

Any ANC versus no ANC.

#### Stage 2

Among ANC users:

Adequate ANC versus inadequate ANC.

This outcome is related to maternal healthcare utilisation but is **not the same as skilled birth attendance**, which is the outcome in my proposed research.

### Methods Used

The researchers compared several supervised machine-learning algorithms:

- Logistic Regression
- Stochastic Gradient Descent with log-loss
- Random Forest
- XGBoost
- LightGBM

The final hierarchical framework used:

- LightGBM for Stage 1: Any ANC versus no ANC
- XGBoost for Stage 2: Adequate versus inadequate ANC among ANC users

The analytical dataset was divided into:

- 75% training data
- 25% test data

Stratified random sampling was used to preserve the distribution of the ANC outcome.

The test set was withheld from model training and model selection and used for final evaluation.

The researchers used pipeline-based preprocessing to reduce the risk of applying preprocessing inconsistently across the training and test datasets.

Hyperparameters for the hierarchical models were specified in advance based on previous methodological evidence and preliminary stability assessment rather than automated hyperparameter optimisation.

### Feature Engineering

The researchers created predictors representing demographic, socioeconomic, informational and healthcare-access characteristics.

Variables included:

- Maternal age
- Marital status
- Pregnancy intention
- Religion
- Ethnicity
- Region
- Urban/rural residence

The researchers also constructed composite variables.

#### Media Exposure Index

This incorporated exposure to:

- Radio
- Television
- Newspapers

#### Socioeconomic Status Index

This incorporated:

- Education
- Household wealth
- Health insurance
- Employment

#### Healthcare Access Difficulty Index

This represented perceived difficulty in accessing healthcare.

The engineered variables were intended to reduce multicollinearity while retaining useful information for prediction.

### Main Findings

Among the 13,955 women:

- 27.90% had no ANC
- 54.52% had inadequate ANC (1–7 visits)
- 17.58% had adequate ANC (≥8 visits)

The single-stage multiclass models had difficulty identifying the smaller adequate-ANC group.

Logistic Regression achieved the highest overall accuracy among the single-stage models:

- Accuracy: 0.65

However, recall for adequate ANC across the single-stage models ranged only from approximately:

- 0.50 to 0.57

The hierarchical model improved performance.

#### Stage 1

LightGBM was used to distinguish any ANC from no ANC.

The model achieved:

- Accuracy: 0.77
- Recall for any ANC: 0.87

Recall for the no-ANC group was lower at approximately 0.49.

#### Stage 2

XGBoost was used to distinguish adequate from inadequate ANC among ANC users.

The model achieved:

- Accuracy: 0.81

Threshold optimisation was used to improve identification of women with adequate ANC.

At the selected policy-oriented threshold of 0.20:

- Recall for adequate ANC: 0.80
- Precision for adequate ANC: 0.50

The final hierarchical three-class model achieved:

- Micro-averaged AUROC: 0.831
- Micro-averaged average precision: 0.695

### Calibration

The researchers explicitly evaluated probability calibration.

Calibration was assessed using:

- Reliability/calibration diagrams
- Brier scores

The reported Brier scores were:

- Stage 1: 0.154
- Stage 2: 0.133

The researchers reported satisfactory agreement between predicted probabilities and observed outcomes.

This study is therefore important to my methodology because it demonstrates the use of calibration assessment in machine-learning research using the same 2024 NDHS that I intend to use.

### Explainability

SHAP was used to explain the model's predictions.

The researchers used SHAP at different levels, including:

- Global feature importance
- Class-specific explanations
- Individual-level explanations

Important predictors included socioeconomic and geographical characteristics.

Key factors included:

- Socioeconomic status
- Rural residence
- Healthcare-access difficulty

The effects of predictors differed depending on whether the model was predicting no ANC, inadequate ANC or adequate ANC.

### My Understanding

In simple terms, the researchers used the new 2024 Nigeria DHS to predict how women used antenatal care.

Instead of asking only:

"Did this woman attend ANC?"

they separated the problem into two stages.

First:

"Did she attend ANC at all?"

Then, if she attended:

"Did she receive enough ANC?"

This makes sense because accessing healthcare for the first time and continuing to receive adequate care may be influenced by different barriers.

The researchers found that a two-stage model performed better at identifying women with adequate ANC than simply asking one model to classify all three groups at once.

They also checked whether the predicted probabilities were reliable using calibration analysis.

SHAP was then used to explain which characteristics were influencing the predictions.

This study helped me understand that machine-learning research has already been conducted using the 2024 NDHS, but on ANC utilisation rather than skilled birth attendance.

### Relevance to My Research

This study is highly relevant to my research for several reasons.

First, it uses the **same 2024 Nigeria DHS** that I intend to use.

Second, it focuses on maternal healthcare utilisation in Nigeria.

Third, it uses machine learning.

Fourth, it evaluates:

- Discrimination
- Precision and recall
- Calibration
- PR performance
- Threshold optimisation
- Explainability using SHAP

This makes it an important methodological comparison for my proposed research.

It also shows that simply claiming:

"No machine-learning research has used the 2024 NDHS"

would be incorrect.

Machine-learning research using the 2024 NDHS already exists.

Therefore, my research gap must be more specific.

### Differences From My Research

The most important difference is the outcome.

Osborne et al. predicted:

**Antenatal care utilisation.**

My proposed research will predict:

**Non-use of skilled birth attendance.**

ANC occurs during pregnancy.

Skilled birth attendance concerns who assists the woman during childbirth.

Therefore, these are related maternal-health services but they are not the same outcome.

Another difference is predictor timing.

Because the Osborne et al. outcome is ANC utilisation itself, the modelling framework was designed around ANC behaviour.

My research will specifically restrict predictors to information that could reasonably be available **before the delivery being predicted**.

I also intend to investigate whether model performance differs across important Nigerian geographical and socioeconomic groups.

### Predictor-Timing Considerations

Many of the characteristics used by Osborne et al. could potentially be available before childbirth.

These include:

- Maternal age
- Education
- Household wealth
- Employment
- Health insurance
- Marital status
- Religion
- Ethnicity
- Region
- Residence
- Pregnancy intention
- Healthcare-access difficulty
- Media exposure

These provide useful candidate predictor groups for my research.

However, I will not automatically copy the engineered indices used in this study.

Each variable and any proposed composite measure will need to be justified using the 2024 NDHS documentation and my defined pre-delivery prediction point.

### Validation and Survey-Design Considerations

The study used a 75/25 stratified random train-test split.

The test set was held out for final model evaluation.

However, the models were fitted without survey weights.

The authors explicitly identified this as a limitation.

They noted that the models were designed for sample-level prediction rather than population-level inference and that absence of survey weighting could affect generalisability to the wider Nigerian population.

The paper describes the 2024 NDHS as using a stratified multistage cluster sampling design.

However, a DHS cluster-aware train-test split was not described.

This is important for my proposed research because I will need to decide carefully how geographical clustering, survey weighting and validation should be handled.

### Limitations / Research Gap Identified

The study used cross-sectional NDHS data, limiting causal interpretation.

ANC information was self-reported and may therefore be affected by recall bias.

Women with missing or invalid information were excluded, which may affect representation of some groups.

The machine-learning models were not survey weighted.

A cluster-aware validation strategy based on DHS sampling clusters was not described.

The study focused on ANC utilisation rather than skilled birth attendance.

Therefore, although it demonstrates that machine learning, SHAP and calibration have already been applied to the 2024 NDHS, it does **not** answer my proposed research question.

This helps refine my research gap.

The gap is not simply:

"No machine-learning study has used the 2024 NDHS."

Instead, the potential gap is more specifically whether the 2024 NDHS has been used to develop and evaluate a Nigeria-specific prediction model for **non-use of skilled birth attendance**, using predictors selected according to a clearly defined **pre-delivery prediction point**.

That gap still needs to be confirmed through the complete literature search.

### Important Variables / Factors Identified

Important predictors and predictor groups included:

- Socioeconomic status
- Rural/urban residence
- Region
- Healthcare-access difficulty
- Maternal age
- Education
- Household wealth
- Employment
- Health insurance
- Marital status
- Religion
- Ethnicity
- Pregnancy intention
- Media exposure

### Pre-Delivery Variables Only?

The study was not designed specifically around predicting skilled birth attendance before delivery.

However, many of the characteristics used in the models could potentially be known before childbirth.

These include socioeconomic, demographic, geographical and healthcare-access characteristics.

Their suitability for my study will depend on:

- Their exact NDHS definitions
- When they were measured
- My final prediction point
- Whether any engineered variables can be constructed without introducing information unavailable at prediction time

### Model Evaluation

- Country: Nigeria
- Dataset: 2024 NDHS
- Initial study population: 17,986
- Final analytical sample: 13,955
- Outcome: ANC utilisation
- No ANC: 27.90%
- Inadequate ANC: 54.52%
- Adequate ANC: 17.58%
- Train/test split: 75/25
- Split method: Stratified random sampling
- Models compared: Logistic Regression, SGD, Random Forest, XGBoost and LightGBM
- Stage 1 model: LightGBM
- Stage 2 model: XGBoost
- Stage 1 accuracy: 0.77
- Stage 1 recall for any ANC: 0.87
- Stage 2 accuracy: 0.81
- Stage 2 adequate-ANC recall after threshold optimisation: 0.80
- Stage 2 adequate-ANC precision at selected threshold: 0.50
- Final hierarchical micro-AUROC: 0.831
- Final hierarchical average precision: 0.695
- Calibration: Yes
- Stage 1 Brier score: 0.154
- Stage 2 Brier score: 0.133
- Explainability: SHAP
- Threshold optimisation: Yes
- Automated hyperparameter tuning: No
- Survey-weighted ML fitting: No
- Cluster-aware train/test split: Not described

### Verification Checklist

- [x] Original paper located
- [x] Full text reviewed
- [x] Authors verified
- [x] Publication status verified
- [x] DOI verified
- [x] 2024 NDHS dataset verified
- [x] Initial study population verified
- [x] Final sample size verified
- [x] ANC outcome definitions verified
- [x] Models compared verified
- [x] Train/test split verified
- [x] Hierarchical modelling framework verified
- [x] Threshold optimisation verified
- [x] Performance metrics verified
- [x] AUROC and average precision verified
- [x] Calibration method verified
- [x] Brier scores verified
- [x] SHAP analysis verified
- [x] Survey-weighting status verified
- [x] Limitations reviewed
- [x] Full citation verified

### Full Citation

Osborne, A., Olawade, D. B., Oton, E. A., Odey, L. M., & Usani, K. (2026). Hierarchical machine learning models for predicting antenatal care utilisation among Nigerian women: Identifying actionable insights for health policy. BioData Mining, 19, 24.

### DOI / Original Publication

https://doi.org/10.1186/s13040-026-00538-0
---

## Study 10: Fagbamigbe et al. (2017)

### Paper Title

Trends and Drivers of Skilled Birth Attendant Use in Nigeria (1990–2013): Policy Implications for Child and Maternal Health

### Publication Status

Peer-reviewed research article published in the International Journal of Women’s Health.

### Source Reviewed

Full text reviewed.

### Country / Study Setting

Nigeria.

The study examined skilled birth attendant utilisation nationally across multiple Nigeria Demographic and Health Survey periods.

### Dataset

The study pooled data from four Nigeria Demographic and Health Survey rounds conducted between 1990 and 2013:

- 1990 NDHS
- 2003 NDHS
- 2008 NDHS
- 2013 NDHS

The researchers applied sample weights and adjusted the analyses for the survey design and sampling errors.

### Purpose of the Study

The study aimed to examine trends in the utilisation of skilled birth attendants in Nigeria between 1990 and 2013 and identify factors associated with SBA utilisation.

The researchers wanted to answer questions including:

- How did SBA utilisation change over time?
- Were the changes substantial?
- Which characteristics were associated with SBA utilisation?
- Which factors could help explain the persistently low use of skilled attendance?

### Outcome

The primary outcome was utilisation of a skilled birth attendant during delivery.

Skilled attendants were defined as:

- Doctors
- Nurses
- Midwives
- Auxiliary nurses/midwives

Other forms of delivery assistance were classified as unskilled.

This outcome is directly relevant to my proposed research because I am also investigating skilled birth attendance in Nigeria.

### Methods Used

The researchers pooled data from the four NDHS rounds.

The analysis included:

- Descriptive statistics
- Tests of association
- Logistic regression

The researchers examined the prevalence and relative changes in SBA utilisation and investigated factors associated with SBA use.

Sample weights were applied, and adjustments were made for the complex survey design and sampling errors.

The explanatory characteristics were organised into broad groups.

#### Sociocultural Factors

These included:

- Maternal age
- Maternal education
- Marital status
- Ethnicity
- Religion
- Women's involvement in decisions about how their earnings were spent
- Women's involvement in decisions about their use of healthcare facilities

#### Perceived Need / Maternal Healthcare Factors

These included:

- Pregnancy wantedness
- Adequacy of ANC utilisation
- Skilled birth attendant use during the previous delivery
- Birth order

ANC utilisation was categorised as:

- No ANC
- Inadequate ANC: 1–3 visits
- Adequate ANC: 4 or more visits

#### Economic Accessibility Factors

These included:

- Maternal employment
- Household wealth

### Main Findings

Skilled birth attendant utilisation remained low throughout the study period.

SBA utilisation increased from:

- 32.4% in 1990
- 38.5% in 2013

The authors described this as only a marginal and statistically insignificant improvement over the study period.

Large differences in SBA utilisation were observed according to women's characteristics.

Education was particularly important.

The study reported SBA utilisation of:

- 92.4% among more highly educated women
- 13.1% among women with no formal education

After adjustment for other characteristics, educated women had approximately three times the odds of SBA utilisation compared with women without education:

- Adjusted OR = 3.09
- 95% CI = 2.17–4.38

Women's involvement in healthcare decision-making was also important.

Women who participated in decisions about their use of healthcare facilities were approximately 12% more likely to use skilled birth attendants than women who did not.

Other significant characteristics included:

- Religion
- Ethnicity
- Urban/rural residence
- Geographical zone

The study also found that SBA utilisation tended to be higher among women with:

- Greater household wealth
- Adequate ANC utilisation
- Previous use of skilled birth attendance
- Lower birth order

SBA utilisation was generally lower in northern regions than in southern regions.

### My Understanding

In simple terms, the researchers wanted to understand whether Nigerian women were becoming more likely to receive skilled assistance during childbirth and what characteristics were associated with receiving that care.

They compared four Nigeria DHS surveys covering the period from 1990 to 2013.

They found that skilled birth attendance improved only slightly.

It increased from about 32 out of every 100 women in 1990 to about 39 out of every 100 women in 2013.

Education was particularly important.

Women with more education were much more likely to use skilled birth attendants than women without formal education.

Women's ability to participate in decisions about their own healthcare also mattered.

The study also showed differences according to religion, ethnicity, residence and geographical region.

This helped me understand that skilled birth attendance in Nigeria is related to a combination of socioeconomic, geographical, healthcare and women's empowerment characteristics.

### Relevance to My Research

This study is highly relevant because it:

- Focuses specifically on Nigeria.
- Uses NDHS data.
- Examines skilled birth attendance directly.
- Examines multiple NDHS periods.
- Accounts for survey weighting and design.
- Identifies socioeconomic, geographical and healthcare characteristics associated with SBA utilisation.

It provides important historical evidence showing that low skilled birth attendance has persisted in Nigeria over several survey periods.

It also identifies potential predictor groups that may be useful when I examine the 2023–24 NDHS.

These include:

- Education
- Household wealth
- Residence
- Geographical region
- Maternal age
- Healthcare decision-making
- Employment
- ANC information
- Birth order

### Differences From My Research

This study focused primarily on trends and statistical associations.

My proposed study focuses on prediction.

Fagbamigbe et al. asked approximately:

"How has skilled birth attendance changed in Nigeria, and which characteristics are associated with its utilisation?"

My research asks:

"How well can information available before childbirth predict non-use of skilled birth attendance using the 2023–24 NDHS?"

Another important difference is the survey period.

The newest NDHS included in this study was the 2013 survey.

My research will use the much newer 2023–24 NDHS.

The study used logistic regression to investigate associations rather than comparing multiple machine-learning prediction models.

My proposed research will evaluate predictive performance, including discrimination and calibration, and investigate model performance across important geographical and socioeconomic groups.

### Predictor-Timing Considerations

This study is especially useful for my research because it highlights an important issue concerning predictor timing.

Several characteristics examined could reasonably be known before childbirth, including:

- Maternal education
- Household wealth
- Maternal age
- Religion
- Ethnicity
- Residence
- Geographical zone
- Employment
- Healthcare decision-making
- Birth order

However, some variables require more careful consideration.

#### ANC Utilisation

The study used the final number of ANC visits.

ANC occurs before childbirth, but whether the final ANC count is appropriate for my prediction model depends on when the prediction is intended to be made.

If my model is intended for use earlier in pregnancy, the woman's eventual total number of ANC visits would not yet be known.

#### Previous Skilled Birth Attendance

The study included whether a woman used a skilled birth attendant during her previous delivery.

This could potentially be a valid pre-delivery predictor for a later birth because that previous delivery has already occurred.

However, I would need to make certain that the variable genuinely refers to a birth before the index delivery and not the same delivery I am trying to predict.

This distinction is important for preventing data leakage.

### Survey-Design Considerations

The researchers applied NDHS sample weights.

They also adjusted their analyses for survey design and sampling errors.

This is relevant to my research because the NDHS is based on a complex survey design.

Although my primary objective is prediction rather than population-level causal inference, I will still need to decide carefully how survey weights, stratification and geographical clustering should be handled during analysis and model validation.

### Limitations / Research Gap Identified

The study used repeated cross-sectional DHS data, so the associations identified should not automatically be interpreted as causal.

The information was based partly on respondents' recall and may therefore be affected by recall or reporting bias.

The newest dataset was the 2013 NDHS.

Therefore, the study cannot describe patterns captured by the newer 2023–24 NDHS.

The study focused on trends and statistical associations rather than developing and validating a prediction model.

It did not compare machine-learning algorithms or report prediction-model evaluation measures such as:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- PR-AUC
- Probability calibration

These measures were not required for the study's explanatory objective.

Another important issue for my research is predictor timing.

Variables such as final ANC utilisation and previous SBA use need to be carefully defined relative to the specific delivery being predicted.

### Important Variables / Factors Examined

Important factors included:

- Maternal age
- Maternal education
- Marital status
- Religion
- Ethnicity
- Urban/rural residence
- Geographical zone
- Maternal employment
- Household wealth
- Healthcare decision-making
- Women's control over earnings
- Pregnancy wantedness
- ANC utilisation
- Birth order
- Previous skilled birth attendant use

### Pre-Delivery Variables Only?

No.

The study was not specifically designed as a pre-delivery prediction study.

Many characteristics could potentially be available before childbirth, including:

- Maternal education
- Household wealth
- Religion
- Ethnicity
- Residence
- Region
- Maternal age
- Employment
- Healthcare decision-making
- Birth order

However, ANC utilisation and previous skilled birth attendance require careful timing checks.

For my proposed study, every predictor will be assessed relative to the specific index delivery and my defined prediction point before being included in the main model.

### Model Evaluation

This was not a machine-learning prediction study.

- Country: Nigeria
- NDHS rounds: 1990, 2003, 2008 and 2013
- Outcome: Skilled birth attendant utilisation
- SBA prevalence in 1990: 32.4%
- SBA prevalence in 2013: 38.5%
- Main analytical methods: Descriptive analysis, tests of association and logistic regression
- Survey weights used: Yes
- Survey-design adjustment: Yes
- Education adjusted OR: 3.09
- Education 95% CI: 2.17–4.38
- Machine-learning comparison: No
- Accuracy: Not applicable as a prediction-model evaluation
- Precision: Not applicable as a prediction-model evaluation
- Recall: Not applicable as a prediction-model evaluation
- F1-score: Not applicable as a prediction-model evaluation
- ROC-AUC: Not reported as a prediction-model evaluation
- PR-AUC: Not reported
- Calibration: Not a prediction-model evaluation component
- SHAP/explainable ML: No

### Verification Checklist

- [x] Original paper located
- [x] Full text reviewed
- [x] Correct authors verified
- [x] Correct journal verified
- [x] Publication year verified
- [x] DOI verified
- [x] NDHS survey rounds verified
- [x] Outcome definition verified
- [x] SBA prevalence figures verified
- [x] Methods verified
- [x] Survey weighting verified
- [x] Survey-design adjustment verified
- [x] Education result verified
- [x] Healthcare decision-making result verified
- [x] Variables examined verified
- [x] Limitations reviewed
- [x] Full citation verified

### Full Citation

Fagbamigbe, A. F., Hurricane-Ike, E. O., Yusuf, O. B., & Idemudia, E. S. (2017). Trends and drivers of skilled birth attendant use in Nigeria (1990–2013): Policy implications for child and maternal health. International Journal of Women's Health, 9, 843–853.

### DOI / Original Publication

https://doi.org/10.2147/IJWH.S137848
---
## Study 11: Negash and Wubneh (2025)

### Paper Title

Skilled Birth Attendance and Its Associated Factors in Chad and Nigeria: A Multilevel Analysis of DHS Data

### Publication Status

Peer-reviewed research article published in PLOS Global Public Health.

### Source Reviewed

Full text reviewed.

### Country / Study Setting

Chad and Nigeria.

### Dataset

The study used Demographic and Health Survey (DHS) data from:

- Chad DHS 2014–15
- Nigeria DHS 2018

The researchers used the Kids Recode (KR) datasets.

The analysis included a total weighted sample of 52,666 reproductive-age women.

The study therefore did not use the 2023–24 Nigeria DHS.

### Purpose of the Study

The study aimed to determine the prevalence of skilled birth attendance and identify individual-level and community-level factors associated with skilled birth attendance in Chad and Nigeria.

The researchers used a multilevel approach because women living within the same communities may share characteristics and healthcare environments that influence maternal healthcare utilisation.

### Methods Used

The researchers conducted a secondary analysis of DHS data using Stata version 17.

They used mixed-effects binary logistic regression to account for the hierarchical structure of the DHS data.

DHS primary sampling units (PSUs) were treated as community-level clusters.

The analysis examined both individual-level and community-level characteristics.

Individual-level characteristics examined included:

- Maternal age
- Maternal education
- Household wealth
- Marital status
- Antenatal care visits
- Media exposure
- Pregnancy wantedness

Community-level characteristics examined included:

- Urban/rural residence
- Distance to a health facility
- Community-level education
- Community-level media exposure
- Community-level poverty

Adjusted odds ratios with 95% confidence intervals were used to identify factors associated with skilled birth attendance.

The researchers also assessed variation between communities and compared the fit of different multilevel models.

### Main Findings

The overall prevalence of skilled birth attendance across Chad and Nigeria was 41.9%.

Several individual-level and community-level characteristics were significantly associated with skilled birth attendance.

Women with a history of antenatal care visits had substantially higher odds of skilled birth attendance:

- ANC visits: AOR = 5.56
- 95% CI: 5.03–6.14

Maternal education was also important:

- Primary education: AOR = 1.77
- Secondary or higher education: AOR = 4.06

Household wealth was associated with skilled birth attendance:

- Middle wealth category: AOR = 1.37
- Rich wealth category: AOR = 2.11
- 95% CI for rich wealth category: 1.87–2.38

Women exposed to media had higher odds of skilled birth attendance:

- Media exposure: AOR = 1.50

Community-level education was also strongly associated with skilled birth attendance:

- High community-level education: AOR = 2.73

Place of residence and distance to a health facility were also identified as important factors.

The study found substantial variation between communities.

The intra-class correlation coefficient (ICC) in the null model was 61%, indicating that a considerable proportion of the variation in skilled birth attendance was attributable to differences between communities.

#### Important Reporting Inconsistency

The article contains an apparent reporting inconsistency for the rich wealth category.

The abstract reports an AOR of 2.77 but gives a 95% confidence interval of 1.87–2.38. This confidence interval does not contain 2.77.

Table 3 and the main Results section report:

- AOR = 2.11
- 95% CI: 1.87–2.38

Therefore, these literature notes use the Table 3 and Results value of 2.11 while recording the discrepancy in the abstract.

### My Understanding

In simple terms, the researchers wanted to understand why some women in Chad and Nigeria received skilled assistance during childbirth while others did not.

They did not look only at the characteristics of individual women. They also considered characteristics of the communities in which the women lived.

The study found that antenatal care was strongly associated with skilled birth attendance.

Education, household wealth and media exposure were also important.

Community characteristics mattered as well. For example, women living in communities with higher levels of education were more likely to receive skilled birth attendance.

The large amount of variation between communities also helped me understand that maternal healthcare use may depend not only on a woman's personal circumstances but also on the environment in which she lives.

### Relevance to My Research

This study is highly relevant to my research because Nigeria was included, DHS data were used, and the outcome was skilled birth attendance.

It provides evidence that both individual-level and community-level characteristics should be considered when studying skilled birth attendance.

Several characteristics identified in the study could potentially provide useful pre-delivery information, including:

- Maternal education
- Household wealth
- Antenatal care
- Media exposure
- Residence
- Distance to healthcare
- Community-level education

The study also reinforces the importance of considering the clustered structure of DHS data.

This is relevant to my research because women in the NDHS are sampled within geographical clusters, and observations from women in the same community may not be completely independent.

### Differences From My Research

The study combined data from Chad and Nigeria rather than developing a Nigeria-only analysis.

It used:

- Chad DHS 2014–15
- Nigeria DHS 2018

My proposed research will focus specifically on Nigeria using the newer 2023–24 NDHS.

The study focused primarily on identifying statistical associations using mixed-effects logistic regression.

My proposed research will focus on predicting non-use of skilled birth attendance using information that could reasonably be available before childbirth.

I also intend to compare predictive models, evaluate discrimination and calibration, use explainability methods, and investigate model performance across important geographical and socioeconomic groups.

Therefore, this study mainly asks:

"Which individual and community characteristics are associated with skilled birth attendance in Chad and Nigeria?"

My research asks:

"How well can information available before childbirth predict non-use of skilled birth attendance in Nigeria using the 2023–24 NDHS?"

### Predictor-Timing Considerations

Several characteristics examined in the study could potentially be known before childbirth, including:

- Maternal age
- Maternal education
- Household wealth
- Marital status
- Media exposure
- Residence
- Distance to a health facility
- Community-level education
- Community-level poverty

Antenatal care requires more careful consideration.

ANC occurs before childbirth, but the amount of ANC information available depends on the point during pregnancy when a prediction is made.

For example, a final count or history of ANC visits may not yet be available if the model is intended to make predictions earlier in pregnancy.

Therefore, the exact ANC variable will need to be checked against my chosen prediction point before it is included in the model.

### Survey-Design and Clustering Considerations

An important contribution of this study is its treatment of the hierarchical structure of DHS data.

Women were nested within DHS clusters or communities.

The researchers therefore used mixed-effects logistic regression rather than treating all observations as completely independent.

The null-model ICC of 61% indicated substantial clustering at the community level.

This is particularly relevant to my proposed research because it demonstrates that geographical clustering can be important when analysing skilled birth attendance using DHS data.

For my machine-learning study, I will need to determine how survey weights, geographical clusters and validation should be handled so that model performance is assessed appropriately.

### Limitations / Research Gap Identified

The study used cross-sectional DHS data, so the identified relationships should not automatically be interpreted as causal.

Some DHS information is self-reported and may therefore be affected by recall or reporting bias.

The study combined Chad and Nigeria, meaning that the reported findings do not represent a Nigeria-specific prediction model.

The Nigeria component used the 2018 NDHS rather than the newer 2023–24 NDHS.

The study focused on statistical associations rather than developing and comparing machine-learning prediction models.

It also did not evaluate predictive performance using measures such as:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- PR-AUC
- Probability calibration

These measures were not required for the study's explanatory objective.

For my research, predictor timing remains important.

Although antenatal care occurs before delivery, the exact ANC information used must still be checked against my chosen prediction point to ensure that the information would genuinely have been available when the prediction is intended to be made.

### Important Variables / Factors Identified

Important factors associated with skilled birth attendance included:

- Antenatal care visits
- Maternal education
- Household wealth
- Media exposure
- Urban/rural residence
- Distance to a health facility
- Community-level education

Other characteristics considered included:

- Maternal age
- Marital status
- Pregnancy wantedness
- Community-level media exposure
- Community-level poverty

### Pre-Delivery Variables Only?

The study was not specifically designed as a pre-delivery prediction study.

However, several characteristics could potentially be known before childbirth, including:

- Maternal education
- Household wealth
- Residence
- Media exposure
- Distance to healthcare
- Community-level education
- Maternal age
- Marital status

Antenatal care could also represent pre-delivery information, but its suitability depends on the exact prediction point used in my research.

Therefore, each candidate predictor will need to be checked carefully against the 2023–24 NDHS documentation and my defined prediction point before inclusion in the prediction model.

### Model Evaluation

This was not primarily a machine-learning prediction study.

- Countries: Chad and Nigeria
- DHS surveys: Chad 2014–15 and Nigeria 2018
- Dataset type: Kids Recode (KR)
- Weighted sample: 52,666
- Outcome: Skilled birth attendance
- Overall SBA prevalence: 41.9%
- Main analytical method: Mixed-effects binary logistic regression
- Individual-level factors examined: Yes
- Community-level factors examined: Yes
- Community clustering assessed: Yes
- Intra-class correlation coefficient (null model): 61%
- Model fit assessment: Deviance (-2 log likelihood)
- ANC visits AOR: 5.56
- ANC visits 95% CI: 5.03–6.14
- Rich wealth AOR used: 2.11
- Rich wealth 95% CI: 1.87–2.38
- Machine-learning model comparison: No
- Accuracy: Not applicable as a prediction-model evaluation
- Precision: Not applicable as a prediction-model evaluation
- Recall: Not applicable as a prediction-model evaluation
- F1-score: Not applicable as a prediction-model evaluation
- ROC-AUC: Not reported as a prediction-model evaluation
- PR-AUC: Not reported
- Calibration: Not reported as a prediction-model evaluation
- SHAP/explainable ML: No

### Verification Checklist

- [x] Original paper located
- [x] Full text reviewed
- [x] Authors verified
- [x] Publication details verified
- [x] DOI verified
- [x] Countries verified
- [x] DHS survey years verified
- [x] Dataset type verified
- [x] Weighted sample size verified
- [x] Outcome verified
- [x] Methods verified
- [x] Overall SBA prevalence verified
- [x] ANC result verified
- [x] Education results verified
- [x] Wealth results verified
- [x] Abstract/Table 3 wealth inconsistency documented
- [x] Individual-level factors reviewed
- [x] Community-level factors reviewed
- [x] ICC verified
- [x] Model-fit approach verified
- [x] Limitations reviewed
- [x] Full citation verified

### Full Citation

Negash, W. D., & Wubneh, H. D. (2025). Skilled birth attendance and its associated factors in Chad and Nigeria: A multilevel analysis of DHS data. PLOS Global Public Health, 5(12), e0005290.

### DOI / Original Publication

https://doi.org/10.1371/journal.pgph.0005290
---
## Study 12: Akpiroroh et al. (2026)

### Paper Title

Hierarchical Logistic Regression Analysis of Skilled Birth Attendance in Northern Nigeria Using Andersen’s Behavioural Model

### Publication Status

Peer-reviewed research article published in Discover Public Health.

### Source Reviewed

Full text reviewed.

### Country / Study Setting

Northern Nigeria.

The study was conducted across six northern Nigerian states:

- Jigawa
- Bauchi
- Niger
- Katsina
- Kaduna
- Kano

### Dataset

Unlike many of the other studies reviewed in this project, this study did not use DHS data.

The researchers collected primary survey data in July 2025 using a pretested interviewer-administered questionnaire.

The study included 1,004 women aged 15–49 years who had delivered within the five years preceding the survey.

Women were recruited from rural and urban communities across the six selected northern Nigerian states.

The researchers used purposive and quota sampling rather than a nationally representative probability sample.

To reduce recall bias, the analysis focused on respondents' most recent birth.

### Purpose of the Study

The study aimed to examine factors associated with skilled birth service utilisation among women of reproductive age in Northern Nigeria.

The researchers investigated two related but distinct outcomes:

1. Skilled birth attendance
2. Place of delivery

Skilled birth attendance was defined as childbirth assisted by a trained health professional, regardless of where the delivery occurred.

Place of delivery was examined separately as health-facility delivery versus home delivery.

The researchers used Andersen’s Behavioural Model of Health Service Use to organise factors that could influence maternal healthcare utilisation.

### Methods Used

The study used a community-based cross-sectional analytical design.

Bivariate associations were examined using Pearson's chi-square tests.

Hierarchical logistic regression was then used to examine factors associated with skilled birth attendance and place of delivery.

The hierarchical analysis was guided by Andersen’s Behavioural Model of Health Service Use.

The explanatory characteristics were organised into three conceptual groups:

1. Predisposing factors
2. Enabling factors
3. Need factors

The groups were entered into the regression models sequentially to determine how much additional explanatory information each group contributed.

The researchers used:

- IBM SPSS 27 for descriptive statistics
- Stata 17 for inferential analyses

### Predisposing Factors

Predisposing characteristics included:

- Maternal age
- Marital status
- Education
- Religion
- Place of residence
- Year of last birth

These represent background characteristics that may influence a woman's tendency to use healthcare services.

### Enabling Factors

Enabling characteristics included factors such as:

- Women's occupation
- Personal income
- Household income
- Partner's education
- Partner's occupation/employment
- Family support
- Transportation
- Phone ownership
- Previous/last place of birth
- Other healthcare-access characteristics

These represent resources or circumstances that may make healthcare easier or more difficult to access.

### Need Factors

Need-related characteristics included:

- Antenatal care attendance
- Number of ANC visits
- Satisfaction with ANC
- Delivery complications
- Newborn complications

These represent pregnancy-related healthcare needs and experiences.

### Main Findings

Overall:

- 72.8% of women reported receiving skilled birth assistance.
- 27.2% did not report receiving skilled birth assistance.

At the bivariate level, phone ownership and ANC satisfaction were significantly associated with healthcare delivery assistance.

However, these associations were no longer statistically significant after adjustment for other characteristics.

In the hierarchical regression analysis, partner's education and last place of birth remained significantly associated with healthcare delivery assistance after adjustment.

The addition of enabling factors produced a substantial improvement in the explanatory performance of the skilled-birth-attendance model.

This suggests that household resources, partner characteristics and access-related factors contributed substantial explanatory information beyond women's basic sociodemographic characteristics.

For place of delivery, several characteristics showed associations before adjustment, including:

- Education
- Year of last delivery
- Partner's employment
- Settlement type
- Mode of transportation
- Phone ownership

After adjustment, year of last delivery and phone ownership remained statistically associated with place of delivery.

### Hierarchical Model Findings

The study fitted three nested logistic regression models for healthcare delivery assistance.

#### Model 1

Predisposing characteristics were entered first.

#### Model 2

Enabling characteristics were added.

#### Model 3

Need-related characteristics were then added.

Model fit improved substantially after enabling factors were introduced.

The paper reports that enabling factors accounted for most of the improvement in model fit, while need-related factors contributed comparatively little after enabling characteristics had already been considered.

This suggests that access, household resources and partner-related characteristics may play an important role in explaining skilled birth service utilisation in this sample.

### My Understanding

In simple terms, the researchers wanted to understand why some women in Northern Nigeria received skilled assistance during childbirth while others did not.

Instead of putting all possible factors into the analysis without any structure, they organised the factors into three groups.

Predisposing factors describe a woman's background.

Enabling factors describe resources and circumstances that can make healthcare easier or harder to access.

Need factors describe pregnancy-related healthcare needs and experiences.

The researchers then added these groups to the statistical model step by step.

One important thing I learned from this paper is that a factor can appear important when examined by itself but become less important after other characteristics are considered.

For example, phone ownership and ANC satisfaction were associated with skilled assistance in the initial analysis, but these associations did not remain statistically significant after adjustment.

Another important finding was that adding enabling factors substantially improved the model.

This suggests that resources, partner characteristics and healthcare-access conditions may provide important information beyond a woman's basic demographic characteristics.

### Relevance to My Research

This study is relevant to my research because it is a recent Nigeria-specific study examining skilled birth attendance.

It is particularly useful because it focuses on Northern Nigeria, an area where maternal healthcare utilisation remains an important concern.

The study also provides a useful theoretical framework for thinking about potential predictors.

Rather than selecting variables simply because they are available, Andersen's Behavioural Model demonstrates how maternal-health characteristics can be organised into meaningful groups:

- Predisposing characteristics
- Enabling/access characteristics
- Need-related characteristics

This framework may help me organise and justify candidate predictors when developing my data dictionary.

The study also reinforces the importance of distinguishing skilled birth attendance from place of delivery.

A woman can theoretically deliver outside a health facility and still receive assistance from a skilled provider.

Therefore, place of delivery and skilled birth attendance are related but are not identical outcomes.

### Differences From My Research

This study did not use the Nigeria DHS.

It collected primary survey data from 1,004 women in six northern Nigerian states.

My proposed research will use the nationally representative 2023–24 Nigeria DHS.

The study was limited to selected states in Northern Nigeria, whereas my proposed research will examine Nigeria nationally.

The researchers primarily used hierarchical logistic regression to investigate statistical associations.

My research will focus on predicting non-use of skilled birth attendance using information available before childbirth.

I intend to compare predictive models, evaluate discrimination and calibration, use explainability methods, and investigate model performance across important geographical and socioeconomic groups.

### Important Predictor-Timing Issue

This paper raises a particularly important issue for my proposed research.

The hierarchical model included last place of birth as an explanatory characteristic, and this variable showed a very strong association with healthcare delivery assistance.

However, I should not automatically treat this as a valid pre-delivery predictor.

Its suitability depends on exactly which birth the variable represents.

If it genuinely refers to a delivery that occurred before the index birth being predicted, it could potentially represent valid maternal history.

However, if it refers to the same most recent delivery for which skilled attendance is being analysed, it would contain information from the delivery itself and would not be appropriate for a prospective pre-delivery prediction model.

Therefore, the timing and definition of this variable must be treated cautiously.

I will not copy it directly into my prediction model.

Every candidate predictor in the 2023–24 NDHS will be checked against the survey documentation to establish exactly what it measures and whether that information would have been available at my defined prediction point.

### Other Variables With Timing Concerns

Delivery complications and newborn complications present clearer timing problems.

These events occur during or after childbirth.

Therefore, they would generally not be appropriate predictors for a model intended to identify women at risk of non-use of skilled birth attendance before childbirth.

ANC variables require a different type of timing check.

ANC occurs before delivery, but the amount of ANC information available depends on when during pregnancy the prediction is intended to be made.

For example, the final number of ANC visits cannot be known early in pregnancy.

This reinforces the need for my project to define a clear prediction point before final predictor selection.

### Limitations / Research Gap Identified

The study used a cross-sectional design, so the reported relationships should be interpreted as associations rather than causal effects.

The researchers used purposive and quota sampling rather than a nationally representative probability sample.

The study was conducted in six selected northern states and therefore should not automatically be generalised to all Nigerian women.

The sample of 1,004 women was also substantially smaller than nationally representative NDHS samples used in several other studies in this literature review.

The study focused primarily on explanatory associations rather than predictive machine-learning performance.

It did not develop or evaluate a national prediction model using the 2023–24 NDHS.

Some variables also raise important predictor-timing concerns for prospective prediction, particularly:

- Last place of birth
- Delivery complications
- Newborn complications
- Final ANC information

For my research, this paper is therefore most useful for understanding recent Northern Nigerian evidence, distinguishing SBA from facility delivery, and providing a theoretical framework for organising potential predictors.

### Important Variables / Factors Examined

Important characteristics examined included:

- Maternal age
- Education
- Marital status
- Religion
- Place of residence
- Income
- Partner's education
- Partner's employment
- Phone ownership
- Transportation
- Family support
- Antenatal care
- ANC satisfaction
- Last/previous place of birth
- Delivery complications
- Newborn complications

### Pre-Delivery Variables Only?

No.

The study was not specifically designed to create a prediction model using only information available before the delivery being predicted.

Several characteristics could potentially represent pre-delivery information, including:

- Maternal age
- Education
- Religion
- Residence
- Income
- Partner's education
- Partner's employment
- Phone ownership
- Transportation
- Family support
- Some antenatal-care information

However, several variables require particular caution.

Delivery complications and newborn complications would generally not be appropriate for a model intended to make predictions before childbirth.

Last place of birth may or may not be appropriate depending on whether it genuinely refers to an earlier delivery or the index delivery.

Final ANC information may also introduce future information if the prediction point occurs before those ANC visits have taken place.

Therefore, predictor timing will need to be verified carefully in my proposed research.

### Model Evaluation

This was not primarily a machine-learning prediction study.

- Country: Nigeria
- Study area: Six northern Nigerian states
- Data source: Primary survey
- Data collection: July 2025
- Sample: 1,004 women aged 15–49
- Main analytical method: Hierarchical logistic regression
- Theoretical framework: Andersen's Behavioural Model of Health Service Use
- SBA prevalence: 72.8%
- Non-SBA: 27.2%
- Predisposing factors examined: Yes
- Enabling factors examined: Yes
- Need factors examined: Yes
- Bivariate analysis: Pearson's chi-square
- Descriptive software: IBM SPSS 27
- Inferential software: Stata 17
- Machine-learning model comparison: No
- Accuracy: Not reported as a prediction-model evaluation
- Precision: Not reported as a prediction-model evaluation
- Recall: Not reported as a prediction-model evaluation
- F1-score: Not reported as a prediction-model evaluation
- ROC-AUC: Not reported as a prediction-model evaluation
- PR-AUC: Not reported
- Calibration: Not reported as a prediction-model evaluation
- SHAP/explainable ML: No
- Main focus: Factors associated with skilled birth attendance and place of delivery

### Verification Checklist

- [x] Original paper located
- [x] Full text reviewed
- [x] Authors verified
- [x] Publication status verified
- [x] Publication date verified
- [x] DOI verified
- [x] Study location verified
- [x] Six study states verified
- [x] Sample size verified
- [x] Data-collection period verified
- [x] Sampling approach verified
- [x] Outcome definitions verified
- [x] SBA prevalence verified
- [x] Methods verified
- [x] Andersen framework verified
- [x] Hierarchical modelling approach verified
- [x] Main findings verified
- [x] Predictor-timing concerns documented
- [x] Limitations reviewed
- [x] Full citation verified

### Full Citation

Akpiroroh, E., Ebinim, H., Ajayi, M., Sabbath, U.-O., Jibril, J., Ehize, P., Ogunsanya, A., Unogu, C., Kolawole, D., Nto, S., Rauf, R., Ajibola, D., Atobatele, S., Sampson, S., & Okagbue, H. (2026). Hierarchical logistic regression analysis of skilled birth attendance in Northern Nigeria using Andersen's Behavioural Model. Discover Public Health, 23, 1512.

### DOI / Original Publication

https://doi.org/10.1186/s12982-026-02943-6
---


## Cross-Study Summary

The 12 studies reviewed provide a broad picture of what is already known about skilled birth attendance in Nigeria and related maternal healthcare prediction.

### Overall Evidence

The studies consistently show that skilled birth attendance is influenced by a combination of individual, household, healthcare-access, geographical and community characteristics.

Factors that appeared repeatedly across the literature included:

- Maternal education
- Household wealth
- Urban/rural residence
- Geographical region
- Antenatal care
- Healthcare accessibility
- Media exposure
- Maternal age
- Birth order or parity
- Women's healthcare decision-making and autonomy
- Partner and household characteristics
- Community-level socioeconomic characteristics

This suggests that non-use of skilled birth attendance is not explained by one factor alone. It is associated with several characteristics operating at different levels.

### Nigeria-Specific Evidence

Several of the reviewed studies focused specifically on Nigeria and used Nigeria Demographic and Health Survey data.

These studies showed persistent socioeconomic and geographical differences in skilled birth attendance.

Education, wealth, residence, region, healthcare access and women's decision-making appeared repeatedly as important factors.

However, much of the Nigeria-specific literature focused on identifying factors statistically associated with skilled birth attendance rather than developing models specifically designed to predict which women may not use skilled birth attendance.

Several studies also relied on older NDHS rounds, including the 2013 and 2018 surveys.

This provides useful historical evidence but also supports the need to investigate patterns using the newer 2023–24 Nigeria DHS.

### Evidence From Machine-Learning Studies

The reviewed machine-learning studies demonstrate that DHS data can be used to develop predictive models for maternal healthcare outcomes, including skilled birth attendance.

Methods used across the machine-learning literature included approaches such as:

- Random Forest
- XGBoost
- LightGBM
- Logistic regression
- Feature-selection techniques
- Class-imbalance methods
- SHAP for model interpretation

Some studies reported strong predictive performance.

However, high predictive performance alone does not mean that a model is appropriate for use before childbirth.

The timing of the predictors used to obtain that performance is also important.

### Predictor Timing and Data Leakage

One of the most important issues identified during this review was predictor timing.

My proposed research aims to predict non-use of skilled birth attendance using information that could reasonably be available before the delivery being predicted.

However, some previous studies included variables that may be known only at delivery, after delivery, or later in pregnancy.

Examples requiring particular caution include:

- Actual place of delivery
- Delivery complications
- Newborn complications
- Final number of antenatal care visits
- Some variables describing previous or last place of birth

For example, a place-of-delivery variable referring to the same delivery being predicted would not be suitable for a pre-delivery prediction model because that information would not yet be known.

Similarly, delivery and newborn complications occur during or after childbirth.

Antenatal care is different because it occurs before childbirth, but its suitability depends on the prediction point. A final ANC count cannot be used if the prediction is intended to occur before all those visits have taken place.

Therefore, every candidate predictor in my research will need to be checked against a clearly defined prediction point.

This will help prevent data leakage and ensure that the model reflects a realistic pre-delivery prediction setting.

### Association Versus Prediction

Another important distinction across the literature is the difference between explanatory and predictive research.

Many of the Nigeria-specific studies used logistic regression or multilevel regression to determine which characteristics were associated with skilled birth attendance.

These studies are valuable because they help identify potentially important factors.

However, identifying an association is not the same as demonstrating that a model can accurately predict future outcomes for individual women.

My proposed research will therefore build on the explanatory evidence while focusing specifically on predictive performance.

### Community and Geographical Effects

Several studies showed that skilled birth attendance varies across geographical areas and communities.

Multilevel studies found that women living within the same communities may share characteristics and healthcare environments that influence maternal healthcare utilisation.

This is particularly important because NDHS observations are collected within geographical clusters.

Therefore, my research should not automatically treat every observation as completely independent.

The survey structure, geographical clustering and validation strategy will need to be considered carefully when developing and evaluating the prediction models.

### Model Evaluation and Calibration

The review also showed that prediction-model evaluation should not rely only on accuracy.

Depending on the study, machine-learning performance was assessed using measures such as:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- PR-AUC

For my research, identifying women who may not use skilled birth attendance is particularly important.

Therefore, model evaluation should consider how well the model identifies the non-SBA group rather than focusing only on overall accuracy.

Calibration is also important.

Discrimination measures such as ROC-AUC show how well a model separates higher-risk from lower-risk individuals, while calibration examines whether predicted probabilities correspond reasonably well with observed outcomes.

The reviewed literature showed that calibration has not been handled consistently across prediction studies.

Therefore, my research should evaluate both discrimination and calibration rather than relying on a single performance measure.

### Explainability

Some of the machine-learning studies used SHAP to explain model predictions and identify influential predictors.

This is useful for my proposed research because a prediction model should not operate only as a black box.

Explainability methods can help show which characteristics contribute most strongly to model predictions.

However, predictive importance should not automatically be interpreted as evidence that a variable causes non-use of skilled birth attendance.

### Subgroup Performance

The reviewed studies repeatedly identified differences in skilled birth attendance according to characteristics such as:

- Geographical region
- Urban/rural residence
- Household wealth
- Education
- Healthcare accessibility

This means that strong overall model performance may hide weaker performance within particular population groups.

My proposed research should therefore investigate model performance across important geographical and socioeconomic groups where sample sizes permit.

This will help determine whether the model performs consistently across different parts of the Nigerian population.

### Evidence From the 2023–24 NDHS

The literature review identified recent machine-learning research using newer Nigeria DHS data for maternal-health outcomes.

Therefore, my research should not claim that machine learning has never been applied to recent Nigeria DHS data.

Instead, the important question is whether the specific combination proposed in my research has been adequately addressed:

- Nigeria-specific analysis
- 2023–24 NDHS
- Non-use of skilled birth attendance as the prediction target
- Predictors selected according to a clearly defined pre-delivery prediction point
- Comparison of predictive models
- Evaluation of discrimination and calibration
- Explainability
- Consideration of geographical and socioeconomic subgroup performance
- Appropriate consideration of the clustered survey structure

### Overall Conclusion From the 12 Studies

The reviewed literature provides strong evidence that skilled birth attendance in Nigeria is related to socioeconomic, geographical, healthcare-access, maternal and community characteristics.

Previous research has made important contributions by identifying factors associated with skilled birth attendance and demonstrating that machine-learning methods can be applied to DHS maternal-health data.

However, the review also identified important methodological issues concerning predictor timing, data leakage, model validation, calibration, geographical clustering and subgroup performance.

These findings provide the foundation for my proposed study.

Rather than simply asking which characteristics are associated with skilled birth attendance, my research will investigate whether women at risk of non-use of skilled birth attendance can be identified using information that would realistically be available before childbirth.

The study will use the 2023–24 Nigeria DHS and will place particular emphasis on careful predictor selection, appropriate model evaluation, explainability and assessment of model performance across important population groups.

---

---

## Research Gap

The reviewed studies show that skilled birth attendance in Nigeria has been widely investigated, particularly in relation to maternal education, household wealth, residence, geographical region, antenatal care, healthcare access, media exposure, women's decision-making and community characteristics.

However, much of the Nigeria-specific research has focused on identifying factors associated with skilled birth attendance using statistical methods such as logistic regression and multilevel regression. These studies are useful for understanding relationships, but they were not primarily designed to predict which women are at risk of not using skilled birth attendance.

Machine-learning studies have shown that DHS data can be used to predict skilled birth attendance and other maternal-health outcomes. However, the literature review identified an important issue concerning predictor timing. Some previous studies used variables such as actual place of delivery or other information that may only be completely known at delivery or afterwards. Such variables would not be appropriate for a model intended to identify women at risk before childbirth.

Antenatal-care information also requires careful consideration. Although ANC occurs before childbirth, information such as the final number of ANC visits may not yet be known if prediction is intended to take place earlier in pregnancy. Therefore, a clear prediction point is needed to determine which information can legitimately be used.

The reviewed literature also shows that predictive performance should not be assessed using accuracy alone. Discrimination, class-specific performance and calibration are important when predicted probabilities may be used to identify women at elevated risk. In addition, the clustered structure of DHS data and differences in skilled birth attendance across geographical and socioeconomic groups suggest that validation strategy and subgroup performance require careful attention.

Recent machine-learning research has used newer Nigeria DHS data for maternal-health outcomes. Therefore, this study will not claim that machine learning has never been applied to recent NDHS data. Instead, the gap identified from the reviewed literature concerns the specific combination of outcome, prediction timing, dataset and evaluation approach proposed in this research.

Among the studies reviewed, limited evidence was identified of a Nigeria-specific prediction study using the 2023–24 Nigeria DHS to predict **non-use of skilled birth attendance** while restricting the primary model to information that would reasonably be available at a clearly defined point before the delivery being predicted.

This study therefore proposes to investigate whether non-use of skilled birth attendance can be predicted using the 2023–24 Nigeria DHS and carefully selected pre-delivery information. The study will compare appropriate predictive models, assess discrimination and calibration, use explainability methods to understand influential predictors, and examine model performance across important geographical and socioeconomic groups where sample sizes permit.

The study will also consider the complex and clustered structure of the NDHS when developing its validation and analytical strategy.

### How My Research Addresses the Gap

My proposed research will address the identified gap by:

- Focusing specifically on **non-use of skilled birth attendance in Nigeria**.
- Using the **2023–24 Nigeria Demographic and Health Survey**.
- Defining a clear **pre-delivery prediction point** before final predictor selection.
- Excluding variables that would not realistically be known at that prediction point.
- Comparing an interpretable baseline model with appropriate machine-learning models.
- Evaluating performance using more than overall accuracy.
- Assessing discrimination using measures such as ROC-AUC and PR-AUC.
- Evaluating precision, recall and F1-score, with particular attention to the non-SBA group.
- Assessing the calibration of predicted probabilities.
- Using explainability methods, where appropriate, to understand influential predictors.
- Considering the clustered structure of the NDHS during model development and validation.
- Examining performance across important geographical and socioeconomic groups where sufficient data are available.

### Research Contribution

The main contribution of this research is therefore not simply the use of machine learning.

Its contribution is the development and evaluation of a prediction approach that is designed around a realistic **pre-delivery decision point**.

By ensuring that the primary model uses only information that could reasonably be available before the childbirth outcome occurs, the study aims to produce a more realistic assessment of whether women at risk of non-use of skilled birth attendance can be identified in advance.

The study will also provide updated evidence using the 2023–24 NDHS and assess not only whether the models can distinguish between women at different levels of risk, but also whether their predicted probabilities are reliable and whether performance is reasonably consistent across important population groups.

---


## Review Progress

- [x] Study 1
- [x] Study 2
- [x] Study 3
- [x] Study 4
- [x] Study 5
- [x] Study 6
- [x] Study 7
- [x] Study 8
- [x] Study 9
- [x] Study 10
- [x] Study 11
- [x] Study 12
- [x] Cross-study audit completed
- [x] Preliminary research gap identified
