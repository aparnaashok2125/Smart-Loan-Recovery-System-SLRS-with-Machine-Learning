# Smart Loan Recovery System SLRS with Machine Learning

A Machine Learning project designed to help financial institutions identify high-risk borrowers, predict loan recovery outcomes, and assign dynamic recovery strategies to minimize defaults and improve repayment rates.

---

## Problem Statement

Loan defaults are one of the biggest challenges faced by financial institutions, as they directly affect profitability and cash flow.  
This **Smart Loan Recovery System** uses **Machine Learning** to analyze borrower profiles, loan details, and repayment behaviour to:

- Identify high-risk borrowers early.
- Segment borrowers into meaningful groups.
- Suggest data-driven and cost-effective recovery strategies.

---

## Dataset Overview

The dataset contains borrower profiles, loan details, repayment history, and collection efforts.  
It includes the following key attributes:

| Category | Example Features |
|-----------|------------------|
| Demographic Information | Age, Gender, Employment Type, Monthly Income, Dependents |
| Loan Details | Loan Amount, Tenure, Interest Rate, Collateral Value |
| Repayment History | Number of Missed Payments, Days Past Due, Monthly EMI |
| Collection Efforts | Recovery Attempts, Collection Method, Legal Actions |
| Target Variable | Loan Recovery Status (Fully Recovered, Partially Recovered, Outstanding) |

---

## Project Workflow

### 1. **Data Preprocessing**
- Imported and cleaned loan repayment data using `pandas`.
- Handled missing values and standardized numerical features using `StandardScaler`.

### 2. **Exploratory Data Analysis (EDA)**
- Analyzed patterns using **Plotly** visualizations.
- Explored relationships between **loan amount**, **monthly income**, and **recovery status**.
- Key findings:
  - Higher income → higher loan amounts → better recovery rate.
  - Frequent missed payments strongly reduce recovery chances.

### 3. **Borrower Segmentation using K-Means Clustering**
- Clustered borrowers based on financial and behavioral features.
- Identified 4 key segments:

| Segment | Characteristics |
|----------|----------------|
| 0 | Moderate Income, High Loan Burden |
| 1 | High Income, Low Default Risk |
| 2 | Moderate Income, Medium Risk |
| 3 | High Loan, Higher Default Risk |

### 4. **Default Risk Prediction**
- Created a binary flag (`High_Risk_Flag`) for high-risk segments.
- Trained a **Random Forest Classifier** to predict borrower risk.
- Evaluated using accuracy, risk probability scores, and visual patterns.

### 5. **Dynamic Recovery Strategy**
- Generated borrower-specific risk scores from the model.
- Assigned personalized recovery strategies based on probability thresholds:

| Risk Score | Recovery Strategy |
|-------------|------------------|
| > 0.75 | Immediate legal notices & aggressive recovery attempts |
| 0.50 – 0.75 | Settlement offers & flexible repayment plans |
| < 0.50 | Automated reminders & routine monitoring |

---

## Technologies Used

| Category | Tools |
|-----------|-------|
| Programming | Python |
| Data Analysis | pandas, numpy |
| Visualization | plotly, plotly.express |
| Machine Learning | scikit-learn (K-Means, Random Forest) |
| Environment | Jupyter Notebook / Google Colab |

---

## Key Insights

- Borrowers with **0–2 missed payments** are most likely to fully recover loans.
- **Higher-income** individuals tend to have larger but more reliable loans.
- **Cluster-based segmentation** helps target recovery efforts more effectively.
- **Automated risk scoring** improves efficiency in prioritizing recovery actions.

---

## Future Enhancements

- Deploy an **interactive dashboard** for live borrower monitoring.
- Integrate **NLP models** to analyze customer feedback and emails.
- Use **deep learning** for more accurate repayment predictions.
- Build an API or web app using **Flask/Django** for financial institutions.



