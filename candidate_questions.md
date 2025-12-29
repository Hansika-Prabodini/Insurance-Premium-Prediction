# Candidate Analytical Questions
## Insurance Premium Prediction Dataset

This document contains 25 candidate analytical questions organized by category. These questions leverage the dataset's 20 features and address real-world insurance industry concerns, ranging from straightforward analyses to sophisticated multi-feature investigations.

---

## 1. Feature Relationships and Interactions

### Q1: Multi-Factor Health Premium Impact
**Question**: How do combinations of Health Score, Smoking Status, and Exercise Frequency interact to predict Premium Amount?

**Rationale**: Understanding the interplay between multiple health indicators can reveal non-linear relationships and interaction effects that impact premium pricing.

**Features Used**: Health Score, Smoking Status, Exercise Frequency, Premium Amount

**Complexity**: Medium-High (3-way interaction analysis)

---

### Q2: Financial Risk Indicators
**Question**: What is the relationship between Credit Score and Previous Claims, and how do they jointly affect premiums?

**Rationale**: Both credit history and claim history are indicators of financial reliability and risk behavior; their combined effect may be synergistic.

**Features Used**: Credit Score, Previous Claims, Premium Amount

**Complexity**: Medium (correlation analysis with missing value handling for Credit Score)

---

### Q3: Vehicle Age and Policy Type Interaction
**Question**: Does the impact of Vehicle Age on Premium Amount differ by Policy Type (Basic vs Comprehensive vs Premium)?

**Rationale**: Different policy types may price vehicle age differently based on coverage levels and risk exposure.

**Features Used**: Vehicle Age, Policy Type, Premium Amount

**Complexity**: Medium (interaction effects across categorical groups)

---

### Q4: Socioeconomic Profile Correlations
**Question**: How does Annual Income correlate with Education Level and Occupation, and what does this reveal about customer profiles?

**Rationale**: Understanding socioeconomic relationships helps identify customer segments and validate data quality through expected patterns.

**Features Used**: Annual Income, Education Level, Occupation

**Complexity**: Low-Medium (correlation and distribution analysis with skewed data)

---

## 2. Customer Segmentation and Profiling

### Q5: Multi-Dimensional Customer Clustering
**Question**: Can we identify distinct customer segments based on demographics (Age, Gender, Marital Status), income, and lifestyle factors?

**Rationale**: Customer segmentation enables targeted marketing, personalized pricing strategies, and better understanding of the customer base.

**Features Used**: Age, Gender, Marital Status, Annual Income, Smoking Status, Exercise Frequency

**Complexity**: High (unsupervised clustering with mixed data types)

---

### Q6: Premium Policy Customer Characteristics
**Question**: What are the characteristics of high-value customers (those with Comprehensive or Premium policies)?

**Rationale**: Identifying traits of premium customers helps focus acquisition efforts and understand what drives higher-tier policy selection.

**Features Used**: Policy Type, Annual Income, Education Level, Occupation, Property Type, Age

**Complexity**: Medium (segmentation and profiling analysis)

---

### Q7: Geographic Customer Profiles
**Question**: How do customer profiles differ across Location types (Urban, Suburban, Rural)?

**Rationale**: Geographic differences may reflect lifestyle variations, income patterns, and risk profiles that inform regional pricing strategies.

**Features Used**: Location, Annual Income, Education Level, Occupation, Property Type, Vehicle Age

**Complexity**: Medium (comparative analysis across geographic segments)

---

### Q8: Family Structure Patterns
**Question**: What patterns exist among customers with multiple dependents versus those with none, and how does this relate to policy choices and premiums?

**Rationale**: Family size may correlate with insurance needs, income levels, and premium amounts.

**Features Used**: Number of Dependents, Marital Status, Annual Income, Policy Type, Premium Amount

**Complexity**: Medium (requires handling missing values in Number of Dependents)

---

## 3. Risk Factor Analysis

### Q9: Composite Risk Score Development
**Question**: Which combination of features (Previous Claims, Credit Score, Health Score) best predicts high-risk customers?

**Rationale**: Developing a composite risk indicator helps identify customers likely to generate claims or payment issues.

**Features Used**: Previous Claims, Credit Score, Health Score, Premium Amount

**Complexity**: High (multi-feature predictive modeling with outliers and missing values)

---

### Q10: Claims History Premium Impact
**Question**: How does the number of Previous Claims relate to policy characteristics and premium pricing?

**Rationale**: Understanding how claim history influences premiums reveals pricing strategies and risk assessment methods.

