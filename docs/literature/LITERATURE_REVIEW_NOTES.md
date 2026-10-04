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

---

## Study 4: Sani et al. (2025)

### Paper Title

Exploring the Application of Machine Learning and SHAP Explanations to Predict Health Facility Deliveries in Somalia

### Country / Study Setting

Somalia.

### Dataset

The study used data from the 2020 Somalia Demographic and Health Survey (SDHS).

The researchers used the Individual Record (IR) dataset and included 8,951 women aged 15–49 who had information about their place of delivery.

### Purpose of the Study

The study aimed to determine whether machine-learning models could predict whether women in Somalia would deliver in a health facility.

The researchers also wanted to identify the factors that were most important in predicting health facility delivery and use SHAP to explain how these factors influenced the model predictions.

### Methods Used

The researchers compared seven machine-learning models:

- Logistic Regression
- Support Vector Machine
- Decision Tree
- Random Forest
- K-Nearest Neighbors
- Gradient Boosting
- XGBoost

The data were divided into 80% training data and 20% testing data.

Stratified 5-fold cross-validation was also used.

The researchers used multiple imputation with predictive mean matching to handle missing values.

SMOTE was used to address class imbalance because facility deliveries were the smaller outcome group.

Recursive Feature Elimination (RFE) was used for feature selection, and 10 features were retained for the final modelling.

SHAP was used to explain the contribution of different predictors to the model predictions.

### Main Findings

Random Forest achieved the best overall performance.

Its reported performance was:

- Accuracy: 82%
- Precision: 81%
- Recall: 84%
- F1-score: 82%
- ROC-AUC: 0.89

XGBoost performed similarly, with an ROC-AUC of 0.89 and accuracy of 80%.

Important predictors identified through SHAP included:

- Household wealth
- Residence type
- Education
- Antenatal care visits
- Region

Marital status, employment and distance to a health facility also contributed to predictions but were less influential.

Household wealth was identified as the most influential predictor.

### My Understanding

In simple terms, the researchers wanted to see whether information about women in the Somalia DHS could help a computer predict whether they would give birth in a healthcare facility rather than at home.

They tested seven different machine-learning models instead of relying on only one.

Random Forest performed best overall.

The researchers also used SHAP to understand why the model was making its predictions.

The results showed that factors such as household wealth, where a woman lived, education, antenatal care attendance and region were important in predicting health facility delivery.

This study shows that machine learning can be combined with DHS data and explainability methods to investigate maternal healthcare use.

### Relevance to My Research

This study is relevant to my proposed research because it applies machine learning to a maternal-health service-use problem using DHS data from an African country.

It also compares several machine-learning models and uses SHAP to explain the predictions.

Many of its important predictors, including education, household wealth, residence, region and antenatal care attendance, could reasonably be known before childbirth.

The study therefore provides useful methodological evidence for using pre-delivery information to predict maternal healthcare utilisation.

It also provides another example of using Random Forest, XGBoost, SMOTE, cross-validation and SHAP in maternal-health prediction research.

### Differences From My Research

The most important difference is the outcome being predicted.

This study predicted health facility delivery, meaning whether a woman gave birth in a healthcare facility or at home.

My proposed research will predict non-use of skilled birth attendance, meaning whether the delivery was assisted by a provider who meets the NDHS definition of a skilled birth attendant.

Health facility delivery and skilled birth attendance are closely related maternal-health outcomes, but they are not the same outcome.

The study was also conducted in Somalia using the 2020 Somalia DHS, while my proposed research will focus specifically on Nigeria using the 2023–24 Nigeria DHS.

My proposed research also intends to examine model calibration and model performance across important Nigerian geographical and socioeconomic groups.

### Limitations / Research Gap Identified

The authors reported several limitations.

The study used cross-sectional data, which means the relationships identified should not be interpreted as proving cause and effect.

Some information, including antenatal care attendance and delivery location, was self-reported and may therefore be affected by recall bias.

The model did not undergo external validation outside Somalia, which limits how confidently its performance can be generalised to other populations.

The authors also noted that although SHAP improves interpretability, machine-learning models may still be difficult to integrate directly into routine maternal-health decision-making.

For my research, the main distinction is that this study does not directly investigate skilled birth attendance.

It therefore provides related methodological evidence rather than direct evidence for my exact outcome.

### Important Variables Identified

Important predictors included:

- Household wealth
- Urban/rural/nomadic residence
- Maternal education
- Antenatal care visits
- Region
- Distance to a healthcare facility
- Marital status
- Employment status

### Pre-Delivery Variables Only?

The important predictors highlighted by the study largely represent information that could potentially be known before childbirth.

Examples include:

- Education
- Household wealth
- Residence
- Region
- Antenatal care attendance
- Distance to a healthcare facility

However, my proposed study will independently assess every candidate predictor to ensure that it would genuinely be available before the specific delivery being predicted.

### Model Evaluation

- Best-performing model: Random Forest
- Accuracy: 82%
- Precision: 81%
- Recall: 84%
- F1-score: 82%
- ROC-AUC: 0.89
- Train/test split: 80% / 20%
- Cross-validation: Stratified 5-fold cross-validation
- Class imbalance approach: SMOTE
- Feature selection: Recursive Feature Elimination
- Explainability: SHAP
- External validation: No
- Calibration: Not highlighted as a main evaluation

### Verification Checklist

- [x] Original paper located
- [x] Abstract reviewed
- [x] Dataset and sample verified
- [x] Methods verified
- [x] Results verified
- [x] Limitations reviewed
- [x] Full citation verified

### Full Citation

Sani, J., Halane, S., Ahmed, M. M., Ahmed, A. M., & Mohamoud, J. H. (2025). Exploring the application of machine learning and SHAP explanations to predict health facility deliveries in Somalia. Discover Artificial Intelligence, 5, 211. https://doi.org/10.1007/s44163-025-00436-0

### DOI / Original Publication

https://doi.org/10.1007/s44163-025-00436-0

---

## Study 5: Unegbu (2026)

### Paper Title

Determinants of Skilled Birth Attendance in Nigeria: A Population-Based Analysis of the 2018 Demographic and Health Survey

### Publication Status

Preprint published on medRxiv.

This study had not undergone peer review at the time it was reviewed. Therefore, its findings will be interpreted with appropriate caution.

### Country / Study Setting

Nigeria.

### Dataset

The study used data from the 2018 Nigeria Demographic and Health Survey (NDHS).

The analysis included 21,465 women who had given birth during the five years preceding the survey and had the required information for the analysis.

### Purpose of the Study

The study aimed to identify demographic, socioeconomic, healthcare and geographical factors associated with skilled birth attendance among women in Nigeria.

Rather than developing a machine-learning prediction model, the study focused mainly on determining which characteristics remained statistically associated with skilled birth attendance after accounting for other factors.

### Methods Used

The researcher used survey-weighted statistical analysis to account for the complex sampling design of the Nigeria DHS.

Multivariable logistic regression was used to examine the relationship between different characteristics and skilled birth attendance.

The analysis considered both crude and adjusted associations.

This allowed the researcher to examine whether relationships observed between individual characteristics and skilled birth attendance remained after accounting for other variables.

### Main Findings

Overall, approximately 44.9% of women in the study had skilled birth attendance.

There were very large geographical differences across Nigeria.

Skilled birth attendance was approximately:

- 17.7% in the North West
- 85.6% in the South West

Several factors remained independently associated with skilled birth attendance after adjustment.

Some of the strongest reported associations included:

- Higher education: adjusted odds ratio approximately 7.01
- Richest household wealth group: adjusted odds ratio approximately 6.27
- Four or more antenatal care visits: adjusted odds ratio approximately 3.80

