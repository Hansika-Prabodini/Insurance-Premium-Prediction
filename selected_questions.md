# Selected Analytical Questions for Insurance Premium Analysis

## Executive Summary

After systematic evaluation of candidate questions using a structured framework, three analytical questions have been selected for investigation. These questions were chosen based on their practical business value, effective use of multiple dataset features, leverage of unique data characteristics (missing values, outliers, and text), potential for actionable insights, analytical sophistication, and clear answerability with available data.

The selected questions represent diverse analytical approaches:
1. **Outlier Investigation** - Predictive risk modeling for excessive claims
2. **Risk Profile Analysis** - Multi-factor interaction effects on premium pricing
3. **Missing Data Pattern Analysis** - Data quality and systematic bias detection

---

## Selected Question #1: Predicting Excessive Claims Through Outlier Analysis

### Question Statement
**What characteristics distinguish customers with outlier claim counts, and can we identify early warning indicators (income patterns, property type, vehicle age combinations) that predict excessive claims before they occur?**

### Comprehensive Justification

This question earned the highest evaluation score (30/30) and represents the most valuable analytical opportunity in the dataset. From a business perspective, excessive claims are the primary driver of insurance company losses, and identifying high-risk customers before they generate claims can have immediate and substantial financial impact. The ability to predict which customers will become frequent claimers enables proactive risk mitigation through pricing adjustments, policy modifications, or enhanced underwriting scrutiny. Given that the insurance industry operates on thin profit margins, even modest improvements in claims prediction can translate to millions in saved losses across a large policy portfolio.

The question excels at leveraging multiple dataset features in sophisticated ways. Previous claims data explicitly contains outliers according to the dataset documentation, providing a perfect target for investigation. The analysis would examine how these outliers correlate with demographic factors (age, occupation, marital status), economic indicators (annual income, credit score), lifestyle choices (smoking status, exercise frequency), asset characteristics (vehicle age, property type), and policy details (insurance duration, policy type). This multi-dimensional approach moves far beyond simple correlation analysis into predictive modeling territory, potentially using ensemble methods or anomaly detection algorithms to identify complex patterns that precede excessive claims behavior.

What makes this question particularly actionable is its focus on early warning indicators. Rather than simply describing what outlier claimers look like (which has limited value), the analysis seeks to identify combinations of features that predict excessive claims before they materialize. For example, discovering that customers with older vehicles, declining credit scores, and recent marital status changes show elevated claim risk would enable insurers to flag these accounts for review, adjust premiums during renewal periods, or offer targeted risk management services. The results could directly inform underwriting guidelines, claims fraud detection systems, and premium pricing models. Additionally, the analysis could reveal whether some outliers represent legitimate high-need customers versus potential fraud cases, enabling more nuanced policy responses that balance profitability with customer retention.

### Key Features Leveraged
- **Outliers:** Previous Claims (primary target)
- **Numerical Features:** Age, Annual Income, Credit Score (with missing values), Vehicle Age, Insurance Duration, Health Score
- **Categorical Features:** Occupation, Marital Status, Property Type, Policy Type, Smoking Status, Exercise Frequency, Location
- **Target Variable:** Premium Amount (to assess pricing adequacy)

### Expected Business Impact
- **Fraud Detection:** Identify patterns consistent with insurance fraud
- **Risk-Based Pricing:** Adjust premiums for high-risk segments to maintain profitability
- **Underwriting Improvements:** Enhance approval criteria to screen problematic applications
- **Customer Management:** Implement early intervention programs for at-risk policyholders
- **Claims Prevention:** Develop targeted risk mitigation programs based on predictive indicators

---

## Selected Question #2: Multi-Factor Risk Profiling and Pricing Optimization

### Question Statement
**How do lifestyle factors (smoking status, exercise frequency) interact with demographic characteristics (age, occupation) to influence premium pricing, and are there underpriced risk segments where actual claims exceed premiums?**

### Comprehensive Justification

