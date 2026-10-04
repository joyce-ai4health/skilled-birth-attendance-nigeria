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
