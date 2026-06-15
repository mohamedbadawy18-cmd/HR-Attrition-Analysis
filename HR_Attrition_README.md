# 👥 HR Employee Attrition Analysis — IBM Dataset
> Identifying the root causes behind a 16.12% employee attrition rate across 1,470 employees

---

## 📌 Project Overview

| | |
|---|---|
| **Dataset** | IBM HR Analytics Employee Attrition (Kaggle) |
| **Sector** | Human Resources / People Analytics |
| **Tools** | Python (EDA) · Power BI (Dashboard) |
| **Dashboard Pages** | 4 pages — Overview · Risk Factors · Compensation · Retention Plan |
| **Type** | Portfolio Project |

---

## 🎯 Business Problem

High employee attrition is one of the most costly HR challenges — replacing an employee can cost 50–200% of their annual salary. This project analyzes 1,470 IBM employees to answer:

1. What is the overall attrition rate and which departments are most affected?
2. What are the strongest predictors of employee departure?
3. How does compensation relate to attrition risk?
4. What targeted actions can reduce attrition?

---

## 📊 Dataset

- **Source:** IBM HR Analytics Employee Attrition & Performance — Kaggle
- **Size:** 1,470 employees · 35 features
- **Key features:** Age, Department, JobRole, MonthlyIncome, OverTime, MaritalStatus, YearsAtCompany, YearsSinceLastPromotion, JobSatisfaction, WorkLifeBalance

**Engineered features:**
- `AgeGroup` — Under 25 / 25-34 / 35-44 / 45+
- `IncomeBand` — Low (<$3K) / Mid ($3K–$7K) / High (>$7K)
- `Attrition_Num` — Binary encoding (Yes=1, No=0)

---

## 🔍 Methodology

### Phase 1 — Data Cleaning (Excel + Python)
- Removed 3 zero-variance columns: `EmployeeCount`, `Over18`, `StandardHours`
- Engineered `AgeGroup` and `IncomeBand` columns
- Verified zero missing values across all 35 features

### Phase 2 — EDA (Python)
- Calculated attrition rates per segment using `pandas groupby`
- Built 5 visualizations: department bar, overtime comparison, age group, income box plot, correlation heatmap
- Identified top attrition drivers via correlation analysis

### Phase 3 — Dashboard (Power BI)
- Built 4-page interactive dashboard with slicers for AgeGroup, Department, JobRole, MaritalStatus

---

## 💡 Key Findings

| # | Finding | Data |
|---|---|---|
| 1 | **Overall attrition rate** | 237 out of 1,470 employees left **(16.12%)** |
| 2 | **OverTime is the #1 risk factor** | OverTime employees churn at **30.53%** vs **10.44%** without |
| 3 | **Sales Rep is the highest-risk role** | **39.76%** attrition — highest of all 9 job roles |
| 4 | **Young employees are most at risk** | Under-25 attrition: **39.18%** — nearly double the average |
| 5 | **Low income drives attrition** | Low band: **28.61%** vs Mid: **12.03%** vs High: **10.80%** |
| 6 | **Single employees leave more** | Singles: **25.5%** vs Married: **12.5%** vs Divorced: **10.1%** |
| 7 | **Sales dept has highest dept attrition** | Sales: **20.6%** · HR: **19.0%** · R&D: **13.8%** |
| 8 | **Churned employees earn $2K less** | Churned avg: **$4.79K** · Stayed avg: **$6.8K** per month |

---

## 📈 Dashboard Pages

### Page 1 — Executive Overview
KPI cards (Attrition Rate, Total Employees, Churned, Avg Income Churned) + Attrition by IncomeBand + Attrition by OverTime + Attrition by Department + Overall Donut Chart

### Page 2 — Risk Factors
Attrition by JobRole (all 9 roles) + Attrition by MaritalStatus + Attrition by AgeGroup
Interactive slicers: JobRole · AgeGroup · MaritalStatus

### Page 3 — Compensation Analysis
Scatter Plot (MonthlyIncome vs YearsAtCompany colored by Attrition) + Avg Years Since Last Promotion (Churned vs Stayed) + Avg MonthlyIncome (Churned vs Stayed)

### Page 4 — Retention Action Plan
Executive summary of top 3 recommendations with supporting KPIs and ranked action table

---

## ✅ Retention Recommendations

### 1. 💰 Review Sales Representative Compensation
With a 39.8% attrition rate, Sales Reps are leaving at more than double the company average. A compensation review and clearer commission structure should be the #1 priority.

### 2. 🎓 Retain Under-25 Talent
39.2% of employees under 25 leave within their early years. Structured onboarding, mentorship programmes, and clear career paths can significantly improve early-tenure retention.

### 3. ⏰ Fix the OverTime Policy
Employees working overtime are 3x more likely to leave (30.5% vs 10.4%). Implementing overtime limits and compensation for extra hours would directly reduce this risk.

---

## 📁 Repository Structure

```
├── README.md                          ← You are here
├── HR_Attrition_EDA.ipynb             ← Python EDA notebook
├── HR_Attrition_Dashboard.pbix        ← Power BI dashboard file
└── data/
    └── WA_Fn-UseC_-HR-Employee-Attrition.csv
```

---

## 🛠 Tools Used

- **Python** (pandas, matplotlib, seaborn) — Data cleaning, EDA, visualizations
- **Power BI** — 4-page interactive dashboard with slicers and KPI cards
- **Excel** — Initial data exploration and column engineering

---

## 👤 About

Portfolio project demonstrating end-to-end HR analytics — from raw data cleaning through to executive-ready dashboard and actionable business recommendations.

📧 [Your Email] | 💼 [Your LinkedIn URL] | 🐙 [Your GitHub URL]
