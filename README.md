# Customer Churn Analysis

## 📌 Project Overview

This project analyzes customer behavior to identify differences between **churned and retained customers** using statistical analysis.

The analysis focuses on three behavioral metrics:

- Cart Abandonment Rate
- Average Session Duration
- Customer Service Calls

**Python, Pandas, Seaborn, and SciPy** were used for data analysis, visualization, and hypothesis testing.

---

## 🎯 Objective

The main objective of this project is to determine whether customer behavior differs significantly between churned and retained customers.

The analysis specifically investigates:

1. Whether churned customers have higher cart abandonment rates.
2. Whether churned customers have different session durations.
3. Whether churned customers make more customer service calls.

---

## 📊 Dataset

The dataset contains **50,000 customer records** and **25 columns** representing e-commerce customer behavior.

The target variable is:

- `Churned = 0` → Retained customer
- `Churned = 1` → Churned customer

### Key Variables

| Variable | Description |
|---|---|
| `Churned` | Customer churn status |
| `Cart_Abandonment_Rate` | Rate at which shopping carts are abandoned |
| `Session_Duration_Avg` | Average customer session duration |
| `Customer_Service_Calls` | Number of customer service interactions |

### Customer Distribution

- Retained customers: **35,550**
- Churned customers: **14,450**
- Churn rate: **28.9%**

---

## 🛠️ Tools & Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy
- Jupyter Notebook / Google Colab

---

## 🔍 Analysis Approach

### 1. Exploratory Data Analysis

The dataset was first inspected for:

- Dataset structure and data types
- Missing values
- Churn distribution
- Behavioral differences between churned and retained customers

Visualizations such as count plots and box plots were used to compare customer behavior.

---

### 2. Hypothesis Testing

An independent **Welch's two-sample t-test** was used to compare the mean of each behavioral metric between churned and retained customers.

#### Null Hypothesis (H₀)

There is no difference in the mean value of the metric between churned and retained customers.

#### Alternative Hypothesis (H₁)

There is a difference in the mean value between the two groups.

Welch's t-test was selected because it does not require the two groups to have equal variances.

A significance level of **α = 0.05** was used.

---

## 📈 Results

| Metric | Retained Mean | Churned Mean | Difference | P-value |
|---|---:|---:|---:|---:|
| Cart Abandonment Rate | 54.19 | 64.18 | **+9.98 pp** | < 0.001 |
| Session Duration | 29.21 | 23.69 | **-5.52** | < 0.001 |
| Customer Service Calls | 5.19 | 6.90 | **+1.72** | < 0.001 |

### Key Findings

- Churned customers had approximately **9.98 percentage points higher cart abandonment** than retained customers.
- Churned customers had approximately **5.52 lower average session duration**.
- Churned customers made approximately **1.72 more customer service calls**.
- All three differences were statistically significant with **p < 0.001**.

---

## 💡 Business Insights

The analysis identified several behavioral patterns associated with customer churn:

- Higher cart abandonment among churned customers may indicate potential friction during the purchasing process.
- Lower session duration suggests comparatively lower customer engagement.
- Higher customer service interactions may indicate unresolved issues or greater customer support requirements.

These findings can be used as starting points for further customer-retention analysis.

> **Note:** The dataset is observational, so these results show associations between customer behavior and churn, not causal relationships.

---

## 📁 Project Structure

```text
Customer-Churn-Analysis/
│
├── Customer_Churn_Analysis.ipynb
├── dataset.csv
└── README.md