**Features Used**: Previous Claims, Premium Amount, Policy Type, Insurance Duration

**Complexity**: Medium (outlier-sensitive analysis)

---

### Q11: Vehicle Age Risk Assessment
**Question**: What role does Vehicle Age play in determining insurance risk and premium levels, controlling for other factors?

**Rationale**: Older vehicles may have different risk profiles (reliability vs. safety features) affecting pricing.

**Features Used**: Vehicle Age, Premium Amount, Policy Type, Previous Claims

**Complexity**: Medium (regression analysis with controls)

---

### Q12: Occupational Risk Patterns
**Question**: Are certain occupations associated with higher claim frequencies or premium amounts?

**Rationale**: Occupation may proxy for risk exposure, financial stability, and claim likelihood.

**Features Used**: Occupation, Previous Claims, Premium Amount, Annual Income

**Complexity**: Low-Medium (categorical comparison)

---

## 4. Lifestyle Impact Questions

### Q13: Lifestyle-Health-Premium Nexus
**Question**: How does Smoking Status interact with Health Score and Exercise Frequency to influence Premium Amount?

**Rationale**: Lifestyle choices collectively impact health outcomes and should show compounding effects on premium pricing.

**Features Used**: Smoking Status, Health Score, Exercise Frequency, Premium Amount

**Complexity**: High (3-way interaction with skewed health score distribution)

---

### Q14: Exercise as Risk Mitigation
**Question**: Is there evidence that regular exercise (Daily/Weekly) offsets negative health factors in premium calculations?

**Rationale**: Understanding whether positive lifestyle choices can mitigate other risk factors informs fair pricing strategies.

**Features Used**: Exercise Frequency, Smoking Status, Health Score, Premium Amount, Age

**Complexity**: Medium-High (interaction effects and conditional analysis)

---

### Q15: Lifestyle-Demographics Combined Effect
**Question**: What is the combined effect of lifestyle choices (smoking, exercise) and demographic factors (age, gender) on premiums?

**Rationale**: Premium pricing should reflect both modifiable (lifestyle) and non-modifiable (demographics) risk factors appropriately.

**Features Used**: Smoking Status, Exercise Frequency, Age, Gender, Premium Amount

**Complexity**: High (multi-feature interaction analysis)

---

## 5. Data Quality Implications

### Q16: Missing Value Pattern Analysis
**Question**: How do missing values in Number of Dependents and Credit Score correlate with other features, and what imputation strategies are most appropriate?

**Rationale**: Understanding missingness patterns determines whether data is MCAR, MAR, or MNAR, guiding imputation strategy selection.

**Features Used**: Number of Dependents, Credit Score, Age, Marital Status, Occupation, Annual Income

**Complexity**: Medium (missingness analysis and imputation strategy evaluation)

---

### Q17: Outlier Investigation in Claims
**Question**: What patterns exist in the outliers for Previous Claims, and should they be treated or retained?

**Rationale**: Outliers may represent genuine high-risk customers or data errors; investigation informs data cleaning decisions.

**Features Used**: Previous Claims, Premium Amount, Policy Type, Insurance Duration, Age

**Complexity**: Medium (outlier detection and contextual analysis)

---

### Q18: Skewness Transformation Strategy
**Question**: How does the skewed distribution of Annual Income and Premium Amount affect model performance, and what transformations are optimal?

**Rationale**: Skewed distributions violate assumptions of many models; transformation strategy impacts predictive accuracy.

**Features Used**: Annual Income, Premium Amount, Health Score

**Complexity**: Medium-High (distribution analysis and transformation evaluation)

---

## 6. Text Analysis Opportunities

### Q19: Customer Feedback Sentiment Analysis
**Question**: What sentiment patterns emerge from Customer Feedback, and do they correlate with Premium Amount, Policy Type, or claim history?

**Rationale**: Customer satisfaction insights from text may reveal pricing issues, service quality patterns, or product-specific concerns.

**Features Used**: Customer Feedback, Premium Amount, Policy Type, Previous Claims

**Complexity**: High (text mining, sentiment analysis, correlation with numerical features)

---

### Q20: Feedback Theme Extraction
**Question**: Can we extract actionable themes from Customer Feedback that relate to satisfaction with specific policy types or premium levels?

**Rationale**: Topic modeling can identify specific pain points or satisfaction drivers for different customer segments.

**Features Used**: Customer Feedback, Policy Type, Premium Amount, Insurance Duration

**Complexity**: High (topic modeling, thematic analysis)

---

## 7. Temporal Pattern Questions