Region, urban/rural residence, maternal age and parity were also associated with skilled birth attendance.

Higher parity was associated with lower odds of skilled birth attendance.

### My Understanding

In simple terms, this study looked at Nigerian women and tried to understand why some women were more likely than others to have a skilled health professional assisting them during childbirth.

The researcher used the 2018 Nigeria DHS and compared characteristics such as education, household wealth, antenatal care, region, residence, age and number of previous births.

The study found that skilled birth attendance was not equally distributed across Nigeria. There were especially large differences between geographical regions.

Women with higher education, greater household wealth and sufficient antenatal care visits were much more likely to have skilled birth attendance.

One important thing I learned from this study is that factors can overlap.

For example, an urban woman may also be wealthier, more educated and have better access to healthcare. Therefore, looking at only one factor at a time may give a misleading picture.

The adjusted analysis helped determine which factors remained associated with skilled birth attendance after considering other characteristics.

### Relevance to My Research

This study is highly relevant to my research because it focuses specifically on Nigeria and investigates the same broad outcome: skilled birth attendance.

It also uses Nigeria DHS data, which is the same survey programme that will provide the data for my proposed research.

The study provides important Nigeria-specific evidence about factors associated with skilled birth attendance.

Education, household wealth, antenatal care, region, residence, age and parity are particularly relevant because many of these characteristics could potentially be known before childbirth.

The very large regional differences identified in the study also support the importance of considering geographical variation when studying skilled birth attendance in Nigeria.

The study will therefore help inform the candidate predictors and subgroup analyses that I may investigate using the 2023–24 NDHS.

### Differences From My Research

The study used the 2018 Nigeria DHS, while my proposed research will use the newer 2023–24 Nigeria DHS.

The study primarily investigated statistical associations using logistic regression.

My proposed research has a different primary objective: to investigate whether information available before childbirth can be used to predict non-use of skilled birth attendance.

I intend to compare predictive models, evaluate their performance and use explainability methods to understand important predictors.

My proposed research also intends to examine model calibration and assess whether predictive performance differs across important Nigerian geographical and socioeconomic groups.

Therefore, the previous study mainly answers:

"Which factors are associated with skilled birth attendance?"

My proposed research asks:

"How well can we identify women at greater risk of non-use before delivery, and does the model perform reliably across different groups?"

### Limitations / Research Gap Identified

The study used cross-sectional survey data. Therefore, the reported associations should not be interpreted as proof that the identified characteristics cause skilled birth attendance.

Some DHS information is self-reported and may be affected by recall or reporting bias.

The study used data from the 2018 NDHS, so the findings may not completely represent the maternal-health situation captured in the newer 2023–24 NDHS.

The study focused primarily on association rather than developing and evaluating a machine-learning prediction model.

Another important consideration is that this study is currently a preprint and had not undergone peer review at the time of this literature review.

For my research, this study provides strong Nigeria-specific background evidence, but it does not answer whether non-use of skilled birth attendance can be predicted using the newer 2023–24 NDHS and information available before delivery.

These observations will be considered together with the remaining literature before defining the final research gap.

### Important Variables Identified

Important factors included:

- Maternal education
- Household wealth
- Antenatal care visits
- Geographical region
- Urban/rural residence
- Maternal age
- Parity

### Pre-Delivery Variables Only?

Many of the important characteristics identified in this study could potentially be known before childbirth.

These include:

- Maternal education
- Household wealth
- Region
- Residence
- Maternal age
- Parity
- Antenatal care history

However, my proposed research will assess the timing of every candidate variable carefully to ensure that the information would genuinely have been available before the specific delivery being predicted.

### Model Evaluation

This was not primarily a machine-learning prediction study.

- Main analytical method: Survey-weighted multivariable logistic regression
- Machine-learning model comparison: No
- ROC-AUC: Not a main reported evaluation
- Accuracy: Not a main reported evaluation
- Precision: Not a main reported evaluation
- Recall: Not a main reported evaluation
- F1-score: Not a main reported evaluation
- Calibration: Not a main reported evaluation
- Explainability method such as SHAP: No
- Main focus: Statistical associations with skilled birth attendance

### Verification Checklist

- [x] Original paper located
- [x] Abstract reviewed
- [x] Dataset and sample verified
- [x] Methods verified
- [x] Results verified
- [x] Limitations reviewed
- [x] Full citation verified
- [x] Publication status checked

### Full Citation

Unegbu, U. L. (2026). Determinants of skilled birth attendance in Nigeria: A population-based analysis of the 2018 Demographic and Health Survey. medRxiv. https://doi.org/10.64898/2026.04.23.26350432

### DOI / Original Publication

https://doi.org/10.64898/2026.04.23.26350432

### Publication Note

This article is a medRxiv preprint and had not undergone peer review when it was reviewed for this project.

---

## Study 6: Akinyemi et al. (2022)

### Paper Title

Multivariate Decomposition of Trends, Inequalities and Predictors of Skilled Birth Attendants Utilisation in Nigeria (1990–2018): A Cross-Sectional Analysis of Change Drivers

### Publication Status

Peer-reviewed journal article published in BMJ Open.

### Country / Study Setting

Nigeria.

### Dataset

The study used data from five Nigeria Demographic and Health Survey rounds:

- 1990 NDHS
- 2003 NDHS
- 2008 NDHS
- 2013 NDHS
- 2018 NDHS

The study population consisted of women aged 15–49 years who had at least one birth during the five years preceding the respective surveys.

### Purpose of the Study

The study aimed to examine changes in the utilisation of skilled birth attendants in Nigeria over time.

The researchers were particularly interested in:

- Trends in skilled birth attendant utilisation.
- Inequalities in utilisation among different groups of women.
- Factors associated with skilled birth attendant utilisation.
- Understanding what contributed to changes in utilisation over time.

### Methods Used

The researchers conducted a cross-sectional analysis using multiple rounds of nationally representative Nigeria DHS data.

They examined trends and inequalities in skilled birth attendant utilisation.

They also used multivariate decomposition analysis to investigate what contributed to changes in skilled birth attendant utilisation over time.

The decomposition separated the observed change into two broad components:

- Changes in population characteristics, also referred to as the endowment or composition component.
- Changes in the effects or influence of those characteristics, also referred to as the coefficient component.

In simple terms, this allowed the researchers to investigate whether changes in skilled birth attendant utilisation happened because Nigerian women's characteristics changed over time or because the relationships between those characteristics and SBA utilisation changed.

### Main Findings

The study found that skilled birth attendant utilisation in Nigeria increased over time.

Between 2003 and 2018, utilisation increased by approximately 12 percentage points.

The decomposition analysis showed that approximately:

- 11.5% of the change was explained by differences in women's characteristics.
- 88.5% was attributed to differences in the effects of those characteristics.

The study also identified persistent inequalities in skilled birth attendant utilisation across demographic, socioeconomic and healthcare-related groups.

The findings showed that changes in skilled birth attendant utilisation could not be explained simply by changes in the characteristics of Nigerian women.

### My Understanding

In simple terms, the researchers wanted to understand how the use of skilled birth attendants in Nigeria changed over many years and why those changes occurred.

They compared information from five Nigeria DHS surveys covering the period from 1990 to 2018.

They found that skilled birth attendant utilisation increased over time, but the improvement was not equal across all groups of women.

The researchers also tried to understand why SBA utilisation changed.

Their analysis showed that only part of the change could be explained by changes in women's characteristics.

A much larger part was related to changes in how those characteristics were associated with the use of skilled birth attendants.

This study helps me understand that maternal healthcare patterns in Nigeria are not fixed. They can change over time.

Therefore, findings from older Nigeria DHS surveys should not automatically be assumed to describe the situation captured by the newer 2023–24 NDHS.

