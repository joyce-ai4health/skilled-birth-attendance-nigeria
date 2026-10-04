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

## 1. Introduction

## 1. Introduction / Background

Maternal health remains an important public-health priority because pregnancy and childbirth can involve complications that require timely recognition and appropriate care. One important component of safe childbirth is access to skilled health personnel who have the competencies required to provide appropriate care during labour and delivery and to identify, manage or refer women and newborns when complications occur. Skilled birth attendance is therefore recognised internationally as an important indicator of maternal healthcare coverage and is included as Sustainable Development Goal (SDG) indicator 3.1.2 (World Health Organization [WHO], n.d.).

Despite the importance of skilled care during childbirth, access remains uneven in Nigeria. According to the 2024 Nigeria Demographic and Health Survey (NDHS), among live births in the two years before the survey, 46% were assisted by a skilled provider, most commonly a nurse or midwife. During the same period, 43% of live births occurred in a health facility, while 56% occurred at home (National Population Commission [NPC] & ICF, 2025). These national figures also conceal substantial socioeconomic inequalities. Home delivery was reported for 82% of births among women with no education and 82% among women in the poorest households (NPC & ICF, 2025). These patterns demonstrate that access to skilled childbirth care remains an important maternal-health challenge in Nigeria.

Previous Nigerian research has identified several characteristics associated with skilled birth attendance, including maternal education, household wealth, geographical location, urban or rural residence, antenatal care, healthcare accessibility, media exposure and women's participation in healthcare decision-making (Adedini et al., 2017; Doctor et al., 2020). These studies have contributed substantially to understanding patterns and inequalities in maternal healthcare utilisation. However, much of the Nigeria-specific literature has focused on explaining which characteristics are statistically associated with skilled birth attendance rather than determining whether available information can be used to identify women who may be at risk of giving birth without skilled attendance before childbirth occurs.

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

### Methodology References for This Section

Efthimiou, O., Seo, M., Chalkou, K., Debray, T., Egger, M., Salanti, G., et al. (2024). Developing clinical prediction models: A step-by-step guide. *BMJ, 386*, e078276. https://doi.org/10.1136/bmj-2023-078276

Saito, T., & Rehmsmeier, M. (2015). The precision-recall plot is more informative than the ROC plot when evaluating binary classifiers on imbalanced datasets. *PLOS ONE, 10*(3), e0118432. https://doi.org/10.1371/journal.pone.0118432


# Research Proposal

## Project Title

Predicting Non-Use of Skilled Birth Attendance in Nigeria Using Pre-Delivery Information: Evidence from the 2024 Nigeria Demographic and Health Survey

## Author 

- Intern Name(s): Joyce Ebruphiyo Etata
- Intern ID: DF-2026-181
- Intern Email: joyceebrusetata@gmail.com
- Programme: Dataraflow  Internship
- Date: October 2026

---

## Abstract

*To be completed after the main proposal. Target: 200–300 words.*

---

## 1. Introduction

*To be completed. Target: 500–800 words.*

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

### Methodology References for This Section

Efthimiou, O., Seo, M., Chalkou, K., Debray, T., Egger, M., Salanti, G., et al. (2024). Developing clinical prediction models: A step-by-step guide. *BMJ, 386*, e078276. https://doi.org/10.1136/bmj-2023-078276

Saito, T., & Rehmsmeier, M. (2015). The precision-recall plot is more informative than the ROC plot when evaluating binary classifiers on imbalanced datasets. *PLOS ONE, 10*(3), e0118432. https://doi.org/10.1371/journal.pone.0118432


# Research Proposal

## Project Title

Predicting Non-Use of Skilled Birth Attendance in Nigeria Using Pre-Delivery Information: Evidence from the 2024 Nigeria Demographic and Health Survey

## Author 

- Intern Name(s): Joyce Ebruphiyo Etata
- Intern ID: DF-2026-181
- Intern Email: joyceebrusetata@gmail.com
- Programme: Dataraflow  Internship
- Date: October 2026

