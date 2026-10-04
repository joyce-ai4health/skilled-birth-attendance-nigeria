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

### Country / Study Setting

27 Sub-Saharan African countries, including Nigeria.

### Dataset

Demographic and Health Survey (DHS) data from surveys conducted between 2016 and 2024.

The study included a weighted sample of 198,707 reproductive-age women who had at least one live birth.

### Purpose of the Study

The study aimed to use machine learning to predict skilled birth attendance among women in 27 Sub-Saharan African countries and identify the factors that were most important in predicting skilled birth attendance.

### Methods Used

The researchers used a Random Forest classifier as the machine-learning model.

SHAP was used to help explain the model predictions and identify important predictors.

The researchers also used:

- K-nearest-neighbour imputation to handle missing values.
- SMOTE to address class imbalance.
- Recursive Feature Elimination for feature selection.

### Main Findings

The Random Forest model showed strong predictive performance.

The abstract reported:

- ROC-AUC: 92%
- Recall: 96%
- Accuracy: 92%
- Precision: 93%
- F1-score: 93%

Important predictors identified using SHAP included facility delivery, maternal education, household wealth, urban residence, healthcare accessibility, media exposure and internet use.

### My Understanding

In simple terms, the researchers used information about women from DHS surveys to train a machine-learning model to recognise patterns associated with skilled birth attendance.

The Random Forest model was able to distinguish women who received skilled birth attendance from those who did not with strong reported performance.

SHAP was then used to understand which characteristics contributed most to the model's predictions.

The study shows that machine learning can be used with DHS data to investigate skilled birth attendance.

### Relevance to My Research

This study is highly relevant to my research because it investigates the same general outcome, skilled birth attendance, and uses DHS data and machine-learning methods.

Nigeria was also included among the 27 countries.

The study provides evidence that Random Forest and explainable machine-learning methods such as SHAP can be applied to skilled birth attendance research.

### Differences From My Research

The study combined data from 27 Sub-Saharan African countries rather than focusing specifically on Nigeria.

My proposed study will focus on Nigeria using the 2023–24 Nigeria DHS.

Another important difference is the timing of the predictors. Facility delivery was identified as an important predictor in the study. My research intends to focus on predictors that could reasonably be known before childbirth. Therefore, variables such as the actual place of delivery will not be used as predictors in the main pre-delivery prediction model.

### Limitations / Research Gap Identified

The authors reported several limitations:

- The study relied on self-reported DHS data, which may be affected by response bias.
- The cross-sectional design limits causal interpretation.
- Survey years differed across the 27 countries.
- The absence of some localised factors may limit applicability to specific groups.

For my research, an additional important consideration is that the model included facility delivery as a predictor. This does not match my intended pre-delivery prediction setting because the actual place of delivery would not be known before childbirth.

The multi-country design also means that the study does not provide a Nigeria-specific model based solely on the latest Nigeria DHS.

### Important Variables Identified

Important predictors included:

- Facility delivery
- Maternal education
- Wealth index
- Urban/rural residence
- Distance/access to healthcare
- Media exposure
- Internet use

### Pre-Delivery Variables Only?

No.

Facility delivery is not a pre-delivery variable because the actual place where the woman gives birth is known at or after delivery.

Several other identified variables, such as education, wealth, residence and healthcare-access characteristics, could potentially be available before delivery.

### Model Evaluation

- Accuracy: 92%
- Precision: 93%
- Recall: 96%
- F1-score: 93% in the abstract and conclusion
- ROC-AUC: 92%
- PR-AUC: Not reported in the abstract
- Calibration: Not reported in the abstract
- Explainability: SHAP
- Main model: Random Forest

Note: The discussion section reports an F1-score of 94%, while the abstract and conclusion report 93%. This inconsistency should be kept in mind when citing the model performance.

### Verification Checklist

- [x] Original paper located
- [x] Abstract reviewed
- [x] Dataset and sample verified
- [x] Methods verified
- [x] Results verified
- [x] Limitations reviewed
- [x] Full citation verified

### Full Citation

Taye, E. A., Woubet, E. Y., Hailie, G. Y., Arage, F. G., Zerihun, T. E., Zegeye, A. T., Zeleke, T. C., & Kassaw, A. T. (2025). Application of the random forest algorithm to predict skilled birth attendance and identify determinants among reproductive-age women in 27 Sub-Saharan African countries: Machine learning analysis. BMC Public Health, 25, 901. https://doi.org/10.1186/s12889-025-22007-9

### DOI / Original Publication

https://doi.org/10.1186/s12889-025-22007-9

## Review Progress

- [x] Study 1
- [ ] Study 2
- [ ] Study 3
- [ ] Study 4
- [ ] Study 5
- [ ] Study 6
- [ ] Study 7
- [ ] Study 8
- [ ] Study 9
- [ ] Study 10
- [ ] Study 11
- [ ] Study 12
