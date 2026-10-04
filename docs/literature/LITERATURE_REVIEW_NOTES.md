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

---

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


---

## Study 3: Miah (2026)

### Paper Title

Explainable Machine Learning Analysis of Factors Associated with Skilled Birth Attendance in Burkina Faso

### Country / Study Setting

Burkina Faso.

### Dataset

The study used data from the 2021 Burkina Faso Demographic and Health Survey (BF-DHS).

The final analysis included 5,111 women aged 15–49 years.

### Purpose of the Study

The study aimed to use explainable machine learning to predict skilled birth attendance in Burkina Faso, identify the most important factors associated with the predictions, and examine geographical and urban-rural inequalities in skilled birth attendance.

### Methods Used

The researcher compared five machine-learning models:

- Random Forest
- Decision Tree
- K-Nearest Neighbors
- Logistic Regression
- Support Vector Machine

Boruta feature selection was used to identify relevant predictors.

SMOTE was used to address class imbalance.

The models were evaluated using several performance measures, including:

- Accuracy
- Precision
- Recall
- F1-score
- Matthews Correlation Coefficient (MCC)
- Cohen's kappa
- AUROC

SHAP was used to explain the model's predictions and identify important predictors.

Decision Curve Analysis (DCA) was used to assess the potential usefulness of the model predictions.

Spatial mapping was also used to examine geographical variation in predicted skilled birth attendance across Burkina Faso.

### Main Findings

Random Forest achieved the highest discrimination among the five models.

The Random Forest model achieved an AUROC of 0.71, which the study described as moderate performance.

Important predictors identified in the study included:

- Province
- Four or more antenatal care visits
- Maternal age at first birth of at least 20 years
- Age at first sexual intercourse of at least 18 years
- Sexual activity
- Household wealth
- Religion

The geographical analysis showed variation in predicted skilled birth attendance across Burkina Faso.

Higher predicted probabilities were observed in some central and western provinces, while lower predicted probabilities were observed in Sahel, Sud-Ouest and Est.

The study also reported greater inequalities in rural areas.

### My Understanding

In simple terms, the researcher wanted to find out whether information from the Burkina Faso DHS could be used by machine-learning models to identify patterns associated with skilled birth attendance.

Five different models were tested, and Random Forest performed best. However, its AUROC of 0.71 showed moderate rather than extremely high predictive performance.

The researcher then used SHAP to understand which characteristics were contributing most to the predictions.

The study also went beyond simply predicting skilled birth attendance by looking at where geographical differences occurred across Burkina Faso.

This showed that machine learning can be combined with explainability and geographical analysis to investigate inequalities in maternal healthcare.

### Relevance to My Research

This study is highly relevant to my proposed research because it investigates skilled birth attendance using DHS data and machine-learning methods.

Like my proposed research, it focuses on one African country rather than pooling many countries together.

The study also compares several machine-learning models and uses SHAP to make the model predictions interpretable.

The geographical component is particularly relevant because my proposed research is also interested in geographical differences within Nigeria.

The study demonstrates that geographical information can be incorporated into an explainable machine-learning analysis of skilled birth attendance.

It also provides another example of dealing with class imbalance, in this case using SMOTE.

### Differences From My Research

The study was conducted in Burkina Faso using the 2021 Burkina Faso DHS.

My proposed research will focus specifically on Nigeria using the 2023–24 Nigeria Demographic and Health Survey.

The study examined geographical variation in predicted skilled birth attendance. My proposed research is interested not only in geographical and socioeconomic patterns in the outcome but also in examining whether the predictive model itself performs differently across important Nigerian geographical and socioeconomic groups.

These are related but different questions.

For example, identifying that one region has lower predicted skilled birth attendance does not necessarily tell us whether the model predicts equally well for women in that region compared with women in another region.

My proposed research will also place particular emphasis on predictors that could reasonably be known before the index delivery.

### Limitations / Research Gap Identified

The study used cross-sectional DHS data, so relationships identified by the models should not be interpreted as proof that the predictors cause skilled birth attendance.

The study was specific to Burkina Faso, meaning that the findings and predictive patterns may not generalise directly to Nigeria.

The best-performing model achieved moderate discrimination with an AUROC of 0.71, showing that predicting skilled birth attendance remains challenging even when machine-learning methods are used.

The study examined geographical differences in predicted skilled birth attendance, but geographical variation in predictions is different from evaluating whether model performance is consistent across geographical or socioeconomic subgroups.

For my proposed research, this raises an important question about whether a model developed using Nigerian data performs similarly across different Nigerian regions and socioeconomic groups.

This remains a potential research gap and will be assessed against the remaining literature before drawing a final conclusion.

### Important Variables Identified

Important predictors included:

- Province
- Antenatal care visits
- Maternal age at first birth
- Age at first sexual intercourse
- Sexual activity
- Household wealth
- Religion

### Pre-Delivery Variables Only?

Several important predictors, including province, antenatal care history, household wealth and religion, could potentially be known before delivery.

However, each candidate predictor for my proposed research will be assessed carefully according to whether it would genuinely be available before the specific index delivery being predicted.

Variables will not be included in my proposed model simply because they were used in a previous study.

### Model Evaluation

- Best-performing model: Random Forest
- ROC-AUC: 0.71
- Performance description: Moderate discrimination
- Other metrics evaluated: Accuracy, Precision, Recall, F1-score, Matthews Correlation Coefficient and Cohen's kappa
- Class imbalance approach: SMOTE
- Feature selection: Boruta
- Explainability: SHAP
- Additional evaluation: Decision Curve Analysis
- Geographical analysis: Spatial mapping
- Calibration: Not highlighted as a main evaluation in the article abstract

### Verification Checklist

- [x] Original paper located
- [x] Abstract reviewed
- [x] Dataset and sample verified
- [x] Methods verified
- [x] Results verified
- [x] Limitations reviewed
- [x] Full citation verified

### Full Citation

Miah, M. S. (2026). Explainable machine learning analysis of factors associated with skilled birth attendance in Burkina Faso. Scientific Reports. https://doi.org/10.1038/s41598-026-72356-7

### DOI / Original Publication

https://doi.org/10.1038/s41598-026-72356-7

## Review Progress

- [x] Study 1
- [x] Study 2
- [x] Study 3
- [ ] Study 4
- [ ] Study 5
- [ ] Study 6
- [ ] Study 7
- [ ] Study 8
- [ ] Study 9
- [ ] Study 10
- [ ] Study 11
- [ ] Study 12
