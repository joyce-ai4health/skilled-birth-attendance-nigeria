
## Cross-Study Summary

The 12 studies reviewed provide a broad picture of what is already known about skilled birth attendance in Nigeria and related maternal healthcare prediction.

### Overall Evidence

The studies consistently show that skilled birth attendance is influenced by a combination of individual, household, healthcare-access, geographical and community characteristics.

Factors that appeared repeatedly across the literature included:

* Maternal education
* Household wealth
* Urban/rural residence
* Geographical region
* Antenatal care
* Healthcare accessibility
* Media exposure
* Maternal age
* Birth order or parity
* Women's healthcare decision-making and autonomy
* Partner and household characteristics
* Community-level socioeconomic characteristics

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

* Random Forest
* XGBoost
* LightGBM
* Logistic regression
* Feature-selection techniques
* Class-imbalance methods
* SHAP for model interpretation

Some studies reported strong predictive performance.

However, high predictive performance alone does not mean that a model is appropriate for use before childbirth.

The timing of the predictors used to obtain that performance is also important.

### Predictor Timing and Data Leakage

One of the most important issues identified during this review was predictor timing.

My proposed research aims to predict non-use of skilled birth attendance using information that could reasonably be available before the delivery being predicted.

However, some previous studies included variables that may be known only at delivery, after delivery, or later in pregnancy.

Examples requiring particular caution include:

* Actual place of delivery
* Delivery complications
* Newborn complications
* Final number of antenatal care visits
* Some variables describing previous or last place of birth

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

* Accuracy
* Precision
* Recall
* F1-score
* ROC-AUC
* PR-AUC

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

* Geographical region
* Urban/rural residence
* Household wealth
* Education
* Healthcare accessibility

This means that strong overall model performance may hide weaker performance within particular population groups.

My proposed research should therefore investigate model performance across important geographical and socioeconomic groups where sample sizes permit.

This will help determine whether the model performs consistently across different parts of the Nigerian population.

### Evidence From the 2023–24 NDHS

The literature review identified recent machine-learning research using newer Nigeria DHS data for maternal-health outcomes.

Therefore, my research should not claim that machine learning has never been applied to recent Nigeria DHS data.

Instead, the important question is whether the specific combination proposed in my research has been adequately addressed:

* Nigeria-specific analysis
* 2023–24 NDHS
* Non-use of skilled birth attendance as the prediction target
* Predictors selected according to a clearly defined pre-delivery prediction point
* Comparison of predictive models
* Evaluation of discrimination and calibration
* Explainability
* Consideration of geographical and socioeconomic subgroup performance
* Appropriate consideration of the clustered survey structure

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

* Focusing specifically on **non-use of skilled birth attendance in Nigeria**.
* Using the **2023–24 Nigeria Demographic and Health Survey**.
* Defining a clear **pre-delivery prediction point** before final predictor selection.
* Excluding variables that would not realistically be known at that prediction point.
* Comparing an interpretable baseline model with appropriate machine-learning models.
* Evaluating performance using more than overall accuracy.
* Assessing discrimination using measures such as ROC-AUC and PR-AUC.
* Evaluating precision, recall and F1-score, with particular attention to the non-SBA group.
* Assessing the calibration of predicted probabilities.
* Using explainability methods, where appropriate, to understand influential predictors.
* Considering the clustered structure of the NDHS during model development and validation.
* Examining performance across important geographical and socioeconomic groups where sufficient data are available.

### Research Contribution

The main contribution of this research is therefore not simply the use of machine learning.

Its contribution is the development and evaluation of a prediction approach that is designed around a realistic **pre-delivery decision point**.

By ensuring that the primary model uses only information that could reasonably be available before the childbirth outcome occurs, the study aims to produce a more realistic assessment of whether women at risk of non-use of skilled birth attendance can be identified in advance.

The study will also provide updated evidence using the 2023–24 NDHS and assess not only whether the models can distinguish between women at different levels of risk, but also whether their predicted probabilities are reliable and whether performance is reasonably consistent across important population groups.

---

# 2. Literature Review

## 2.1 Skilled Birth Attendance and Maternal Healthcare Utilisation

Skilled birth attendance is an important component of maternal healthcare because access to appropriately trained health professionals during childbirth can support the recognition and management of complications. In Nigeria, previous research has consistently shown that the use of skilled birth attendants is influenced by a combination of individual, household, healthcare-access, geographical and community characteristics.

Nigeria-specific studies using Demographic and Health Survey data have repeatedly identified maternal education, household wealth, place of residence, geographical region, healthcare accessibility, antenatal care, media exposure, parity and women's participation in healthcare decision-making as important factors associated with skilled birth attendance. The recurrence of these characteristics across studies suggests that non-use of skilled birth attendance cannot be adequately understood through a single individual-level factor. Instead, maternal healthcare utilisation reflects a combination of socioeconomic circumstances, healthcare access and the broader environment in which women live.