---

## Abstract

*To be completed after the main proposal. Target: 200–300 words.*

---

## 1. Introduction

*To be completed. Target: 500–800 words.*

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

### Methodology References for This Section

Efthimiou, O., Seo, M., Chalkou, K., Debray, T., Egger, M., Salanti, G., et al. (2024). Developing clinical prediction models: A step-by-step guide. *BMJ, 386*, e078276. https://doi.org/10.1136/bmj-2023-078276

Saito, T., & Rehmsmeier, M. (2015). The precision-recall plot is more informative than the ROC plot when evaluating binary classifiers on imbalanced datasets. *PLOS ONE, 10*(3), e0118432. https://doi.org/10.1371/journal.pone.0118432


# Research Proposal

## Project Title

Predicting Non-Use of Skilled Birth Attendance in Nigeria Using Pre-Delivery Information: Evidence from the 2024 Nigeria Demographic and Health Survey

## Author 

- Intern Name(s): Joyce Ebruphiyo Etata
- Intern ID: DF-2026-181
- Intern Email: joyceebrusetata@gmail.com
- Programme: Dataraflow  Internship
- Date: October 2026

---

## Abstract

*To be completed after the main proposal. Target: 200–300 words.*

---

## 1. Introduction

*To be completed. Target: 500–800 words.*

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

### Methodology References for This Section

Efthimiou, O., Seo, M., Chalkou, K., Debray, T., Egger, M., Salanti, G., et al. (2024). Developing clinical prediction models: A step-by-step guide. *BMJ, 386*, e078276. https://doi.org/10.1136/bmj-2023-078276

Saito, T., & Rehmsmeier, M. (2015). The precision-recall plot is more informative than the ROC plot when evaluating binary classifiers on imbalanced datasets. *PLOS ONE, 10*(3), e0118432. https://doi.org/10.1371/journal.pone.0118432


### 2.5 Validation, Survey Structure and Subgroup Performance

The Nigeria Demographic and Health Survey uses a complex sampling design in which respondents are sampled within geographical clusters. Women living within the same communities may share healthcare environments, socioeconomic conditions and other contextual characteristics. Previous multilevel studies of skilled birth attendance have also demonstrated the importance of community-level variation.

This clustered structure is relevant when developing and evaluating prediction models. Prediction-model methodology for clustered datasets emphasises that clustering should be considered during model development and validation because model performance may vary across clusters and populations (Debray et al., 2023).

The reviewed machine-learning studies used validation approaches including train-test splitting and cross-validation. However, the appropriateness of a validation strategy depends on the intended use of the prediction model and the structure of the data. Randomly dividing individuals from the same clustered dataset between development and validation samples may provide limited information about how well a model generalises to different clusters or settings. Cluster-based approaches can instead evaluate performance while preserving the clustered structure of the data (Debray et al., 2023).

Internal-external cross-validation is one approach described for clustered prediction data. In this approach, a model is repeatedly developed using all clusters except one and evaluated in the cluster that was left out. Repeating the process across clusters can provide information about variation in model performance and its potential generalisability across different settings (Debray et al., 2023). However, the exact validation strategy for the proposed research will be determined after examining the structure, number and distribution of clusters in the 2023–24 NDHS.

Subgroup performance is also important. Previous Nigerian research has demonstrated substantial differences in skilled birth attendance according to geographical region, urban or rural residence, household wealth, education and healthcare accessibility. Strong overall predictive performance may therefore conceal weaker performance within particular population groups.

Where sample sizes permit, the proposed research will examine model performance across important geographical and socioeconomic subgroups. This will help determine whether discrimination and calibration are reasonably consistent across different sections of the Nigerian population rather than relying solely on overall model performance.

### Methodology Reference for This Section

Debray, T. P. A., et al. (2023). Transparent reporting of multivariable prediction models developed or validated using clustered data (TRIPOD-Cluster): Explanation and elaboration. *BMJ, 380*, e071058. https://doi.org/10.1136/bmj-2022-071058

