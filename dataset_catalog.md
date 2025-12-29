# Insurance Premium Dataset Catalog

## Executive Summary

This comprehensive catalog documents the insurance premium prediction dataset containing **2,000+ records** across **20 features**. The dataset is designed for educational purposes to practice regression modeling, feature engineering, and data cleaning. The target variable is **Premium Amount**, which represents the insurance premium to be predicted.

---

## Dataset Characteristics

- **Total Records**: 2,000+
- **Total Features**: 20 (excluding target)
- **Target Variable**: Premium Amount
- **Data Types**: Categorical, Numerical, and Text
- **Data Quality**: Contains missing values, outliers, skewed distributions, incorrect data types, and formatting issues to simulate real-world scenarios

---

## Feature Inventory by Category

### 1. Demographic Features (6 features)

| # | Feature Name | Data Type | Category Values/Range | Notes |
|---|--------------|-----------|----------------------|-------|
| 1 | Age | Numerical | - | Age of insured individual |
| 2 | Gender | Categorical | Male, Female | Gender of insured individual |
| 4 | Marital Status | Categorical | Single, Married, Divorced | Marital status of insured |
| 5 | Number of Dependents | Numerical | - | Number of dependents ⚠️ **Contains missing values** |
| 6 | Education Level | Categorical | High School, Bachelor's, Master's, PhD | Highest education level |
| 7 | Occupation | Categorical | Employed, Self-Employed, Unemployed | Occupation type |

### 2. Financial Features (2 features)

| # | Feature Name | Data Type | Category Values/Range | Notes |
|---|--------------|-----------|----------------------|-------|
| 3 | Annual Income | Numerical | - | Annual income ⚠️ **Skewed distribution** |
| 13 | Credit Score | Numerical | - | Credit score ⚠️ **Contains missing values** |

### 3. Health & Lifestyle Features (3 features)

| # | Feature Name | Data Type | Category Values/Range | Notes |
|---|--------------|-----------|----------------------|-------|
| 8 | Health Score | Numerical | - | Health status score ⚠️ **Skewed distribution** |
| 18 | Smoking Status | Categorical | Yes, No | Smoking status |
| 19 | Exercise Frequency | Categorical | Daily, Weekly, Monthly, Rarely | Exercise frequency |

### 4. Policy-Related Features (4 features)

| # | Feature Name | Data Type | Category Values/Range | Notes |
|---|--------------|-----------|----------------------|-------|
| 10 | Policy Type | Categorical | Basic, Comprehensive, Premium | Insurance policy type |
| 11 | Previous Claims | Numerical | - | Number of previous claims ⚠️ **Contains outliers** |
| 14 | Insurance Duration | Numerical | Years | Duration of insurance policy |
| 16 | Policy Start Date | Text | - | Policy start date ⚠️ **Improperly formatted** |

### 5. Property & Asset Features (3 features)

| # | Feature Name | Data Type | Category Values/Range | Notes |
|---|--------------|-----------|----------------------|-------|
| 9 | Location | Categorical | Urban, Suburban, Rural | Type of location |
| 12 | Vehicle Age | Numerical | Years | Age of insured vehicle |
| 20 | Property Type | Categorical | House, Apartment, Condo | Type of property owned |

### 6. Feedback Features (1 feature)

| # | Feature Name | Data Type | Category Values/Range | Notes |
|---|--------------|-----------|----------------------|-------|
| 17 | Customer Feedback | Text | Free text | Short feedback comments ⚠️ **Text formatting issues** |

### 7. Target Variable (1 feature)

| # | Feature Name | Data Type | Category Values/Range | Notes |
|---|--------------|-----------|----------------------|-------|
| 15 | **Premium Amount** | Numerical | - | **TARGET VARIABLE** - Insurance premium amount ⚠️ **Skewed distribution** |

---

## Data Quality Issues

### 1. Missing Values

| Feature | Issue Description | Impact |
|---------|-------------------|--------|
| Number of Dependents | Contains missing values | May require imputation or removal strategies |
| Credit Score | Contains missing values | Critical financial indicator requiring careful handling |

**Total Features with Missing Values**: 2

### 2. Outliers

| Feature | Issue Description | Impact |
|---------|-------------------|--------|
| Previous Claims | Contains outliers | May require outlier detection and treatment to prevent model bias |

**Total Features with Outliers**: 1

### 3. Skewed Distributions

