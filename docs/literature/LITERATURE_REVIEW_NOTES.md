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


## Study 2: Memon, Wamala and Kabano (2025)

### Paper Title

Identifying Predictors of Utilization of Skilled Birth Attendance in Uganda Through Interpretable Machine Learning

### Country / Study Setting

Uganda.

### Dataset

The study used data from the 2016 Uganda Demographic and Health Survey (UDHS).

The analysis focused on women aged 15–49 who had given birth within the five years preceding the survey.

### Purpose of the Study

The study aimed to determine whether machine-learning models could predict the use of skilled birth attendance among women in Uganda.

The researchers also wanted to identify and explain the factors that were most important in predicting whether a woman would use skilled birth attendance.

### Methods Used

The researchers compared seven machine-learning models:

- Logistic Regression
- Decision Tree
- Random Forest
- Gradient Boosting
- XGBoost
- LightGBM
- CatBoost

The data were divided into 80% training data and 20% testing data.

The researchers also used 5-fold cross-validation during hyperparameter tuning.

Because fewer women belonged to the non-use of skilled birth attendance group, class weighting was used to help the models pay more attention to this smaller group.

The researchers chose class weighting rather than SMOTE because many of the predictors were categorical and they wanted to avoid generating potentially unrealistic synthetic observations.

SHAP was used to explain the predictions of the best-performing model and identify the factors that contributed most to its predictions.

### Main Findings

XGBoost was identified as the best-performing model.

For identifying women who did not use skilled birth attendance, the study reported:

- F1-score: 0.52
- Recall: 0.73
- ROC-AUC: 0.75

Important predictors included:

- Maternal education
- Antenatal care visits
- Region
- Urban/rural residence
- Perceived distance to a healthcare facility

The SHAP analysis showed how these characteristics influenced the model's predictions.

For example, higher education and greater antenatal care use were associated with predictions toward skilled birth attendance, while rural residence and difficulty with distance to a healthcare facility contributed toward predictions of non-use.

### My Understanding

In simple terms, the researchers wanted to find out whether information about women in the Uganda DHS could help a computer identify women who were less likely to have a skilled health professional assisting them during childbirth.

Instead of testing only one machine-learning model, they tested seven different models to see which one performed best.

XGBoost performed best overall.

The researchers were particularly interested in identifying women who did not use skilled birth attendance. This group was smaller than the group that used skilled attendance, so they used class weighting to make the model pay more attention to these women.

They also used SHAP to understand why the model made its predictions.

The study showed that factors such as education, antenatal care, region, residence and access to healthcare were useful for predicting skilled birth attendance.

### Relevance to My Research

This study is highly relevant to my proposed research because it investigates the same general outcome: skilled birth attendance.

It also uses DHS data and compares several machine-learning models rather than relying on only one model.

The use of SHAP is relevant because my proposed research also aims to make the final model interpretable rather than treating it as a black box.

Another important similarity is the focus on identifying women who do not use skilled birth attendance. This is closely related to the outcome described in my research topic.

The study is particularly useful to my research because the researchers excluded variables directly tied to the outcome, such as place of delivery. This supports my intention to avoid variables that would not reasonably be available before childbirth.

The study also provides a useful example of handling class imbalance using class weighting rather than automatically applying synthetic oversampling methods.

### Differences From My Research

The study was conducted in Uganda using the 2016 Uganda DHS.

My proposed research will focus specifically on Nigeria using the 2023–24 Nigeria Demographic and Health Survey.

The healthcare system, geographical differences, socioeconomic conditions and patterns of maternal healthcare use in Nigeria may differ from those in Uganda. Therefore, findings from the Uganda study cannot automatically be assumed to apply to Nigerian women.

My proposed research also intends to evaluate model calibration and investigate whether model performance differs across important Nigerian geographical and socioeconomic groups.

### Limitations / Research Gap Identified

The study used cross-sectional DHS data, meaning that the findings should not be interpreted as proving that the identified predictors cause women to use or not use skilled birth attendance.

The data were also based on women's self-reported information and may therefore be affected by recall or reporting bias.

The research was specific to Uganda and used the 2016 Uganda DHS, so its findings and predictive model may not generalise directly to Nigeria or to more recent populations.

For my proposed research, an important remaining question is whether a similar interpretable machine-learning approach can successfully identify women less likely to receive skilled birth attendance specifically in Nigeria using the more recent 2023–24 NDHS.

I am also interested in going beyond discrimination metrics by examining model calibration and performance across geographical and socioeconomic groups.

These potential gaps will be considered together with evidence from the remaining studies before the final research gap is concluded.

### Important Variables Identified

Important predictors included:

- Maternal education
- Antenatal care visits
- Region
- Urban/rural residence
- Perceived distance to a healthcare facility

### Pre-Delivery Variables Only?

The study deliberately excluded variables directly tied to the outcome, including place of delivery.

The important predictors highlighted by the study, such as education, antenatal care visits, region, residence and perceived distance to a healthcare facility, can generally be determined before delivery.

This makes the study particularly relevant to my proposed pre-delivery prediction approach.

### Model Evaluation

- Best-performing model: XGBoost
- F1-score for non-use group: 0.52
- Recall for non-use group: 0.73
- ROC-AUC: 0.75
- Train/test split: 80% / 20%
- Cross-validation: 5-fold cross-validation used during hyperparameter tuning
- Class imbalance approach: Class weighting
- Explainability: SHAP
- Calibration: Not a main reported evaluation in the study

### Verification Checklist

- [x] Original paper located
- [x] Abstract reviewed
- [x] Dataset and study population verified
- [x] Methods verified
- [x] Results verified
- [x] Limitations reviewed
- [x] Full citation verified

### Full Citation

Memon, S. M. Z., Wamala, R., & Kabano, I. H. (2025). Identifying predictors of utilization of skilled birth attendance in Uganda through interpretable machine learning. International Journal of Environmental Research and Public Health, 22(11), 1691. https://doi.org/10.3390/ijerph22111691

### DOI / Original Publication

https://doi.org/10.3390/ijerph22111691

## Review Progress

- [x] Study 1
- [x] Study 2
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