### 2.6 Research Gap

Existing research provides substantial evidence regarding factors associated with skilled birth attendance in Nigeria, while recent studies demonstrate that machine-learning methods can be applied to DHS maternal-health data. The reviewed literature therefore does not support a broad claim that machine learning has never been used for skilled birth attendance or Nigerian maternal-health research.

Instead, a more specific gap emerges from the combination of dataset recency, prediction target, predictor timing and model-evaluation approach.

Much of the Nigeria-specific skilled birth attendance literature has focused on identifying statistical associations using regression or multilevel methods. Machine-learning studies of skilled birth attendance have demonstrated predictive potential, but some have included variables whose timing may not correspond to a realistic pre-delivery prediction setting. Furthermore, calibration, clustered validation and subgroup performance have not been addressed consistently across the reviewed prediction studies.

Among the studies reviewed, limited evidence was identified of a Nigeria-specific prediction study using the 2023–24 Nigeria Demographic and Health Survey to predict **non-use of skilled birth attendance** while restricting the primary prediction model to information that would reasonably be available at a clearly defined point before the delivery being predicted.

The proposed research will address this gap by investigating whether non-use of skilled birth attendance can be predicted using the 2023–24 NDHS and carefully selected pre-delivery information. An interpretable baseline model will be compared with appropriate machine-learning approaches. Model evaluation will consider discrimination, class-specific performance and calibration. Explainability methods will be used where appropriate to identify influential predictors, while the clustered survey structure and performance across important geographical and socioeconomic groups will also be considered.

The contribution of the proposed study is therefore not simply the use of machine learning. Its main contribution is the development and evaluation of a prediction framework centred on a realistic **pre-delivery decision point**, using recent nationally representative Nigerian data and explicitly considering predictor timing, probability reliability and variation in predictive performance across relevant population groups.

---

## 3. Problem Statement

*To be completed. Target: 150–300 words.*

---

## 4. Research Questions and Hypotheses

*To be completed.*

---

## 5. Research Objectives

### 5.1 General Objective

*To be completed.*

### 5.2 Specific Objectives

*To be completed. Approximately 3–5 specific objectives.*

---

## 6. Methodology

### 6.1 Research Design

*To be completed.*

### 6.2 Data Source, Study Population and Sampling

*To be completed.*

### 6.3 Outcome Definition

*To be completed.*

### 6.4 Pre-Delivery Prediction Point and Candidate Predictors

*To be completed.*

### 6.5 Data Preprocessing and Feature Engineering

*To be completed.*

### 6.6 Candidate Models

*To be completed.*

### 6.7 Validation and Experimental Protocol

*To be completed.*

### 6.8 Evaluation Metrics

*To be completed.*

### 6.9 Model Interpretation

*To be completed.*

### 6.10 Subgroup Performance Assessment

*To be completed.*

### 6.11 Ethical Considerations and Approvals

*To be completed.*

### 6.12 Reproducibility and Code/Data Release

*To be completed.*

---

## 7. Significance and Expected Contribution

*To be completed.*

---

## 8. Limitations and Scope

*To be completed.*

---

## 9. Implementation Plan and Repository Structure

*To be completed.*

---

## 10. Timeline

*To be completed. A phased table or Gantt chart will be added.*

---

## 11. References

*To be completed. All references will be verified against the original publications before the final proposal is submitted.* 2.5 Validation, Survey Structure and Subgroup Performance

The Nigeria Demographic and Health Survey uses a complex sampling design in which respondents are sampled within geographical clusters. Women living within the same communities may share healthcare environments, socioeconomic conditions and other contextual characteristics. Previous multilevel studies of skilled birth attendance have also demonstrated the importance of community-level variation.

This clustered structure is relevant when developing and evaluating prediction models. Prediction-model methodology for clustered datasets emphasises that clustering should be considered during model development and validation because model performance may vary across clusters and populations (Debray et al., 2023).