### Relevance to My Research

This study is highly relevant to my research because it focuses specifically on Nigeria and investigates the same broad outcome: skilled birth attendant utilisation.

It also uses Nigeria DHS data, which is the same survey programme that provides the data for my proposed research.

The study provides important historical evidence showing how skilled birth attendance has changed in Nigeria over time.

It also highlights inequalities in skilled birth attendant utilisation among different population groups.

This is relevant to my proposed research because I intend to use the newer 2023–24 NDHS and examine whether predictive performance differs across important geographical and socioeconomic groups.

The study also demonstrates why using the latest available Nigeria DHS is valuable. Relationships identified using older surveys may change over time.

### Differences From My Research

This study focused primarily on historical trends, inequalities and the factors contributing to changes in skilled birth attendant utilisation between different survey periods.

It did not primarily aim to develop a machine-learning prediction model.

My proposed research will focus on the 2023–24 Nigeria DHS and investigate whether information available before childbirth can be used to predict non-use of skilled birth attendance.

I also intend to compare predictive models, assess model performance and calibration, use explainability methods, and investigate model performance across important geographical and socioeconomic groups.

Therefore, this study mainly asks:

"How has skilled birth attendant utilisation changed in Nigeria over time, and what contributed to those changes?"

My proposed study asks:

"Can information available before childbirth identify women at greater risk of non-use of skilled birth attendance using the latest NDHS, and how reliably does the model perform across different groups?"

### Limitations / Research Gap Identified

The study was based on repeated cross-sectional DHS surveys rather than longitudinally following the same women over time.

Therefore, the analysis describes population-level changes across different survey periods rather than changes experienced by the same individual women.

The study relied on secondary DHS data and was limited to variables available within those surveys.

Because DHS information includes self-reported responses, some variables may also be affected by recall or reporting bias.

The most recent survey included in the study was the 2018 NDHS.

Therefore, the study does not describe patterns captured in the newer 2023–24 Nigeria DHS.

The study also focused on trends and decomposition rather than developing and evaluating a model for predicting individual non-use of skilled birth attendance before delivery.

For my research, this leaves an important reason to investigate the latest Nigerian data using a prediction-focused approach.

However, this will be considered together with the remaining studies before the final research gap is concluded.

### Important Variables / Factors Examined

The study examined demographic, socioeconomic and healthcare-related characteristics associated with skilled birth attendant utilisation.

These included factors relating to:

- Maternal education
- Household socioeconomic status
- Place of residence
- Geographical region
- Maternal characteristics
- Healthcare utilisation

### Pre-Delivery Variables Only?

This was not specifically designed as a pre-delivery prediction study.

However, several of the demographic and socioeconomic characteristics examined could potentially be known before childbirth.

For my proposed research, every candidate predictor will be assessed separately to confirm that it would genuinely have been available before the specific delivery being predicted.

### Model Evaluation

This was not primarily a machine-learning prediction study.

- Main approach: Trend, inequality and multivariate decomposition analysis
- Machine-learning model comparison: No
- Accuracy: Not applicable as a main evaluation
- Precision: Not applicable as a main evaluation
- Recall: Not applicable as a main evaluation
- F1-score: Not applicable as a main evaluation
- ROC-AUC: Not applicable as a main evaluation
- Calibration: Not a main evaluation
- SHAP/explainable ML: No
- Main focus: Trends, inequalities and drivers of change in SBA utilisation

### Verification Checklist

- [x] Original paper located
- [x] Abstract reviewed
- [x] DHS survey rounds verified
- [x] Study population verified
- [x] Methods verified
- [x] Main findings verified
- [x] Limitations reviewed
- [x] Full citation verified
- [x] Publication status checked

### Full Citation

Akinyemi, J. O., et al. (2022). Multivariate decomposition of trends, inequalities and predictors of skilled birth attendants utilisation in Nigeria (1990–2018): A cross-sectional analysis of change drivers. BMJ Open, 12, e051791.

### DOI / Original Publication

https://doi.org/10.1136/bmjopen-2021-051791

---
## Study 7: Okoli et al. (2020)

### Paper Title

Geographical and Socioeconomic Inequalities in the Utilization of Maternal Healthcare Services in Nigeria: 2003–2017

### Publication Status

Peer-reviewed journal article published in BMC Health Services Research.

### Country / Study Setting

Nigeria.

### Dataset

The study used four rounds of the Nigeria Demographic and Health Survey:

- 2003 NDHS
- 2008 NDHS
- 2013 NDHS
- 2018 NDHS

The analysis focused on women aged 15–49 years.

### Purpose of the Study

The study aimed to investigate geographical and socioeconomic inequalities in the use of maternal healthcare services in Nigeria over time.

The researchers examined three maternal healthcare outcomes:

- Antenatal care (ANC)
- Facility-based delivery (FBD)
- Skilled birth attendance (SBA)

They investigated whether utilisation differed according to:

- Urban or rural residence
- Nigeria's six geopolitical zones
- Maternal education
- Household wealth

### Methods Used

The researchers used several statistical measures to examine different types of inequality.

Rate ratios and rate differences were used to compare maternal healthcare utilisation between urban and rural women.

The Theil Index and between-group variance were used to examine relative and absolute inequalities across Nigeria's six geopolitical zones.

Relative and absolute concentration indices were used to examine education- and wealth-related inequalities.

In simple terms, these methods allowed the researchers to measure how large the differences in maternal healthcare utilisation were between different groups of Nigerian women and whether those differences changed over time.

### Main Findings

The study found persistent geographical and socioeconomic inequalities in maternal healthcare utilisation in Nigeria.

Maternal healthcare utilisation was generally lower among:

- Poorer women
- Less-educated women
- Women living in rural areas
- Women living in the North West
- Women living in the North East

The study found that relative inequalities in antenatal care and facility-based delivery across the six geopolitical zones declined over time.

However, the results did not show evidence that absolute geographical inequalities in ANC, facility-based delivery and skilled birth attendance disappeared over time.

Maternal healthcare utilisation also remained concentrated among better-educated and wealthier women.

The study therefore showed that improvements in maternal healthcare utilisation at the national level did not mean that all Nigerian women benefited equally.

### My Understanding

In simple terms, the researchers wanted to know whether Nigerian women had equal access to and use of important maternal healthcare services.

They compared women according to where they lived, their education and their household wealth.

They found that maternal healthcare utilisation was not equally distributed.

Poorer women, women with less education, rural women and women living in the North West and North East generally had lower utilisation.

This study helped me understand that looking only at a national average can hide important differences between groups.

For example, maternal healthcare utilisation in Nigeria may improve overall while some regions or socioeconomic groups remain far behind.

### Relevance to My Research

This study is highly relevant to my research because it provides Nigeria-specific evidence of geographical and socioeconomic inequalities in skilled birth attendance and related maternal healthcare services.

My proposed research intends to develop a model for predicting non-use of skilled birth attendance using the 2023–24 NDHS.

If skilled birth attendance already differs substantially across geographical and socioeconomic groups, evaluating only the overall performance of my predictive model may hide important differences.

For example, a model could perform well overall but perform less effectively for women in a particular geopolitical zone, wealth group or place of residence.

This study therefore provides public-health justification for considering subgroup performance when evaluating my proposed model.

### Differences From My Research

This study did not develop a machine-learning prediction model.

Its main objective was to measure geographical and socioeconomic inequalities in maternal healthcare utilisation.

It also used NDHS surveys from 2003 to 2018, whereas my proposed research will use the newer 2023–24 NDHS.

The study examined inequalities in the healthcare outcomes themselves.

My proposed research intends to additionally investigate whether the performance of a prediction model differs across important geographical and socioeconomic groups.

These are related but different questions.