Solanke and Rahman (2018), for example, examined assistance during delivery among rural Nigerian women using the 2013 Nigeria Demographic and Health Survey. Their multilevel analysis demonstrated the importance of considering both individual and community characteristics. Maternal education, parity, religion, participation in healthcare decision-making, access to mass media and means of transportation were among the relevant individual-level factors, while community literacy, poverty, perceived distance to healthcare and geographical region were also important. The study therefore demonstrates that maternal healthcare utilisation may be influenced not only by a woman's individual circumstances but also by the community in which she lives.

Fagbamigbe and Oyedele (2022) further examined trends, inequalities and drivers of change in skilled birth attendant utilisation across five Nigeria DHS rounds from 1990 to 2018. Skilled birth attendant use remained relatively low despite improvement over time. Their multivariate decomposition analysis showed that 11.5% of the change between 2003 and 2018 was attributable to differences in population characteristics, while 88.5% was attributable to differences in the effects of those characteristics. Women's participation in healthcare decision-making and rural population characteristics were among the important contributors to changes in skilled birth attendant utilisation.

More recent Nigeria-specific evidence also indicates substantial inequalities in skilled birth attendance. In a recent preprint, Unegbu (2026), using the 2018 NDHS, reported a weighted skilled birth attendance prevalence of 44.9%, with considerable regional variation. Skilled birth attendance ranged from 17.7% in the North West to 85.6% in the South West. These geographical differences reinforce the importance of considering regional context when studying skilled birth attendance in Nigeria.

Taken together, these studies provide substantial evidence about factors associated with skilled birth attendance. However, much of the Nigeria-specific literature has primarily addressed an explanatory question— which characteristics are associated with skilled birth attendance? — rather than a predictive question concerning whether women at risk of non-use can be identified before childbirth.

## 2.2 Machine Learning for Predicting Skilled Birth Attendance

Recent research has increasingly explored whether machine-learning methods can be used to predict skilled birth attendance and related maternal-health outcomes using DHS data. These studies extend conventional association-based analyses by developing predictive models and evaluating how accurately they distinguish between women with different maternal healthcare outcomes.

Taye et al. (2025) applied a Random Forest classifier to DHS data from a weighted sample of 198,707 women across 27 sub-Saharan African countries, including Nigeria. The study reported strong predictive performance, with a ROC-AUC of 92%, accuracy of 92%, precision of 93%, recall of 96% and F1-score of 93% in the abstract. SHAP was used to interpret the model and identify influential predictors. These included facility delivery, maternal education, household wealth, urban residence, healthcare accessibility, media exposure and internet use.

Memon et al. (2025) adopted a broader model-comparison approach using the 2016 Uganda DHS. Seven supervised learning algorithms were compared, including logistic regression, Random Forest, Gradient Boosting, XGBoost, LightGBM, Decision Tree and CatBoost. XGBoost produced the highest ROC-AUC of 0.7473. Importantly, the study also examined performance for women who did not use skilled birth attendance, with XGBoost achieving a recall of 0.73 for this group. This demonstrates the importance of considering performance for the population of greatest public-health interest rather than relying solely on overall accuracy.

Explainable machine learning has also been applied to skilled birth attendance in Burkina Faso. Miah (2026) used the 2021 Burkina Faso DHS and compared five machine-learning models. Random Forest achieved the strongest reported discrimination, with an AUROC of 0.71. The study also incorporated feature selection, SHAP-based interpretation and spatial analysis, illustrating how prediction can be combined with explainability and geographical investigation.

Nigeria-specific machine-learning evidence is also emerging for related maternal-health service-utilisation outcomes. Sani et al. (2026), for example, applied seven machine-learning algorithms to predict institutional delivery dropout among Nigerian women using the 2018 NDHS. Although institutional delivery dropout is not identical to non-use of skilled birth attendance, the study is methodologically relevant because it demonstrates the application of machine learning and SHAP interpretation to a related maternal-health service-utilisation problem in Nigeria.

Consequently, the contribution of the proposed research cannot be based simply on the application of machine learning to Nigerian maternal-health data. A more specific methodological and substantive gap must be considered.

## 2.3 Predictor Timing and the Need for a Pre-Delivery Framework

An important methodological issue identified from the reviewed prediction studies concerns when predictor information becomes available.

For a model intended to identify women at risk before childbirth, predictors should represent information that would realistically be known at the intended prediction point. Using information generated during or after the outcome event can introduce data leakage and may result in an unrealistically optimistic assessment of predictive performance.

This issue is illustrated by Taye et al. (2025), whose model included facility delivery among the important predictors of skilled birth attendance. Although place of delivery may be strongly associated with skilled attendance, the actual place where a woman gives birth would not be known before the same delivery. It would therefore not be appropriate as a predictor in a model intended to identify risk before childbirth.

Other variables also require careful consideration. Delivery complications and newborn outcomes, for example, occur during or after childbirth and would therefore not be suitable for a pre-delivery model predicting the same delivery.

Antenatal-care variables require a more nuanced approach. ANC occurs before childbirth and may provide valuable predictive information. However, the suitability of variables such as the total number of ANC visits depends on the intended prediction point. A woman's final number of ANC visits would not be available early in pregnancy because some visits may not yet have occurred.