The reviewed machine-learning studies used validation approaches including train-test splitting and cross-validation. However, the appropriateness of a validation strategy depends on the intended use of the prediction model and the structure of the data. Randomly dividing individuals from the same clustered dataset between development and validation samples may provide limited information about how well a model generalises to different clusters or settings. Cluster-based approaches can instead evaluate performance while preserving the clustered structure of the data (Debray et al., 2023).

Internal-external cross-validation is one approach described for clustered prediction data. In this approach, a model is repeatedly developed using all clusters except one and evaluated in the cluster that was left out. Repeating the process across clusters can provide information about variation in model performance and its potential generalisability across different settings (Debray et al., 2023). However, the exact validation strategy for the proposed research will be determined after examining the structure, number and distribution of clusters in the 2023–24 NDHS.

Subgroup performance is also important. Previous Nigerian research has demonstrated substantial differences in skilled birth attendance according to geographical region, urban or rural residence, household wealth, education and healthcare accessibility. Strong overall predictive performance may therefore conceal weaker performance within particular population groups.

Where sample sizes permit, the proposed research will examine model performance across important geographical and socioeconomic subgroups. This will help determine whether discrimination and calibration are reasonably consistent across different sections of the Nigerian population rather than relying solely on overall model performance.

### Methodology Reference for This Section

Debray, T. P. A., et al. (2023). Transparent reporting of multivariable prediction models developed or validated using clustered data (TRIPOD-Cluster): Explanation and elaboration. *BMJ, 380*, e071058. https://doi.org/10.1136/bmj-2022-071058

### 2.6 Research Gap

Existing research provides substantial evidence regarding factors associated with skilled birth attendance in Nigeria, while recent studies demonstrate that machine-learning methods can be applied to DHS maternal-health data. The reviewed literature therefore does not support a broad claim that machine learning has never been used for skilled birth attendance or Nigerian maternal-health research.

Instead, a more specific gap emerges from the combination of dataset recency, prediction target, predictor timing and model-evaluation approach.

Much of the Nigeria-specific skilled birth attendance literature has focused on identifying statistical associations using regression or multilevel methods. Machine-learning studies of skilled birth attendance have demonstrated predictive potential, but some have included variables whose timing may not correspond to a realistic pre-delivery prediction setting. Furthermore, calibration, clustered validation and subgroup performance have not been addressed consistently across the reviewed prediction studies.

Among the studies reviewed, limited evidence was identified of a Nigeria-specific prediction study using the 2023–24 Nigeria Demographic and Health Survey to predict **non-use of skilled birth attendance** while restricting the primary prediction model to information that would reasonably be available at a clearly defined point before the delivery being predicted.

The proposed research will address this gap by investigating whether non-use of skilled birth attendance can be predicted using the 2023–24 NDHS and carefully selected pre-delivery information. An interpretable baseline model will be compared with appropriate machine-learning approaches. Model evaluation will consider discrimination, class-specific performance and calibration. Explainability methods will be used where appropriate to identify influential predictors, while the clustered survey structure and performance across important geographical and socioeconomic groups will also be considered.

The contribution of the proposed study is therefore not simply the use of machine learning. Its main contribution is the development and evaluation of a prediction framework centred on a realistic **pre-delivery decision point**, using recent nationally representative Nigerian data and explicitly considering predictor timing, probability reliability and variation in predictive performance across relevant population groups.

---

## 3. Problem Statement

*To be completed. Target: 150–300 words.*

---

## 4. Research Questions and Hypotheses

*To be completed.*

---

## 5. Research Objectives

### 5.1 General Objective

*To be completed.*

### 5.2 Specific Objectives

*To be completed. Approximately 3–5 specific objectives.*

---

## 6. Methodology

### 6.1 Research Design

*To be completed.*

### 6.2 Data Source, Study Population and Sampling

*To be completed.*

### 6.3 Outcome Definition

*To be completed.*

### 6.4 Pre-Delivery Prediction Point and Candidate Predictors