An outcome being less common in one group does not automatically mean that a predictive model performs poorly for that group.

Therefore, my proposed subgroup evaluation will focus on model performance rather than only differences in SBA prevalence.

### Limitations / Research Gap Identified

The study used repeated cross-sectional DHS surveys rather than following the same women over time.

It was also limited to variables available within the DHS datasets.

The analysis focused on population-level inequalities in maternal healthcare utilisation rather than individual-level prediction.

The most recent NDHS included was the 2018 survey, so the study does not describe inequalities using the newer 2023–24 NDHS.

Most importantly for my proposed research, the study evaluated inequalities in maternal healthcare utilisation but did not evaluate whether a predictive model performs consistently across geographical and socioeconomic groups.

This provides important motivation for considering subgroup model performance in my research.

However, whether this represents a clear research gap will only be concluded after the remaining literature has been reviewed.

### Important Variables / Groups Examined

Important dimensions of inequality included:

- Maternal education
- Household wealth
- Urban/rural residence
- Geopolitical zone

The study compared Nigeria's six geopolitical zones and examined socioeconomic inequalities based particularly on education and household wealth.

### Pre-Delivery Variables Only?

This was not designed as a pre-delivery prediction study.

However, the main characteristics used to define inequalities could be known before childbirth:

- Education
- Household wealth
- Place of residence
- Geopolitical zone

These characteristics may therefore be relevant both as candidate predictors and as possible groups for evaluating model performance in my proposed research.

The final subgroup variables will only be selected after examining the 2023–24 NDHS and completing the literature review.

### Model Evaluation

This was not a machine-learning prediction study.

- Main approach: Inequality analysis
- Urban/rural inequality: Rate ratios and rate differences
- Geographical inequality: Theil Index and between-group variance
- Education/wealth inequality: Relative and absolute concentration indices
- Machine-learning models: No
- Accuracy: Not applicable
- Precision: Not applicable
- Recall: Not applicable
- F1-score: Not applicable
- ROC-AUC: Not applicable
- Calibration: Not applicable
- SHAP/explainable ML: No
- Main focus: Geographical and socioeconomic inequalities in maternal healthcare utilisation

### Verification Checklist

- [x] Original paper located
- [x] Abstract reviewed
- [x] DHS survey rounds verified
- [x] Study population verified
- [x] Maternal healthcare outcomes verified
- [x] Inequality measures verified
- [x] Main findings verified
- [x] Full citation verified
- [x] Publication status checked

### Full Citation

Okoli, C., Hajizadeh, M., Rahman, M. M., & Khanam, R. (2020). Geographical and socioeconomic inequalities in the utilization of maternal healthcare services in Nigeria: 2003–2017. BMC Health Services Research, 20, 849. https://doi.org/10.1186/s12913-020-05700-w

### DOI / Original Publication

https://doi.org/10.1186/s12913-020-05700-w

---

## Study 8: Doctor et al. (2020)

### Paper Title

Prevalence, Trends, and Drivers of the Utilization of Unskilled Birth Attendants during Democratic Governance in Nigeria from 1999 to 2018

### Publication Status

Peer-reviewed journal article.

### Country / Study Setting

Nigeria.

### Dataset

The study used data from five Nigeria Demographic and Health Survey rounds:

- 1999 NDHS
- 2003 NDHS
- 2008 NDHS
- 2013 NDHS
- 2018 NDHS

The study examined births assisted by traditional birth attendants and other unskilled birth attendants.

### Purpose of the Study

The study aimed to examine the prevalence and trends in the use of unskilled birth attendants in Nigeria and identify factors associated with their utilisation.

The researchers distinguished between:

- Traditional birth attendants (TBAs)
- Other unskilled birth attendants

This allowed them to examine not only whether women received skilled care but also the types of unskilled assistance used during childbirth.

### Methods Used

The researchers analysed nationally representative Nigeria DHS data from multiple survey years.

Descriptive analyses were used to examine changes in the prevalence of different types of birth attendants over time.

Multivariable multinomial logistic regression was used to identify factors associated with the use of traditional birth attendants and other unskilled birth attendants.

The analysis considered demographic, socioeconomic, healthcare-access and women's empowerment characteristics.

### Main Findings

The study found that the use of traditional birth attendants remained relatively stable over the study period.

Traditional birth attendant use was approximately:

- 20.7% in 1999
- 20.5% in 2018

This suggests that the proportion of births assisted by traditional birth attendants changed very little over almost two decades.

The use of other unskilled birth attendants declined over time but remained substantial.

Several characteristics were associated with the use of unskilled birth attendants.

Factors associated with lower likelihood of using unskilled attendants included:

- Higher maternal and paternal education
- Greater household wealth
- Maternal employment
- Four or more antenatal care visits
- Better proximity to healthcare facilities
- Greater female autonomy

Geographical region, rural residence and other maternal and reproductive characteristics were also associated with the type of birth attendant used.

### My Understanding

In simple terms, the researchers wanted to understand which Nigerian women were giving birth with assistance from people who were not classified as skilled birth attendants.

They also wanted to know whether this situation had improved over time.

One important finding was that the use of traditional birth attendants changed very little between 1999 and 2018.

The study also showed that women's circumstances mattered.

Women with more education, greater household wealth, adequate antenatal care, better healthcare access and greater decision-making autonomy were generally less likely to use unskilled birth attendants.

This helped me understand that non-use of skilled birth attendance is connected not only to healthcare availability but also to socioeconomic circumstances and women's ability to make healthcare decisions.

### Relevance to My Research

This study is highly relevant to my research because it focuses specifically on Nigeria and examines the unskilled side of childbirth assistance.

My proposed research focuses on predicting non-use of skilled birth attendance.

Therefore, understanding the characteristics associated with the use of unskilled attendants provides useful background evidence about the population I am interested in identifying.

The study also uses Nigeria DHS data and identifies several factors that could potentially be available before childbirth, including education, wealth, residence, region, antenatal care, healthcare access and women's autonomy.

These factors can be investigated as potential candidate predictors when I examine the 2023–24 NDHS.

The finding concerning women's autonomy is particularly useful because it suggests that decision-making power may provide information beyond commonly examined socioeconomic variables such as education and wealth.

### Differences From My Research

This study examined trends and factors associated with the use of different types of unskilled birth attendants.

My proposed research will construct an outcome based on the 2023–24 NDHS definition of skilled birth attendance and predict non-use of skilled attendance.

Therefore, the outcome definitions are closely related but should not automatically be treated as identical.

The study also focused primarily on statistical associations using multinomial logistic regression rather than developing and evaluating several machine-learning prediction models.

It used surveys ending with the 2018 NDHS, whereas my research will use the newer 2023–24 NDHS.

My proposed study will also focus specifically on information that could reasonably be known before the delivery being predicted.

### Limitations / Research Gap Identified

The study relied on repeated cross-sectional DHS surveys rather than following the same women over time.

DHS information is partly self-reported and may therefore be affected by recall and reporting bias.

The analysis was also limited to variables available in the DHS.

The study examined associations with unskilled birth-attendant utilisation rather than developing a prospective-style prediction model using only information available before delivery.

Its most recent dataset was the 2018 NDHS, so it does not describe the situation captured by the 2023–24 Nigeria DHS.

Another important consideration for my research is outcome definition.

Use of a traditional or other unskilled birth attendant in this study should not simply be copied as my definition of non-use of skilled birth attendance.

My outcome will instead be constructed according to the skilled-provider definition used in the 2023–24 NDHS.

### Important Variables / Factors Examined

Important factors included:

- Maternal education
- Paternal education
- Household wealth
- Maternal employment
- Antenatal care attendance
- Urban/rural residence
- Geographical region
- Healthcare accessibility
- Maternal age
- Reproductive characteristics
- Women's autonomy and decision-making