This question scored 27/30 and addresses the fundamental challenge of insurance underwriting: accurately pricing risk across diverse customer segments. The business value is immediately apparent—mispriced risk segments represent either lost revenue (underpriced high-risk customers) or competitive disadvantage (overpriced low-risk customers who defect to competitors). By examining interaction effects between lifestyle and demographic factors, this analysis can uncover complex risk patterns that traditional single-variable pricing models miss. For instance, young smokers who exercise daily might represent a different risk profile than young smokers who exercise rarely, but simple models that only consider age and smoking status would price them identically.

The question effectively leverages multiple dataset features by examining interactions rather than isolated effects. It combines lifestyle factors (smoking status with four exercise frequency levels) with demographics (continuous age variable, categorical occupation) to create nuanced risk segments. The analysis would identify whether certain combinations amplify or mitigate risk—for example, whether regular exercise truly offsets smoking-related health risks for insurance purposes, or whether self-employed individuals show different smoking-related risk patterns than employed individuals. This goes substantially beyond simple correlation analysis into interaction modeling, likely requiring techniques such as regression trees, interaction terms in GLMs, or segmentation analysis.

What makes this question particularly actionable is its explicit focus on identifying underpriced segments where claims exceed premiums. This directly translates to pricing model improvements. If the analysis reveals that sedentary smokers in high-stress occupations generate 40% more claims than their premium levels suggest, insurers can immediately adjust pricing algorithms for this segment. Conversely, identifying overpriced segments (such as active smokers in low-risk occupations) enables competitive pricing advantages to attract profitable customers. The results can feed directly into actuarial pricing models, potentially using insights to create new rating factors or refine weights in existing premium calculation formulas. Additionally, findings could inform wellness program development—if exercise truly reduces claims among smokers, insurers might offer gym membership discounts to high-risk segments as a loss prevention strategy.

### Key Features Leveraged
- **Lifestyle Factors:** Smoking Status, Exercise Frequency (Daily/Weekly/Monthly/Rarely)
- **Demographics:** Age, Occupation (Employed/Self-Employed/Unemployed), Gender, Marital Status
- **Risk Indicators:** Health Score, Previous Claims
- **Financial Metrics:** Premium Amount, Annual Income
- **Policy Details:** Policy Type, Insurance Duration

### Expected Business Impact
- **Pricing Refinement:** Implement more granular risk-based pricing that captures interaction effects
- **Competitive Advantage:** Attract profitable low-risk customers with better pricing while maintaining margins on high-risk segments
- **Wellness Programs:** Design targeted health interventions based on which lifestyle factors most impact claims
- **Market Segmentation:** Develop specialized products for specific demographic-lifestyle combinations
- **Actuarial Model Enhancement:** Incorporate interaction terms that improve predictive accuracy of premium adequacy

---

## Selected Question #3: Systematic Missing Data Patterns and Risk Implications

### Question Statement
**What patterns exist in missing credit scores and dependent information, and do customers with missing data represent different risk profiles or premium categories that suggest systematic data collection issues or customer segmentation?**

### Comprehensive Justification

This question scored 26/30 and represents a sophisticated approach to data quality analysis with direct business implications. Missing data is rarely random in insurance datasets—customers who decline to provide credit scores or dependent information often do so for systematic reasons that correlate with risk. This analysis directly leverages one of the dataset's unique characteristics (explicitly documented missing values in Credit Score and Number of Dependents fields), turning a data quality challenge into an analytical opportunity. From a business perspective, understanding why data is missing and what it implies about customer risk is crucial for both operational improvements and pricing accuracy.

The question effectively uses multiple dataset features by examining patterns across demographic characteristics, policy choices, premium levels, and claims history for customers with versus without missing data. The analysis would investigate whether missing credit scores cluster among certain age groups, occupations, or income levels, potentially revealing that younger customers or self-employed individuals are more likely to have incomplete credit histories. Similarly, examining dependent information patterns could reveal whether single customers, divorced individuals, or certain occupation types systematically omit this information. More importantly, the analysis would assess whether customers with missing data show different claims patterns or premium levels—if customers with missing credit scores generate 20% more claims, this represents both a risk pricing challenge and a data collection priority.

