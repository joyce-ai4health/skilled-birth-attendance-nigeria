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
## Review Progress

- [x] Study 1
- [x] Study 2
- [x] Study 3
- [x] Study 4
- [x] Study 5
- [x] Study 6
- [ ] Study 7
- [ ] Study 8
- [ ] Study 9
- [ ] Study 10
- [ ] Study 11
- [ ] Study 12