### Pre-Delivery Variables Only?

This was not specifically designed as a pre-delivery prediction study.

However, many of the characteristics identified could potentially be known before childbirth, including:

- Education
- Household wealth
- Employment
- Residence
- Region
- Antenatal care history
- Healthcare access
- Maternal age
- Women's decision-making/autonomy

Each variable will still need to be checked carefully in the 2023–24 NDHS to determine whether it was measured in a way that makes it appropriate for predicting the specific index delivery.

### Model Evaluation

This was not primarily a machine-learning prediction study.

- Main analytical method: Multivariable multinomial logistic regression
- Machine-learning model comparison: No
- Accuracy: Not applicable as a main evaluation
- Precision: Not applicable as a main evaluation
- Recall: Not applicable as a main evaluation
- F1-score: Not applicable as a main evaluation
- ROC-AUC: Not applicable as a main evaluation
- Calibration: Not a main evaluation
- SHAP/explainable ML: No
- Main focus: Trends and factors associated with use of unskilled birth attendants

### Verification Checklist

- [x] Original paper located
- [x] Abstract reviewed
- [x] DHS survey rounds verified
- [x] Outcome categories verified
- [x] Methods verified
- [x] Main findings verified
- [x] Important factors reviewed
- [x] Full citation verified
- [x] Publication status checked

### Full Citation

Doctor, H. V., Radovich, E., Benova, L., et al. (2020). Prevalence, trends, and drivers of the utilization of unskilled birth attendants during democratic governance in Nigeria from 1999 to 2018. International Journal of Environmental Research and Public Health, 17(1), 372.

### DOI / Original Publication

https://doi.org/10.3390/ijerph17010372

---

## Study 9: Solanke and Rahman (2018)

### Paper Title

Multilevel Analysis of Factors Associated with Assistance During Delivery in Rural Nigeria: Implications for Reducing Rural-Urban Inequity in Skilled Care at Delivery

### Publication Status

Peer-reviewed research article published in BMC Pregnancy and Childbirth.

### Country / Study Setting

Nigeria, specifically women living in rural areas.

### Dataset

The study used data from the 2013 Nigeria Demographic and Health Survey (NDHS).

The analysis included a weighted sample of 12,665 rural women.

The outcome was assistance during the woman's most recent delivery, classified as:

- Skilled assistance
- Unskilled assistance

### Purpose of the Study

The study aimed to investigate both individual-level and community-level factors associated with skilled assistance during delivery among women living in rural Nigeria.

The researchers wanted to go beyond examining only characteristics of individual women and determine whether characteristics of the communities where women lived also contributed to differences in skilled birth attendance.

### Methods Used

The researchers used mixed-effects logistic regression.

This type of analysis allowed them to examine factors operating at two levels:

1. Individual-level characteristics
2. Community-level characteristics

Individual-level characteristics included:

- Maternal education
- Parity
- Age at first birth
- Religion
- Participation in healthcare decisions
- Employment status
- Access to mass media
- Means of transportation

Community-level characteristics included:

- Community literacy level
- Community childcare burden
- Proportion of women employed outside agriculture
- Community perception of distance to a healthcare facility
- Community poverty level
- Geographical region

The researchers also used the Intra-Class Correlation (ICC) to determine whether differences between communities contributed meaningfully to differences in skilled assistance.

### Main Findings

Only 23.0% of rural women used skilled assistance during their most recent delivery.

Approximately 77.0% used unskilled assistance.

Important individual-level factors associated with skilled assistance included:

- Maternal education
- Parity
- Religion
- Participation in healthcare decisions
- Access to mass media
- Means of transportation

Important community-level factors included:

- Community literacy level
- Community poverty level
- Community perception of distance to a healthcare facility
- Geographical region

The Intra-Class Correlation results also supported the presence of significant community-level differences in skilled assistance.

For example, women who participated in decisions about their own healthcare were more likely to use skilled assistance than women who did not participate in those decisions.

### My Understanding

In simple terms, the researchers wanted to understand why some women living in rural Nigeria had skilled assistance during childbirth while others did not.

Instead of looking only at the individual woman, they also considered the type of community in which she lived.

The study found that only about 23% of rural women had skilled assistance during their most recent delivery, while about 77% had unskilled assistance.

A woman's education, number of previous births, religion, involvement in healthcare decisions, access to media and means of transportation were important.

However, the community also mattered.

Women living in communities with different levels of poverty, literacy, healthcare accessibility and geographical location had different likelihoods of using skilled assistance.

This helped me understand that skilled birth attendance may be influenced by both personal circumstances and the wider environment in which a woman lives.

### Relevance to My Research

This study is highly relevant to my research because it focuses specifically on Nigeria and examines skilled versus unskilled assistance during childbirth.

It also uses NDHS data.

The study shows that information about the individual woman may not provide the complete picture when investigating non-use of skilled birth attendance.

Community and geographical characteristics may also contain important information.

This is relevant when I examine potential predictors in the 2023–24 NDHS.

The study also identifies several factors that could potentially be available before delivery, including education, parity, healthcare decision-making, media exposure, transportation and geographical characteristics.

It therefore provides useful evidence for considering both individual and contextual information when developing my prediction model.

### Differences From My Research

The study used the 2013 NDHS, while my proposed research will use the newer 2023–24 NDHS.

It included only women living in rural Nigeria, whereas my proposed research intends to study the eligible Nigerian population more broadly.

The study primarily investigated statistical associations using mixed-effects logistic regression.

My proposed research will focus on predicting non-use of skilled birth attendance using information available before childbirth.

I also intend to compare predictive models, evaluate discrimination and calibration, use explainability methods and investigate model performance across important geographical and socioeconomic groups.

Therefore, this study mainly asks:

"Which individual and community characteristics are associated with skilled assistance among rural Nigerian women?"

My research asks:

"How well can pre-delivery information predict non-use of skilled birth attendance in Nigeria, and how reliably does the model perform across different groups?"

### Limitations / Research Gap Identified

The study used cross-sectional DHS data, so the identified relationships should not automatically be interpreted as causal.

The study focused only on rural women, which limits its ability to represent all Nigerian women.

It also used the 2013 NDHS, so the findings may not represent patterns in the newer 2023–24 NDHS.

The research focused on associations rather than developing and evaluating a machine-learning prediction model.

Another important consideration is that some community-level variables were constructed by aggregating information from women within DHS communities rather than being simple variables directly available in the dataset.

Therefore, if I consider similar community-level predictors, I will need to determine carefully how they were constructed and whether they can be reproduced appropriately using the 2023–24 NDHS.

### Important Variables / Factors Examined

#### Individual-Level Factors

- Maternal education
- Parity
- Age at first birth
- Religion
- Healthcare decision-making
- Employment status
- Access to mass media
- Means of transportation

#### Community-Level Factors

- Community literacy
- Community poverty
- Community childcare burden
- Employment outside agriculture
- Community perception of distance to healthcare
- Geographical region

### Pre-Delivery Variables Only?

This was not specifically designed as a pre-delivery prediction study.

However, many of the characteristics examined could potentially be known before childbirth, including:

- Maternal education
- Parity
- Religion
- Healthcare decision-making
- Media exposure
- Transportation
- Community poverty
- Community literacy
- Geographical region

However, the timing and construction of every candidate variable will need to be checked carefully before it can be included in my proposed prediction model.

Community-level variables will require particular attention because some were derived by aggregating information from respondents within DHS communities.

### Model Evaluation

This was not primarily a machine-learning prediction study.