The actionability of this question extends in multiple directions. If missing data correlates with higher risk, insurers can adjust pricing algorithms to incorporate an uncertainty premium for incomplete applications, or invest in data enrichment services (purchasing credit data from third parties). If missing data patterns reveal systematic collection issues—such as certain sales channels failing to gather complete information—operational processes can be improved through better forms, mandatory fields, or agent training. The analysis might also uncover customer segmentation opportunities: if high-income customers with missing dependent data show excellent claims histories, they might represent privacy-conscious individuals who warrant customized data collection approaches. Additionally, findings could inform regulatory compliance efforts if missing data patterns suggest discriminatory data collection practices or accessibility issues among certain demographic groups that need remediation.

### Key Features Leveraged
- **Missing Data:** Credit Score (missing values), Number of Dependents (missing values)
- **Risk Indicators:** Previous Claims, Premium Amount
- **Demographics:** Age, Occupation, Marital Status, Education Level, Annual Income
- **Policy Details:** Policy Type, Insurance Duration, Location
- **Behavioral Indicators:** Patterns of completeness across related fields

### Expected Business Impact
- **Risk Pricing:** Adjust premiums to account for uncertainty when data is incomplete
- **Data Collection:** Improve processes to capture complete information at point of sale
- **Operational Efficiency:** Identify and fix systematic data quality issues by channel or agent
- **Customer Segmentation:** Recognize that missing data patterns may indicate valuable customer personas
- **Compliance:** Ensure data collection practices are equitable across demographic groups
- **Third-Party Data:** Justify investment in external data sources if missing data represents material risk

---

## Evaluation Methodology

All candidate questions were systematically evaluated using six criteria, each scored on a 1-5 scale:

### Evaluation Criteria

1. **Practical Business Value for Insurance Companies**
   - Does the question address critical business challenges (profitability, risk management, customer retention)?
   - Can results directly impact decision-making and financial outcomes?

2. **Leverages Multiple Dataset Features Effectively**
   - Does the analysis incorporate diverse features (demographic, behavioral, financial, policy)?
   - Are features combined in meaningful ways rather than examined in isolation?

3. **Takes Advantage of Unique Data Characteristics**
   - Does it specifically utilize missing values, outliers, text data, or skewed distributions?
   - Does it turn data quality challenges into analytical opportunities?

4. **Potential for Actionable Insights**
   - Will findings translate to specific business actions (pricing changes, process improvements, product development)?
   - Can results be implemented within existing systems and workflows?

5. **Goes Beyond Simple Correlations**
   - Does it employ sophisticated analytical techniques (interaction effects, predictive modeling, pattern recognition)?
   - Does it seek to understand causal mechanisms or complex relationships?

6. **Clearly Answerable with Available Data**
   - Are all necessary features present in the dataset?
   - Is the question well-defined enough to produce concrete findings?

### Scoring Results

| Question | Business Value | Multiple Features | Unique Characteristics | Actionable | Beyond Correlations | Answerable | **Total** |
|----------|---------------|-------------------|----------------------|------------|-------------------|------------|-----------|
| **#1: Outlier Claims Investigation** | 5 | 5 | 5 | 5 | 5 | 5 | **30/30** |
| **#2: Risk Profile & Pricing** | 5 | 5 | 3 | 5 | 4 | 5 | **27/30** |
| **#3: Missing Data Patterns** | 4 | 4 | 5 | 4 | 4 | 5 | **26/30** |
| #4: Text Mining (Customer Feedback) | 4 | 4 | 5 | 4 | 5 | 3 | 25/30 |
| #5: Socioeconomic Interactions | 4 | 4 | 3 | 4 | 4 | 5 | 24/30 |
| #6: Geographic-Health Disparities | 4 | 4 | 3 | 4 | 3 | 5 | 23/30 |
| #7: Temporal Policy Progression | 4 | 4 | 2 | 4 | 3 | 4 | 21/30 |