*To be completed.*

### 6.5 Data Preprocessing and Feature Engineering

*To be completed.*

### 6.6 Candidate Models

*To be completed.*

### 6.7 Validation and Experimental Protocol

*To be completed.*

### 6.8 Evaluation Metrics

*To be completed.*

### 6.9 Model Interpretation

*To be completed.*

### 6.10 Subgroup Performance Assessment

*To be completed.*

### 6.11 Ethical Considerations and Approvals

*To be completed.*

### 6.12 Reproducibility and Code/Data Release

*To be completed.*

---

## 7. Significance and Expected Contribution

*To be completed.*

---

## 8. Limitations and Scope

*To be completed.*

---

## 9. Implementation Plan and Repository Structure

*To be completed.*

---

## 10. Timeline

*To be completed. A phased table or Gantt chart will be added.*

---

## 11. References

*To be completed. All references will be verified against the original publications before the final proposal is submitted.* 2.5 Validation, Survey Structure and Subgroup Performance

The Nigeria Demographic and Health Survey uses a complex sampling design in which respondents are sampled within geographical clusters. Women living within the same communities may share healthcare environments, socioeconomic conditions and other contextual characteristics. Previous multilevel studies of skilled birth attendance have also demonstrated the importance of community-level variation.

This clustered structure is relevant when developing and evaluating prediction models. Prediction-model methodology for clustered datasets emphasises that clustering should be considered during model development and validation because model performance may vary across clusters and populations (Debray et al., 2023).

The reviewed machine-learning studies used validation approaches including train-test splitting and cross-validation. However, the appropriateness of a validation strategy depends on the intended use of the prediction model and the structure of the data. Randomly dividing individuals from the same clustered dataset between development and validation samples may provide limited information about how well a model generalises to different clusters or settings. Cluster-based approaches can instead evaluate performance while preserving the clustered structure of the data (Debray et al., 2023).

Internal-external cross-validation is one approach described for clustered prediction data. In this approach, a model is repeatedly developed using all clusters except one and evaluated in the cluster that was left out. Repeating the process across clusters can provide information about variation in model performance and its potential generalisability across different settings (Debray et al., 2023). However, the exact validation strategy for the proposed research will be determined after examining the structure, number and distribution of clusters in the 2023–24 NDHS.

Subgroup performance is also important. Previous Nigerian research has demonstrated substantial differences in skilled birth attendance according to geographical region, urban or rural residence, household wealth, education and healthcare accessibility. Strong overall predictive performance may therefore conceal weaker performance within particular population groups.

Where sample sizes permit, the proposed research will examine model performance across important geographical and socioeconomic subgroups. This will help determine whether discrimination and calibration are reasonably consistent across different sections of the Nigerian population rather than relying solely on overall model performance.

### Methodology Reference for This Section

Debray, T. P. A., et al. (2023). Transparent reporting of multivariable prediction models developed or validated using clustered data (TRIPOD-Cluster): Explanation and elaboration. *BMJ, 380*, e071058. https://doi.org/10.1136/bmj-2022-071058

### 2.6 Research Gap

Existing research provides substantial evidence regarding factors associated with skilled birth attendance in Nigeria, while recent studies demonstrate that machine-learning methods can be applied to DHS maternal-health data. The reviewed literature therefore does not support a broad claim that machine learning has never been used for skilled birth attendance or Nigerian maternal-health research.

Instead, a more specific gap emerges from the combination of dataset recency, prediction target, predictor timing and model-evaluation approach.

Much of the Nigeria-specific skilled birth attendance literature has focused on identifying statistical associations using regression or multilevel methods. Machine-learning studies of skilled birth attendance have demonstrated predictive potential, but some have included variables whose timing may not correspond to a realistic pre-delivery prediction setting. Furthermore, calibration, clustered validation and subgroup performance have not been addressed consistently across the reviewed prediction studies.