| Feature | Issue Description | Impact |
|---------|-------------------|--------|
| Annual Income | Skewed distribution | May require log transformation or other normalization techniques |
| Health Score | Skewed distribution | Consider transformation for better model performance |
| Premium Amount | Skewed distribution (TARGET) | May require transformation; affects model evaluation metrics |

**Total Features with Skewed Distributions**: 3

### 4. Incorrect Data Types

| Issue Description | Impact |
|-------------------|--------|
| Some fields are intentionally set to incorrect data types | Requires type conversion during data cleaning; specific fields not enumerated in documentation |

**Note**: Specific fields with incorrect data types are not explicitly named in the README but are present in the dataset as part of the data quality challenges.

### 5. Text Data Formatting Problems

| Feature | Issue Description | Impact |
|---------|-------------------|--------|
| Policy Start Date | Improperly formatted | Requires parsing and standardization to proper date format |
| Customer Feedback | Text data with potential formatting issues | May require text cleaning, tokenization, or encoding for model use |

**Total Features with Formatting Issues**: 2

---

## Target Variable Details

### Premium Amount

- **Type**: Numerical (Continuous)
- **Role**: Target variable for regression modeling
- **Distribution**: Skewed distribution
- **Purpose**: The primary variable to be predicted by regression models
- **Considerations**: 
  - Skewness may require logarithmic or other transformations
  - Evaluation metrics should account for skewed distribution (e.g., RMSE, MAE, MAPE)
  - May benefit from examining distribution before and after transformation

---

## Dataset Purpose and Intended Use Cases

### Educational Purpose

This is a **synthetic dataset created specifically for educational purposes** to simulate real-world data challenges faced by data scientists and analysts in the insurance industry.

### Primary Use Cases

1. **Feature Engineering Practice**
   - Creating new features from existing ones
   - Encoding categorical variables
   - Handling text data
   - Binning and discretization

2. **Data Cleaning and Preprocessing**
   - Handling missing values (imputation strategies)
   - Outlier detection and treatment
   - Data type correction
   - Date parsing and standardization
   - Distribution normalization/transformation

3. **Regression Model Training**
   - Building predictive models for insurance premium estimation
   - Comparing different regression algorithms
   - Feature selection and importance analysis

4. **Model Evaluation and Tuning**
   - Hyperparameter optimization
   - Cross-validation strategies
   - Performance metrics evaluation
   - Model interpretability

### Real-World Simulation

The dataset intentionally includes various data quality issues to mimic real-world scenarios where:
- Data collection is imperfect
- Multiple data types must be handled
- Distributions are non-normal
- Missing data requires strategic decisions

---

## Summary Statistics

### Feature Type Distribution

| Data Type | Count | Features |
|-----------|-------|----------|
| Numerical | 9 | Age, Annual Income, Number of Dependents, Health Score, Previous Claims, Vehicle Age, Credit Score, Insurance Duration, Premium Amount |
| Categorical | 9 | Gender, Marital Status, Education Level, Occupation, Location, Policy Type, Smoking Status, Exercise Frequency, Property Type |
| Text | 2 | Policy Start Date, Customer Feedback |

### Data Quality Overview

| Quality Aspect | Count | Percentage |
|----------------|-------|------------|
| Features with Missing Values | 2 | 10% |
| Features with Outliers | 1 | 5% |
| Features with Skewed Distributions | 3 | 15% |
| Features with Formatting Issues | 2 | 10% |
| Clean Features | ~12 | ~60% |

---

## Quick Reference: Features by Data Quality Concern

### ⚠️ Requires Special Attention

- **Number of Dependents**: Missing values
- **Credit Score**: Missing values
- **Previous Claims**: Outliers
- **Annual Income**: Skewed distribution
- **Health Score**: Skewed distribution
- **Premium Amount**: Skewed distribution (TARGET)
- **Policy Start Date**: Improper formatting
- **Customer Feedback**: Text formatting
- **Various Fields**: Incorrect data types (to be identified during analysis)

### ✓ Standard Processing Expected

- Age
- Gender
- Marital Status
- Education Level
- Occupation
- Location
- Policy Type
- Vehicle Age
- Insurance Duration
- Smoking Status
- Exercise Frequency
- Property Type

---

## License and Attribution

**License**: Free for educational use  
**Type**: Synthetic dataset  
**Purpose**: Practice and experimentation  
**Restrictions**: None specified

---

*This catalog was generated from README.md documentation and serves as a comprehensive reference for all subsequent data analysis and modeling tasks.*
