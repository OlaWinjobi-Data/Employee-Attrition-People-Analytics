# Employee-Attrition-People-Analytics-Retention-Analysis

## Employee Attrition & People Analytics: Understanding Workforce Turnover and Identifying Opportunities for Proactive Retention

---

## 📊 Visual Dashboards & Insights

### 1. Descriptive Analysis Overview
<img src="https://githubusercontent.com" width="100%">

### 2. Attrition Analysis Overview
<img src="https://githubusercontent.com" width="100%">

### 3. Diagnostic Insights & Segment Breakdowns
<img src="https://githubusercontent.com" width="100%">

### 4. Predictive Modelling Risk Distribution
<img src="https://githubusercontent.com" width="100%">

### 5. Retention Prioritisation & Resource Allocation
<img src="https://githubusercontent.com" width="100%">

---

## 📁 Project Assets & Source Files
Because GitHub does not natively display interactive spreadsheets or nested document frames in the browser view, you can download the full high-resolution project materials directly using the buttons below:

* 📄 **[Download the Complete Project Report (PDF)](Employee_Attrition_Analysis.pdf)**
* 📈 **[Download the Cleaned Dataset & Logistic Regression Model (XLSX)](Employee_Attrition_Analysis.xlsx)**

---

## Project Overview

This project is a People Analytics case study analysing employee attrition across a workforce of 1,000 employees.

The analysis moves from descriptive and diagnostic analysis to predictive modelling and retention prioritisation, with the aim of understanding workforce turnover and identifying employee groups that may warrant further investigation.

The project demonstrates how People Analytics can support evidence-based workforce decisions by combining employee data, statistical analysis, visualisation and predictive modelling.

---

## Business Problem

Employee attrition can create significant challenges for organisations, including recruitment costs, loss of organisational knowledge, disruption to teams and potential impacts on employee engagement and performance.

The key business question for this analysis was:

> **What is driving employee attrition, which workforce segments are most affected, and how can People Analytics support proactive retention?**

The analysis follows four stages:

**Describe → Diagnose → Predict → Prioritise**

---

## Project Objectives

The analysis aimed to:

- Understand the profile of employees who left the organisation
- Identify workforce segments with higher attrition rates
- Explore factors associated with employee attrition
- Develop a logistic regression model to estimate attrition risk
- Evaluate the model's ability to discriminate between leavers and non-leavers
- Prioritise employees based on estimated attrition risk
- Translate analytical findings into potential retention actions

---

## Dataset Description

The dataset contains **1,000 employees** and **27 employee-level variables** covering areas including:

- Demographics
- Department and business unit
- Country
- Job level
- Age and tenure
- Salary and compa-ratio
- Performance
- Promotion history
- Salary increase recency
- Employee engagement
- Absence
- Manager tenure
- Working arrangement
- Overtime
- Training
- Attrition

### Workforce overview

| Metric | Result |
|---|---:|
| Employees | 1,000 |
| Leavers | 149 |
| Non-leavers | 851 |
| Overall attrition | 14.9% |
| Average tenure of leavers | 4.5 years |

---

## Tools & Technologies

- **Excel** – data preparation, analysis, modelling and calculations
- **Power BI** – dashboard development and visualisation
- **Python** – analytical validation and supporting analysis
- **Logistic Regression** – predictive modelling
- **GitHub** – project documentation and portfolio presentation

---

# Project Workflow

## 1. Data Preparation

The employee dataset was reviewed and prepared for analysis.

Key activities included:

- Checking data completeness
- Reviewing categorical variables
- Creating analytical bands
- Creating binary and categorical dummy variables for modelling
- Establishing reference categories for the regression model
- Validating the employee-level data used in the analysis

---

## 2. Descriptive Analysis

The first stage examined the characteristics of employees who left the organisation.

Key questions included:

- Who is leaving?
- Which age groups are represented among leavers?
- Which tenure groups account for the largest share of leavers?
- Which departments and job levels contribute most to the leaver population?

### Key findings

- **60% of leavers were aged 32–45**
- **44% of leavers had 2–<5 years of tenure**
- **36% of leavers were Professional-level employees**
- **40% of leavers were based in the UK**