- Main analytical method: Mixed-effects logistic regression
- Individual-level analysis: Yes
- Community-level analysis: Yes
- Community clustering assessed: Yes, using Intra-Class Correlation
- Machine-learning model comparison: No
- Accuracy: Not a main evaluation
- Precision: Not a main evaluation
- Recall: Not a main evaluation
- F1-score: Not a main evaluation
- ROC-AUC: Not a main evaluation
- Calibration: Not a main evaluation
- SHAP/explainable ML: No
- Main focus: Individual and community factors associated with skilled assistance

### Verification Checklist

- [x] Original paper located
- [x] Abstract reviewed
- [x] Dataset and sample verified
- [x] Outcome definition verified
- [x] Individual-level variables verified
- [x] Community-level variables verified
- [x] Methods verified
- [x] Main findings verified
- [x] Full citation verified
- [x] Publication status checked

### Full Citation

Solanke, B. L., & Rahman, S. A. (2018). Multilevel analysis of factors associated with assistance during delivery in rural Nigeria: Implications for reducing rural-urban inequity in skilled care at delivery. BMC Pregnancy and Childbirth, 18, 438. https://doi.org/10.1186/s12884-018-2074-9

### DOI / Original Publication

https://doi.org/10.1186/s12884-018-2074-9

---

## Study 10: Adedini et al. (2017)

### Paper Title

Trends and Drivers of Skilled Birth Attendant Use in Nigeria (1990–2013): Policy Implications for Child and Maternal Health

### Publication Status

Peer-reviewed journal article.

### Country / Study Setting

Nigeria.

### Dataset

The study used data from four Nigeria Demographic and Health Survey rounds:

- 1990 NDHS
- 2003 NDHS
- 2008 NDHS
- 2013 NDHS

The study examined changes in skilled birth attendant use over time and factors associated with the use of skilled assistance during childbirth.

### Purpose of the Study

The study aimed to examine trends in the use of skilled birth attendants in Nigeria and identify factors associated with whether women used skilled assistance during childbirth.

The researchers were particularly interested in understanding the demographic, socioeconomic, geographical and women's empowerment characteristics associated with skilled birth attendant use.

### Methods Used

The researchers analysed nationally representative Nigeria DHS data from multiple survey years.

Descriptive analysis was used to examine changes in skilled birth attendant use over time.

Logistic regression analysis was used to investigate factors associated with skilled birth attendant utilisation while accounting for other characteristics.

The analysis considered factors such as:

- Maternal education
- Household wealth
- Religion
- Ethnicity
- Urban/rural residence
- Geopolitical zone
- Employment
- Antenatal care
- Birth order
- Women's involvement in healthcare decision-making

### Main Findings

Skilled birth attendant utilisation increased only modestly over the study period.

SBA use increased from approximately:

- 32.4% in 1990
- 38.5% in 2013

Maternal education was strongly associated with skilled birth attendant use.

Women with education had substantially higher odds of using skilled birth attendants than women without education.

The study reported an adjusted odds ratio of approximately 3.09 for education.

Geographical and sociocultural characteristics, including place of residence, geopolitical zone, religion and ethnicity, were also associated with skilled birth attendant use.

Women's involvement in healthcare decision-making was another important factor.

Women who participated in decisions concerning their healthcare were more likely to use skilled birth attendants.

### My Understanding

In simple terms, the researchers wanted to understand whether skilled birth attendance had improved in Nigeria over time and why some women were more likely to use skilled birth attendants than others.

They compared four Nigeria DHS surveys covering more than two decades.

Although skilled birth attendant use increased, the improvement was relatively small, from about 32.4% in 1990 to 38.5% in 2013.

Education was one of the important factors. Women with education were more likely to use skilled birth attendants.

Where women lived and their social circumstances also mattered.

Another important finding was women's involvement in healthcare decisions. Women who participated in decisions about their own healthcare were more likely to use skilled birth attendants.

This helped me understand that maternal healthcare utilisation may depend not only on education, wealth and healthcare access but also on whether women have the ability to participate in decisions concerning their own healthcare.

### Relevance to My Research

This study is highly relevant to my research because it focuses specifically on Nigeria, uses NDHS data and investigates skilled birth attendant use.

It provides additional Nigeria-specific evidence about characteristics that may be related to skilled birth attendance.

It also strengthens evidence from other studies I have reviewed showing the potential importance of women's autonomy and healthcare decision-making.

Studies 8 and 9 also identified women's autonomy or participation in healthcare decisions as relevant factors.

Therefore, when reviewing the 2023–24 NDHS variables, I should investigate whether appropriate decision-making or women's empowerment variables are available and whether they meet my pre-delivery requirement.

The study also provides historical context showing that skilled birth attendance in Nigeria has changed over time, supporting the importance of examining the newer 2023–24 NDHS rather than assuming that relationships identified in older surveys remain unchanged.

### Differences From My Research

This study focused mainly on trends and factors statistically associated with skilled birth attendant use.

It did not primarily develop a machine-learning prediction model.

The study used NDHS data up to 2013, whereas my proposed research will use the newer 2023–24 NDHS.

My proposed research will focus specifically on predicting non-use of skilled birth attendance using information that could reasonably be known before childbirth.

I also intend to compare predictive models, evaluate discrimination and calibration, use explainability methods and investigate whether model performance differs across important geographical and socioeconomic groups.

Therefore, this study mainly asks:

"How has skilled birth attendant use changed in Nigeria, and which characteristics are associated with its utilisation?"

My proposed research asks:

"How well can information available before childbirth predict non-use of skilled birth attendance using the 2023–24 NDHS?"

### Limitations / Research Gap Identified

The study used repeated cross-sectional DHS data rather than following the same women over time.

The identified associations should therefore not automatically be interpreted as causal relationships.

The study also relied on secondary and partly self-reported DHS information, which may be affected by recall or reporting bias.

The most recent survey included was the 2013 NDHS, so the study does not represent the situation captured by the newer 2023–24 NDHS.

The study focused mainly on statistical associations and trends rather than developing and evaluating a machine-learning prediction model.

For my research, another important issue is predictor timing.

Some maternal-history variables may appear useful for prediction, but I will need to verify exactly what each NDHS variable represents and whether that information would genuinely have been known before the specific delivery being predicted.

This is necessary to prevent data leakage.

### Important Variables / Factors Examined

Important factors included:

- Maternal education
- Household wealth
- Religion
- Ethnicity
- Urban/rural residence
- Geopolitical zone
- Employment
- Antenatal care
- Birth order
- Women's healthcare decision-making
- Previous maternal healthcare utilisation

### Pre-Delivery Variables Only?

This study was not specifically designed as a pre-delivery prediction study.

However, several characteristics examined could potentially be known before childbirth, including:

- Maternal education
- Household wealth
- Religion
- Ethnicity
- Residence
- Geopolitical zone
- Employment
- Antenatal care history
- Birth order
- Healthcare decision-making

Previous birth or healthcare history may also potentially provide pre-delivery information, but this will require careful checking.

For every candidate predictor, I will verify whether it refers to information that occurred before the specific delivery being predicted.

Variables referring to the same delivery or information only known during or after delivery will not be included in the main pre-delivery prediction model.

### Model Evaluation

This was not primarily a machine-learning prediction study.

- Main analytical approach: Descriptive analysis and logistic regression
- Machine-learning model comparison: No
- Accuracy: Not a main evaluation
- Precision: Not a main evaluation
- Recall: Not a main evaluation
- F1-score: Not a main evaluation
- ROC-AUC: Not a main evaluation
- PR-AUC: Not a main evaluation
- Calibration: Not a main evaluation
- SHAP/explainable ML: No
- Main focus: Trends and factors associated with skilled birth attendant use

### Verification Checklist