Among the studies reviewed, limited evidence was identified of a Nigeria-specific prediction study using the 2023–24 Nigeria Demographic and Health Survey to predict **non-use of skilled birth attendance** while restricting the primary prediction model to information that would reasonably be available at a clearly defined point before the delivery being predicted.

The proposed research will address this gap by investigating whether non-use of skilled birth attendance can be predicted using the 2023–24 NDHS and carefully selected pre-delivery information. An interpretable baseline model will be compared with appropriate machine-learning approaches. Model evaluation will consider discrimination, class-specific performance and calibration. Explainability methods will be used where appropriate to identify influential predictors, while the clustered survey structure and performance across important geographical and socioeconomic groups will also be considered.

The contribution of the proposed study is therefore not simply the use of machine learning. Its main contribution is the development and evaluation of a prediction framework centred on a realistic **pre-delivery decision point**, using recent nationally representative Nigerian data and explicitly considering predictor timing, probability reliability and variation in predictive performance across relevant population groups.

---

## 3. Problem Statement

*To be completed. Target: 150–300 words.*

---

## 4. Research Questions and Hypotheses

*To be completed.*

---

## 5. Research Objectives

### 5.1 General Objective

*To be completed.*

### 5.2 Specific Objectives

*To be completed. Approximately 3–5 specific objectives.*

---

## 6. Methodology

### 6.1 Research Design

*To be completed.*

### 6.2 Data Source, Study Population and Sampling

*To be completed.*

### 6.3 Outcome Definition

*To be completed.*

### 6.4 Pre-Delivery Prediction Point and Candidate Predictors

*To be completed.*

### 6.5 Data Preprocessing and Feature Engineering

*To be completed.*

### 6.6 Candidate Models

*To be completed.*

### 6.7 Validation and Experimental Protocol

*To be completed.*

### 6.8 Evaluation Metrics

*To be completed.*

### 6.9 Model Interpretation

*To be completed.*

### 6.10 Subgroup Performance Assessment

*To be completed.*

### 6.11 Ethical Considerations and Approvals

*To be completed.*

### 6.12 Reproducibility and Code/Data Release

*To be completed.*

---

## 7. Significance and Expected Contribution

*To be completed.*

---

## 8. Limitations and Scope

*To be completed.*

---

## 9. Implementation Plan and Repository Structure

*To be completed.*

---

## 10. Timeline

*To be completed. A phased table or Gantt chart will be added.*

---

## 11. References

*To be completed. All references will be verified against the original publications before the final proposal is submitted.* 2.5 Validation, Survey Structure and Subgroup Performance

The Nigeria Demographic and Health Survey uses a complex sampling design in which respondents are sampled within geographical clusters. Women living within the same communities may share healthcare environments, socioeconomic conditions and other contextual characteristics. Previous multilevel studies of skilled birth attendance have also demonstrated the importance of community-level variation.

This clustered structure is relevant when developing and evaluating prediction models. Prediction-model methodology for clustered datasets emphasises that clustering should be considered during model development and validation because model performance may vary across clusters and populations (Debray et al., 2023).

The reviewed machine-learning studies used validation approaches including train-test splitting and cross-validation. However, the appropriateness of a validation strategy depends on the intended use of the prediction model and the structure of the data. Randomly dividing individuals from the same clustered dataset between development and validation samples may provide limited information about how well a model generalises to different clusters or settings. Cluster-based approaches can instead evaluate performance while preserving the clustered structure of the data (Debray et al., 2023).

Internal-external cross-validation is one approach described for clustered prediction data. In this approach, a model is repeatedly developed using all clusters except one and evaluated in the cluster that was left out. Repeating the process across clusters can provide information about variation in model performance and its potential generalisability across different settings (Debray et al., 2023). However, the exact validation strategy for the proposed research will be determined after examining the structure, number and distribution of clusters in the 2023–24 NDHS.

Subgroup performance is also important. Previous Nigerian research has demonstrated substantial differences in skilled birth attendance according to geographical region, urban or rural residence, household wealth, education and healthcare accessibility. Strong overall predictive performance may therefore conceal weaker performance within particular population groups.