Similarly, previous place-of-delivery information may be appropriate if it refers to an earlier birth but inappropriate if it refers to the same birth being predicted. Therefore, variable labels alone are insufficient for determining predictor eligibility; the timing and meaning of each variable must be examined carefully.

The proposed research will consequently define a clear pre-delivery prediction point before final predictor selection. Candidate variables will be evaluated not only according to their statistical relevance but also according to whether the information could realistically have been known by that prediction point. Variables containing information from the index delivery or from events occurring after the prediction point will be excluded from the primary prediction model.

## 2.4 Model Evaluation, Calibration and Explainability

The reviewed machine-learning literature demonstrates that model performance can be evaluated using several complementary measures, including accuracy, precision, recall, F1-score, ROC-AUC and, where appropriate, PR-AUC. These measures provide different information about predictive performance and should not be treated as interchangeable.

For the proposed research, performance among women who do not use skilled birth attendance is particularly important. A model could achieve high overall accuracy while performing poorly in identifying this group, particularly when outcome classes are imbalanced. Evaluation should therefore include class-specific measures such as precision, recall and F1-score in addition to overall discrimination.

PR-AUC may also be informative because it focuses on the relationship between precision and recall and can provide useful information when the outcome of interest is less common than the alternative class.

Calibration represents another important dimension of prediction-model evaluation. Whereas discrimination assesses how well a model separates women with different outcomes, calibration concerns the agreement between predicted probabilities and observed outcomes. The reviewed prediction studies did not evaluate calibration consistently. The proposed research will therefore explicitly assess calibration alongside discrimination and class-specific performance.

Explainability is also important when applying machine-learning methods to maternal-health research. Several reviewed studies used SHAP to identify characteristics contributing to model predictions. Such approaches can help clarify how complex models arrive at their predictions and identify influential variables.

However, predictive importance should not automatically be interpreted as evidence of causality. A characteristic may contribute strongly to prediction without causing non-use of skilled birth attendance. Explainability results in the proposed study will therefore be interpreted as predictive relationships rather than causal effects.

## 2.5 Validation, Survey Structure and Subgroup Performance

The Nigeria Demographic and Health Survey uses a complex sampling design in which respondents are sampled within geographical clusters. Women living within the same communities may share healthcare environments, socioeconomic conditions and other contextual characteristics.

Previous multilevel studies of skilled birth attendance have demonstrated the importance of community-level variation. This suggests that the clustered structure of the NDHS should be considered when developing and evaluating prediction models rather than automatically assuming that all observations are completely independent.

The reviewed machine-learning studies used validation approaches including train-test splitting and cross-validation. However, the appropriateness of the validation strategy depends on the intended use of the prediction model and the structure of the data. The proposed research will therefore examine an appropriate validation strategy that considers the clustered structure of the NDHS and reduces the risk of obtaining overly optimistic estimates of model performance.

Subgroup performance is also important. Previous Nigerian research has demonstrated substantial differences in skilled birth attendance according to geographical region, urban or rural residence, household wealth, education and healthcare accessibility.

Strong overall predictive performance may therefore conceal weaker performance within particular population groups. Where sample sizes permit, the proposed research will examine model performance across important geographical and socioeconomic subgroups. This will help determine whether the model performs reasonably consistently across different sections of the Nigerian population.

## 2.6 Research Gap

Existing research provides substantial evidence regarding factors associated with skilled birth attendance in Nigeria, while recent studies demonstrate that machine-learning methods can be applied to DHS maternal-health data. The reviewed literature therefore does not support a broad claim that machine learning has never been used for skilled birth attendance or Nigerian maternal-health research.

Instead, a more specific gap emerges from the combination of dataset recency, prediction target, predictor timing and model-evaluation approach.

Much of the Nigeria-specific skilled birth attendance literature has focused on identifying statistical associations using regression or multilevel methods. Machine-learning studies of skilled birth attendance have demonstrated predictive potential, but some have included variables whose timing may not correspond to a realistic pre-delivery prediction setting. Furthermore, calibration, clustered validation and subgroup performance have not been addressed consistently across the reviewed prediction studies.

Among the studies reviewed, limited evidence was identified of a Nigeria-specific prediction study using the 2023–24 Nigeria Demographic and Health Survey to predict **non-use of skilled birth attendance** while restricting the primary prediction model to information that would reasonably be available at a clearly defined point before the delivery being predicted.

The proposed research will address this gap by investigating whether non-use of skilled birth attendance can be predicted using the 2023–24 NDHS and carefully selected pre-delivery information. An interpretable baseline model will be compared with appropriate machine-learning approaches. Model evaluation will consider discrimination, class-specific performance and calibration. Explainability methods will be used where appropriate to identify influential predictors, while the clustered survey structure and performance across important geographical and socioeconomic groups will also be considered.

The contribution of the proposed study is therefore not simply the use of machine learning. Its main contribution is the development and evaluation of a prediction framework centred on a realistic **pre-delivery decision point**, using recent nationally representative Nigerian data and explicitly considering predictor timing, probability reliability and variation in predictive performance across relevant population groups.