### Q21: Policy Duration and Premium Dynamics
**Question**: How does Insurance Duration relate to Premium Amount, and are there pricing patterns for long-term versus short-term policies?

**Rationale**: Policy tenure may reflect loyalty discounts, rate increases over time, or customer risk evolution.

**Features Used**: Insurance Duration, Premium Amount, Previous Claims, Age

**Complexity**: Medium (temporal trends and pricing patterns)

---

### Q22: Policy Start Date Seasonality
**Question**: Are there seasonal or temporal patterns in Policy Start Dates that correlate with customer characteristics or premium levels?

**Rationale**: Seasonal enrollment patterns may reflect marketing campaigns, life events, or demographic-specific timing.

**Features Used**: Policy Start Date, Premium Amount, Age, Marital Status, Number of Dependents

**Complexity**: Medium-High (requires cleaning improperly formatted dates, temporal pattern analysis)

---

## 8. Fairness and Bias Considerations

### Q23: Gender-Based Premium Parity
**Question**: Do premium predictions show systematic differences across Gender when controlling for other risk factors?

**Rationale**: Fairness analysis ensures pricing doesn't discriminate based on protected characteristics beyond actuarial justification.

**Features Used**: Gender, Premium Amount, Age, Health Score, Smoking Status, Exercise Frequency, Previous Claims

**Complexity**: High (requires careful control for confounding factors, statistical testing for disparate impact)

---

### Q24: Geographic Pricing Equity
**Question**: Is there evidence of pricing disparities across Location types (Urban/Suburban/Rural) that aren't justified by risk factors?

**Rationale**: Geographic pricing differences should reflect actual risk differences, not discriminatory practices.

**Features Used**: Location, Premium Amount, Previous Claims, Vehicle Age, Property Type, Annual Income

**Complexity**: Medium-High (comparative analysis with risk adjustment)

---

### Q25: Education-Based Premium Variation
**Question**: How do premiums vary across Education Levels, and is this variation explained by correlated features like income and occupation?

**Rationale**: Understanding whether education directly or indirectly affects pricing helps identify potential proxy discrimination.

**Features Used**: Education Level, Premium Amount, Annual Income, Occupation, Credit Score

**Complexity**: Medium (mediation analysis, correlation decomposition)

---

## Summary Statistics

**Total Questions**: 25

**Category Distribution**:
- Feature Relationships and Interactions: 4 questions
- Customer Segmentation and Profiling: 4 questions
- Risk Factor Analysis: 4 questions
- Lifestyle Impact: 3 questions
- Data Quality Implications: 3 questions
- Text Analysis: 2 questions
- Temporal Patterns: 2 questions
- Fairness and Bias: 3 questions

**Complexity Distribution**:
- Low: 0 questions
- Low-Medium: 2 questions
- Medium: 10 questions
- Medium-High: 6 questions
- High: 7 questions

**Feature Coverage**: All 20 features are utilized across the questions:
- Age: 9 questions
- Gender: 3 questions
- Annual Income: 9 questions
- Marital Status: 4 questions
- Number of Dependents: 3 questions
- Education Level: 5 questions
- Occupation: 5 questions
- Health Score: 7 questions
- Location: 3 questions
- Policy Type: 10 questions
- Previous Claims: 10 questions
- Vehicle Age: 4 questions
- Credit Score: 5 questions
- Insurance Duration: 4 questions
- Premium Amount: 22 questions (target variable)
- Policy Start Date: 1 question
- Customer Feedback: 2 questions
- Smoking Status: 6 questions
- Exercise Frequency: 6 questions
- Property Type: 3 questions

**Data Complexity Addressed**:
- Missing values: 3 questions explicitly address this
- Outliers: 1 question explicitly addresses this
- Skewed distributions: 2 questions explicitly address this
- Text data: 2 questions utilize Customer Feedback
- Improperly formatted data: 1 question addresses Policy Start Date cleaning
- Multi-feature interactions: 15 questions involve 3+ features

---

## Notes for Question Selection (Task #4)

These candidate questions provide diverse analytical directions. When selecting the most interesting questions for implementation:

1. **Balance complexity**: Choose a mix that demonstrates different analytical techniques
2. **Business value**: Prioritize questions with clear actionable insights for insurance operations
3. **Technical showcase**: Include questions that highlight handling of data quality issues (missing values, outliers, text data)
4. **Ethical considerations**: Include at least one fairness/bias question to demonstrate responsible analytics
5. **Feature diversity**: Ensure selected questions collectively cover most of the 20 features

The questions are designed to be answerable with the available data while pushing the boundaries of insight extraction from this rich dataset.