Where sample sizes permit, the proposed research will examine model performance across important geographical and socioeconomic subgroups. This will help determine whether discrimination and calibration are reasonably consistent across different sections of the Nigerian population rather than relying solely on overall model performance.

### Methodology Reference for This Section

Debray, T. P. A., et al. (2023). Transparent reporting of multivariable prediction models developed or validated using clustered data (TRIPOD-Cluster): Explanation and elaboration. *BMJ, 380*, e071058. https://doi.org/10.1136/bmj-2022-071058

### 2.6 Research Gap

Existing research provides substantial evidence regarding factors associated with skilled birth attendance in Nigeria, while recent studies demonstrate that machine-learning methods can be applied to DHS maternal-health data. The reviewed literature therefore does not support a broad claim that machine learning has never been used for skilled birth attendance or Nigerian maternal-health research.

Instead, a more specific gap emerges from the combination of dataset recency, prediction target, predictor timing and model-evaluation approach.

Much of the Nigeria-specific skilled birth attendance literature has focused on identifying statistical associations using regression or multilevel methods. Machine-learning studies of skilled birth attendance have demonstrated predictive potential, but some have included variables whose timing may not correspond to a realistic pre-delivery prediction setting. Furthermore, calibration, clustered validation and subgroup performance have not been addressed consistently across the reviewed prediction studies.

Among the studies reviewed, limited evidence was identified of a Nigeria-specific prediction study using the 2023–24 Nigeria Demographic and Health Survey to predict **non-use of skilled birth attendance** while restricting the primary prediction model to information that would reasonably be available at a clearly defined point before the delivery being predicted.

The proposed research will address this gap by investigating whether non-use of skilled birth attendance can be predicted using the 2023–24 NDHS and carefully selected pre-delivery information. An interpretable baseline model will be compared with appropriate machine-learning approaches. Model evaluation will consider discrimination, class-specific performance and calibration. Explainability methods will be used where appropriate to identify influential predictors, while the clustered survey structure and performance across important geographical and socioeconomic groups will also be considered.

The contribution of the proposed study is therefore not simply the use of machine learning. Its main contribution is the development and evaluation of a prediction framework centred on a realistic **pre-delivery decision point**, using recent nationally representative Nigerian data and explicitly considering predictor timing, probability reliability and variation in predictive performance across relevant population groups.

---

## 3. Problem Statement

*To be completed. Target: 150–300 words.*

---

## 4. Research Questions and Hypotheses

*To be completed.*

---

## 5. Research Objectives

### 5.1 General Objective

*To be completed.*

### 5.2 Specific Objectives

*To be completed. Approximately 3–5 specific objectives.*

---

## 6. Methodology

### 6.1 Research Design

*To be completed.*

### 6.2 Data Source, Study Population and Sampling

*To be completed.*

### 6.3 Outcome Definition

*To be completed.*

### 6.4 Pre-Delivery Prediction Point and Candidate Predictors

*To be completed.*

### 6.5 Data Preprocessing and Feature Engineering

*To be completed.*

### 6.6 Candidate Models

*To be completed.*

### 6.7 Validation and Experimental Protocol

*To be completed.*

### 6.8 Evaluation Metrics

*To be completed.*

### 6.9 Model Interpretation

*To be completed.*

### 6.10 Subgroup Performance Assessment

*To be completed.*

### 6.11 Ethical Considerations and Approvals

*To be completed.*

### 6.12 Reproducibility and Code/Data Release

*To be completed.*

---

## 7. Significance and Expected Contribution

*To be completed.*

---

## 8. Limitations and Scope

*To be completed.*

---

## 9. Implementation Plan and Repository Structure

*To be completed.*

---

## 10. Timeline

*To be completed. A phased table or Gantt chart will be added.*

---

## 11. References

*To be completed. All references will be verified against the original publications before the final proposal is submitted.*