- [x] Original paper located
- [x] Abstract reviewed
- [x] DHS survey rounds verified
- [x] Outcome verified
- [x] Methods verified
- [x] Main findings verified
- [x] Important factors reviewed
- [x] Limitations reviewed
- [x] Full citation verified
- [x] Publication status checked

### Full Citation

Adedini, S. A., Odimegwu, C., Bamiwuye, O., Fadeyibi, O., & De Wet, N. (2017). Trends and drivers of skilled birth attendant use in Nigeria (1990–2013): Policy implications for child and maternal health. International Perspectives on Sexual and Reproductive Health, 43(1), 25–40.

### DOI / Original Publication

https://doi.org/10.1363/43e2417

---
## Study 11: Negash and Wubneh (2025)

### Paper Title

Skilled Birth Attendance and Its Associated Factors in Chad and Nigeria: A Multilevel Analysis of DHS Data

### Publication Status

Peer-reviewed research article published in PLOS Global Public Health.

### Country / Study Setting

Chad and Nigeria.

### Dataset

The study used recent Demographic and Health Survey data from Chad and Nigeria.

The researchers combined eligible observations from the two countries to investigate skilled birth attendance and factors associated with its use.

### Purpose of the Study

The study aimed to determine the prevalence of skilled birth attendance and identify individual-level and community-level factors associated with skilled birth attendance in Chad and Nigeria.

The researchers used a multilevel approach because women living within the same communities may share characteristics and healthcare environments that influence maternal healthcare utilisation.

### Methods Used

The researchers used multilevel logistic regression.

This allowed them to examine factors operating at both:

- Individual level
- Community level

The analysis considered demographic, socioeconomic, healthcare-use and community characteristics.

The researchers reported adjusted odds ratios with confidence intervals to identify factors independently associated with skilled birth attendance.

### Main Findings

Overall skilled birth attendance in the combined study population was approximately 41.9%.

Several characteristics were significantly associated with skilled birth attendance.

Antenatal care was particularly important.

Women who had antenatal care visits had substantially higher odds of receiving skilled birth attendance.

The study reported an adjusted odds ratio of approximately 5.56 for antenatal care.

Maternal education was also associated with higher skilled birth attendance.

Reported adjusted odds ratios included approximately:

- Primary education: 1.77
- Secondary education: 4.06

Household wealth was also associated with skilled birth attendance.

Women exposed to media had higher odds of skilled birth attendance, with an adjusted odds ratio of approximately 1.50.

Community-level education was also important, with an adjusted odds ratio of approximately 2.73.

Other factors relating to residence and healthcare accessibility were also associated with skilled birth attendance.

### My Understanding

In simple terms, the researchers wanted to understand why some women in Nigeria and Chad received skilled assistance during childbirth while others did not.

They looked not only at characteristics of individual women but also at characteristics of the communities in which the women lived.

The study found that antenatal care was strongly associated with skilled birth attendance.

Education, household wealth, media exposure and community education were also important.

This helped me understand that skilled birth attendance may be influenced by both a woman's personal circumstances and the wider environment in which she lives.

It also provides more recent evidence that factors such as antenatal care, education, wealth and community characteristics continue to be relevant when studying skilled birth attendance.

### Relevance to My Research

This study is highly relevant to my research because Nigeria was included, DHS data were used and the outcome was skilled birth attendance.

It also provides recent peer-reviewed evidence about individual and community characteristics associated with skilled birth attendance.

Several of the important characteristics identified could potentially be available before childbirth, including:

- Maternal education
- Household wealth
- Antenatal care
- Media exposure
- Residence
- Healthcare accessibility
- Community education

The findings therefore provide useful evidence for variables that I may investigate when reviewing the 2023–24 Nigeria DHS.

The study also reinforces evidence from earlier papers that contextual and community characteristics may provide useful information beyond individual-level characteristics.

### Differences From My Research

The study combined data from Chad and Nigeria rather than developing a Nigeria-only analysis.

It primarily focused on identifying factors statistically associated with skilled birth attendance using multilevel regression.

My proposed research will focus specifically on Nigeria using the 2023–24 NDHS.

My primary objective is to investigate whether information available before childbirth can predict non-use of skilled birth attendance.

I also intend to compare predictive models, evaluate discrimination and calibration, use explainability methods and investigate whether model performance differs across important geographical and socioeconomic groups.

Therefore, this study mainly asks:

"Which individual and community factors are associated with skilled birth attendance in Chad and Nigeria?"

My proposed research asks:

"How well can pre-delivery information predict non-use of skilled birth attendance specifically in Nigeria using the 2023–24 NDHS?"

### Limitations / Research Gap Identified

The study used cross-sectional DHS data, so associations should not automatically be interpreted as causal relationships.

Some DHS variables are based on self-reported information and may therefore be affected by recall or reporting bias.

The study combined Nigeria and Chad, meaning that the results do not represent a Nigeria-specific predictive model.

The study also focused primarily on association rather than developing and evaluating machine-learning models for prediction.

For my proposed research, another important issue is predictor timing.

Although antenatal care and several other characteristics could potentially be known before childbirth, I will need to define the prediction point carefully.

For example, the use of total antenatal care visits may be appropriate if prediction occurs late in pregnancy before delivery, but it would not be available if the intended prediction point were early pregnancy.

Therefore, the exact timing and definition of every candidate predictor will be reviewed before modelling.

### Important Variables / Factors Identified

Important factors included:

- Antenatal care
- Maternal education
- Household wealth
- Media exposure
- Place of residence
- Healthcare accessibility
- Community-level education
- Other individual and community characteristics

### Pre-Delivery Variables Only?

The study was not specifically designed as a pre-delivery prediction study.

However, several important characteristics could potentially be known before childbirth.

These include:

- Maternal education
- Household wealth
- Residence
- Media exposure
- Community education
- Healthcare accessibility

Antenatal care may also represent pre-delivery information, but its suitability depends on the exact prediction point used in my research.

Therefore, each variable will be assessed carefully to ensure that it was genuinely available before the delivery being predicted and does not introduce data leakage.

### Model Evaluation

This was not primarily a machine-learning prediction study.

- Main analytical method: Multilevel logistic regression
- Individual-level factors examined: Yes
- Community-level factors examined: Yes
- Machine-learning model comparison: No
- Accuracy: Not a main evaluation
- Precision: Not a main evaluation
- Recall: Not a main evaluation
- F1-score: Not a main evaluation
- ROC-AUC: Not a main evaluation
- PR-AUC: Not a main evaluation
- Calibration: Not a main evaluation
- SHAP/explainable ML: No
- Main focus: Factors associated with skilled birth attendance

### Verification Checklist

- [x] Original paper located
- [x] Abstract reviewed
- [x] Countries verified
- [x] DHS data source verified
- [x] Outcome verified
- [x] Methods verified
- [x] Main findings verified
- [x] Individual and community factors reviewed
- [x] Full citation verified
- [x] Publication status checked

### Full Citation

Negash, W. D., & Wubneh, H. D. (2025). Skilled birth attendance and its associated factors in Chad and Nigeria: A multilevel analysis of DHS data. PLOS Global Public Health.

### DOI / Original Publication

https://doi.org/10.1371/journal.pgph.0005290
---
## Study 12: Akpiroroh et al. (2026)

### Paper Title

Hierarchical Logistic Regression Analysis of Skilled Birth Attendance in Northern Nigeria Using Andersen’s Behavioural Model

### Publication Status

Peer-reviewed research article published in Discover Public Health.

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

The researchers collected primary survey data in July 2025 using a structured interviewer-administered questionnaire.

The study included 1,004 women aged 15–49 years who had experienced at least one live birth during the five years preceding the survey.

Women were recruited from rural and urban communities across the six selected northern Nigerian states.

### Purpose of the Study