---

## Runner-Up Questions Worth Considering

### Question #4: Text Mining Customer Feedback (25/30)
**"What themes emerge from customer feedback text, and how do sentiment patterns correlate with policy types, premium amounts, and subsequent claims behavior?"**

This question scored well (25/30) and offers unique value by directly leveraging the Customer Feedback text field, which represents untapped qualitative data. The analysis would use natural language processing to extract sentiment and themes from customer comments, potentially revealing that negative feedback about claims processing predicts policy cancellation, or that certain policy types generate consistent complaint patterns. The main limitation that prevented it from being a top selection is the uncertainty around text data quality and volume—if feedback is sparse or unstructured, text mining may yield limited insights. However, if Task #5 reveals rich text data, this question should be reconsidered as a primary analysis.

**Business Value:** Customer satisfaction insights, retention predictors, service quality improvements  
**Unique Strengths:** Only question leveraging text data; combines quantitative and qualitative analysis  
**Why Not Selected:** Lower confidence in data sufficiency; text mining complexity; less immediately actionable than top 3

### Question #5: Socioeconomic Pricing Equity (24/30)
**"How does the relationship between income level and premium amount vary across education levels and occupation types, and are there inequitable pricing patterns or opportunities for more nuanced risk-based pricing?"**

This question (24/30) addresses important considerations around pricing fairness and optimization across socioeconomic segments. It could reveal whether pricing models inadvertently disadvantage certain education-occupation combinations, or identify underserved market segments where refined pricing could unlock new business. The analysis would leverage the skewed income distribution and examine interaction effects between income, education (High School through PhD), and occupation categories. It wasn't selected as a top 3 question primarily because it has somewhat lower immediate business urgency compared to claims prediction and missing data issues, and it doesn't leverage as many unique data characteristics (missing values, outliers, text) as strongly.

**Business Value:** Pricing optimization, market expansion, regulatory compliance  
**Unique Strengths:** Addresses fairness concerns; uses skewed income distribution  
**Why Not Selected:** Slightly lower immediate financial impact; fewer unique data characteristics leveraged

---

## Diversity of Selected Questions

The three selected questions represent complementary analytical approaches that together provide comprehensive dataset insights:

- **Question #1 (Outlier Investigation):** Predictive modeling, anomaly detection, fraud analytics
- **Question #2 (Risk Profiling):** Interaction analysis, segmentation, pricing optimization  
- **Question #3 (Missing Data):** Data quality analysis, pattern recognition, systematic bias detection

Each question leverages different unique dataset characteristics:
- **Question #1:** Outliers in Previous Claims
- **Question #2:** Multiple categorical lifestyle factors with complex interactions
- **Question #3:** Missing values in Credit Score and Number of Dependents

All three questions are highly actionable, with clear pathways to business implementation:
- **Question #1:** Update fraud detection systems and underwriting guidelines
- **Question #2:** Refine actuarial pricing models with interaction terms
- **Question #3:** Improve data collection processes and adjust risk pricing for incomplete data

---

## Next Steps

With these three analytical questions selected, subsequent work should proceed in the following order:

1. **Exploratory Data Analysis:** Conduct detailed EDA focused on the features relevant to each selected question, documenting distributions, relationships, and data quality issues

2. **Question #3 First:** Begin with missing data pattern analysis since findings will inform data preparation for Questions #1 and #2 (e.g., whether to impute missing values, exclude cases, or treat missingness as a feature)

3. **Question #1 Second:** Proceed to outlier claims investigation, as this has the highest business value and urgency for risk management

4. **Question #2 Third:** Complete with multi-factor risk profiling, leveraging insights from the previous analyses

5. **Synthesis:** Integrate findings across all three questions to develop comprehensive recommendations for pricing models, underwriting guidelines, and operational improvements

This sequencing ensures that foundational data quality insights inform subsequent predictive modeling work, while prioritizing high-value analyses that address immediate business needs.