The descriptive analysis answers:

> **Who is leaving?**

---

## 3. Attrition Analysis

The analysis then examined attrition rates across workforce segments.

Unlike leaver composition, attrition rate measures the proportion of employees within each segment who left.

### Department attrition

| Department | Attrition |
|---|---:|
| Finance | 18% |
| HR | 16.3% |
| Claims | 16.1% |
| IT | 15.9% |
| Sales | 15.0% |
| Operations | 14.7% |
| Marketing | 11.7% |
| Underwriting | 9.9% |

This analysis answers:

> **Where is attrition highest?**

---

## 4. Diagnostic Analysis

The next stage examined workforce characteristics associated with higher observed attrition.

Notable patterns included:

| Factor | Observed attrition |
|---|---:|
| Low engagement | 38% |
| 24+ months since salary increase | 24% |
| Compa-ratio <0.85 | 22% |
| Overtime | 21% |
| No promotion in previous 2 years | 18% |

These relationships are **observed associations rather than evidence of causation**.

The analysis therefore uses these findings to identify areas for further investigation rather than assuming that a particular factor directly causes employees to leave.

---

## 5. Intersection Analysis

The analysis also examined combinations of workforce characteristics to identify more concentrated patterns.

Examples included:

### Finance

Finance had an overall attrition rate of **18%**.

Within Finance:

- Low engagement: **57% attrition**
- Compa-ratio below 0.85: **54% attrition**
- 24+ months since salary increase: **31% attrition**

### Entry-level employees

Entry-level employees had an overall attrition rate of **21%**.

Among employees with 24+ months since their salary increase, attrition was **48%**.

### Female employees

Female employees had an overall attrition rate of **17.3%**.

Within this population:

- Compa-ratio below 0.85: **30% attrition**
- 24+ months since salary increase: **27% attrition**
- Low engagement: **25% attrition**

These intersection analyses help identify where patterns may become more concentrated and provide areas for further HR investigation.

---

# 6. Predictive Modelling

A logistic regression model was developed to estimate the probability that an employee would be classified as a leaver.

### Target variable

**Leaver flag**

- `1` = employee left
- `0` = employee remained

Categorical variables were represented using dummy variables with reference categories.

The model generated:

- Logit
- Odds
- Predicted probability
- Log-likelihood
- Squared error

Excel Solver was used to estimate the model coefficients.

The probability calculation was:

`Probability = Odds / (1 + Odds)`

The model was developed using the full 1,000-employee dataset, so the reported performance metrics should be interpreted as **development/in-sample metrics rather than out-of-sample validation results**.

---

## Model Performance

| Metric | Result |
|---|---:|
| ROC-AUC | 0.728 |
| Brier Score | 0.1127 |
| Employees modelled | 1,000 |
| Leavers | 149 |
| Attrition prevalence | 14.9% |

### Interpretation

The ROC-AUC of **0.728** indicates moderate discrimination between employees who left and those who remained within this development dataset.

The Brier Score of **0.1127** provides an assessment of the accuracy of the predicted probabilities.

Because the model was developed on the full dataset, future work should use a holdout sample or cross-validation to assess how well the model generalises to unseen data.

---

# 7. Predicted Risk Distribution

Employees were grouped into working risk bands based on their modelled probability of attrition:

| Risk Band | Probability |
|---|---:|
| Low | <10% |
| Moderate | 10–<20% |
| High | 20–<30% |
| Very High | ≥30% |

The resulting population distribution was:

| Risk Band | Employees |
|---|---:|
| Low | 437 |
| Moderate | 313 |
| High | 148 |
| Very High | 102 |

These thresholds are **working bands rather than statistically validated risk categories** and should be reviewed against future outcomes and HR intervention capacity.

---

# 8. Retention Prioritisation

Rather than treating every employee as having the same retention priority, employees were ranked from highest to lowest predicted attrition probability.

The model's cumulative capture analysis showed:

| Highest-risk population targeted | Historical leavers captured |
|---|---:|
| Top 10% | 31.5% |
| Top 20% | 48.3% |
| Top 30% | 59.1% |
| Top 40% | 65.8% |