The study aimed to examine factors associated with skilled birth service utilisation among women in Northern Nigeria.

The researchers investigated two related outcomes:

- Skilled birth attendance
- Place of delivery

Skilled birth attendance was defined as childbirth assisted by a trained health professional, regardless of where the delivery occurred.

Place of delivery was examined separately as health-facility delivery versus home delivery.

The researchers used Andersen’s Behavioural Model of Health Service Use to organise the factors that could influence maternal healthcare utilisation.

### Methods Used

The study used a cross-sectional analytical design.

Hierarchical logistic regression was used to examine factors associated with skilled birth attendance and place of delivery.

Andersen’s Behavioural Model organised explanatory variables into three groups:

1. Predisposing factors
2. Enabling factors
3. Need factors

Predisposing factors included characteristics such as:

- Maternal age
- Marital status
- Education
- Religion
- Place of residence
- Year of last birth

Enabling factors included:

- Women's occupation
- Personal and household income
- Partner's education
- Partner's occupation
- Family support
- Transportation
- Phone ownership
- Other healthcare-access characteristics

Need factors included:

- Antenatal care attendance
- Number of ANC visits
- Satisfaction with ANC
- Delivery complications
- Newborn complications

Variables were entered into the regression models hierarchically according to these conceptual groups.

### Main Findings

Overall, 72.8% of the women reported receiving skilled birth assistance, while 27.2% did not.

At the bivariate level, phone ownership and satisfaction with antenatal care were associated with healthcare delivery assistance.

However, some of these relationships were no longer statistically significant after adjustment for other characteristics.

In the hierarchical regression analysis, partner's education and previous place of delivery remained significantly associated with healthcare delivery assistance after adjustment.

For place of delivery, several characteristics showed associations before adjustment, including:

- Education
- Year of last delivery
- Partner's employment
- Settlement type
- Mode of transportation
- Phone ownership

After adjustment, year of last delivery and phone ownership remained significantly associated with place of delivery.

The researchers also found that adding enabling factors substantially improved the explanatory performance of the skilled birth-attendance model.

This suggested that household resources and access-related characteristics contributed important information beyond women's basic sociodemographic characteristics.

### My Understanding

In simple terms, the researchers wanted to understand why some women in Northern Nigeria received skilled assistance during childbirth while others did not.

Instead of putting all possible factors together without any structure, they organised them into three groups.

Predisposing factors describe a woman's background.

Enabling factors describe resources and circumstances that may make healthcare easier or harder to access.

Need factors describe pregnancy-related healthcare needs and experiences.

The researchers then added these groups to the statistical model step by step.

One important thing I learned from this paper is that a factor can appear important when examined by itself but become less important after other characteristics are considered.

For example, phone ownership and ANC satisfaction showed associations with skilled assistance in the initial analysis, but these associations did not remain significant after adjustment.

This reminds me that relationships between maternal-health characteristics can overlap and should be interpreted carefully.

### Relevance to My Research

This study is relevant to my research because it is a recent Nigeria-specific study examining skilled birth attendance.

It is particularly useful because it focuses on Northern Nigeria, where skilled birth attendance remains an important maternal-health challenge.

The study also provides a useful framework for thinking about potential predictors.

Rather than selecting variables simply because they are available, Andersen's Behavioural Model demonstrates how maternal-health characteristics can be organised into meaningful groups such as:

- Predisposing characteristics
- Enabling/access characteristics
- Need-related characteristics

This could help me organise and justify candidate variables when developing my own data dictionary.

The study also reinforces the importance of distinguishing skilled birth attendance from place of delivery. They are related outcomes, but they are not identical.

### Differences From My Research

This study did not use the Nigeria DHS.

It collected primary survey data from 1,004 women in six northern Nigerian states.

My proposed research will use the nationally representative 2023–24 Nigeria DHS.

The study was also limited to selected states in Northern Nigeria, whereas my proposed research will examine Nigeria nationally.

The researchers primarily used hierarchical logistic regression to investigate statistical associations.

My research will focus on prediction of non-use of skilled birth attendance using information available before childbirth.

I intend to compare predictive models, evaluate discrimination and calibration, use explainability methods and investigate model performance across important geographical and socioeconomic groups.

### Important Predictor-Timing Issue

One particularly important issue for my research is that this study used previous place of delivery as an important explanatory variable.

Whether a variable like this is appropriate for my prediction model depends entirely on which birth it refers to.

If it genuinely describes a delivery that occurred before the birth I am trying to predict, it could potentially represent valid maternal history.

However, if it refers to the same delivery whose skilled attendance is being predicted, it would not be available before that delivery and could introduce data leakage.

Therefore, I will not automatically copy predictors from this or any other study.

Every candidate predictor will be checked against the 2023–24 NDHS documentation to determine exactly what it measures and when that information became available.

### Limitations / Research Gap Identified

The study used a cross-sectional design, so the reported relationships should be interpreted as associations rather than causal effects.

The researchers used purposive and quota sampling rather than a nationally representative probability sample.

The study was conducted in six selected northern states and therefore should not automatically be generalised to all Nigerian women.

The sample size of 1,004 women was also much smaller than the nationally representative NDHS datasets used in several other studies reviewed.

The study focused primarily on explanatory association rather than predictive machine-learning performance.

It did not evaluate a national prediction model using the 2023–24 NDHS.

For my research, the paper is therefore most useful for understanding recent Northern Nigerian evidence and for providing a theoretical framework for organising possible predictors.

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
- Previous place of delivery
- Delivery complications

### Pre-Delivery Variables Only?

No.

The study was not specifically designed to create a model using only information available before the delivery being predicted.

Several variables could potentially represent pre-delivery information, including:

- Maternal age
- Education
- Religion
- Residence
- Income
- Partner's education
- Partner's employment
- Phone ownership
- Transportation
- Antenatal care information

However, some variables require particular caution.

Delivery complications and newborn complications would generally not be appropriate predictors for a model intended to make predictions before childbirth.

Previous place of delivery may or may not be appropriate depending on whether it refers to an earlier birth or the index delivery.

Therefore, predictor timing will need to be verified carefully in my proposed research.

### Model Evaluation

This was not primarily a machine-learning prediction study.

- Main analytical method: Hierarchical logistic regression
- Theoretical framework: Andersen's Behavioural Model of Health Service Use
- Predisposing factors examined: Yes
- Enabling factors examined: Yes
- Need factors examined: Yes
- Machine-learning model comparison: No
- Accuracy: Not reported as a main evaluation
- Precision: Not reported as a main evaluation
- Recall: Not reported as a main evaluation
- F1-score: Not reported as a main evaluation
- ROC-AUC: Not reported as a main evaluation
- PR-AUC: Not reported
- Calibration: Not reported as a main evaluation
- SHAP/explainable ML: No
- Main focus: Factors associated with SBA and place of delivery

### Verification Checklist

- [x] Original paper located
- [x] Abstract reviewed
- [x] Study location verified
- [x] Sample size verified
- [x] Data source verified
- [x] Outcome definitions verified
- [x] Methods verified
- [x] Main findings verified
- [x] Limitations reviewed
- [x] Full citation verified
- [x] Publication status checked

### Full Citation

Akpiroroh, E., Ebinim, H., Ajayi, M., Sabbath, U.-O., Jibril, J., Ehize, P., Ogunsanya, A., Unogu, C., Kolawole, D., Nto, S., Rauf, R., Ajibola, D., Atobatele, S., Sampson, S., & Okagbue, H. (2026). Hierarchical logistic regression analysis of skilled birth attendance in Northern Nigeria using Andersen's Behavioural Model. Discover Public Health, 23, 1512.

### DOI / Original Publication

https://doi.org/10.1186/s12982-026-02943-6

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
