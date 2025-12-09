# 📊 Loan Analytics Dashboard — Data Analytics Project

This repository showcases an end-to-end data analytics project built to analyze loan applications, product performance, portfolio quality, and customer insights. All datasets used in this project are **synthetic data** generated using Python, making this project safe and suitable for portfolio demonstration.

The dashboard is developed in **Power BI**, with a full data pipeline starting from Python → SQL Join → Excel Cleaning → Power BI Visualization.

---

## 🚀 Project Overview

The main objective of this project is to develop a comprehensive analytical dashboard that enables business teams and management to:
- Understand loan application trends
- Measure approval rates
- Monitor portfolio quality (PAR, DPD, Aging)
- Analyze customer segmentation
- Evaluate application channel performance

---

## 🛠️ Data Pipeline / Workflow

### 1️⃣ Synthetic Data Generation (Python)
Synthetic datasets were generated using Python with libraries such as:
- pandas
- numpy
- faker
- random
- datetime

Generated tables:
- customers
- applications
- loans
- repayment
- product_type
- application_channel

### 2️⃣ Data Integration & SQL Join
Example SQL join used to build the master dataset:
```sql
SELECT a.*, c.gender, c.annual_income, p.product_name
FROM applications a
LEFT JOIN customers c ON a.customer_id = c.customer_id
LEFT JOIN product_type p ON a.product_type = p.product_type;
```

### 3️⃣ Data Cleaning (Excel / CSV)
Data was cleaned using Excel, including:
- Handling missing values
- Standardizing date formats
- Normalizing categorical fields
- Creating calculated metrics
- Validating numeric columns and outliers

### 4️⃣ Data Visualization (Power BI)
Four dashboards were developed:
- Executive Overview
- Application & Sales Funnel
- Portfolio Quality Monitoring
- Customer Insight Dashboard

---

## 📸 Dashboard Preview
(Replace image links after uploading to `/images/` in your GitHub repo)

### 🔹 Executive Overview Dashboard
![Executive Overview](images/executive_dashboard.png)

### 🔹 Application & Sales Funnel
![Sales Funnel](images/sales_funnel.png)

### 🔹 Portfolio Quality Dashboard
![Portfolio Quality](images/portfolio_quality.png)

### 🔹 Customer Insight Dashboard
![Customer Insight](images/customer_insight.png)

---

## 📈 Key Insights (Data Analyst Summary)

### 1️⃣ Business Performance
- Total Applications: **6000**
- Approval Rate: **48%**
- Total Loan Amount: **28 Billion**
- Active Loans: **706**

### 2️⃣ Loan Trend Analysis
- Peak loan applications occur in **March–April**.
- Decline observed in **July–August**, suggesting seasonal impact.

### 3️⃣ Product Performance
Top-performing products:
- Multipurpose
- Motor Financing

Credit Card products show lower uptake, indicating potential for targeted marketing.

### 4️⃣ Application Channel Performance
- Highest approval rate: **Agent**
- Lowest approval rate: **Branch**

This suggests improvements may be needed in branch-level onboarding and verification processes.

### 5️⃣ Rejection Reason Analysis
Top rejection reasons:
- Negative Bureau (24.93%)
- High DTI (24.74%)
- Low Credit Score (16.38%)

### 6️⃣ Portfolio Quality (Risk Insight)
- Total Overdue Amount: **5.93B**
- PAR30: **8.68%** (higher than ideal threshold)
- PAR60/PAR90: **0.51%**
- Majority of DPD sits in **1–10 days** (early delinquency)

### 7️⃣ Customer Insights
- Gender distribution is balanced
- Majority age group: **46+**
- Dominant occupation: **Employed**
- Customer locations concentrated in urban areas (Jakarta, Bandung, Surabaya)

---

## 📂 Repository Structure
```
📁 loan-analytics-dashboard
│
├── data/
│   ├── raw/
│   ├── cleaned/
│   └── synthetic_data_generation.ipynb
│
├── sql/
│   └── join_master_table.sql
│
├── dashboard/
│   └── powerbi.pbix
│
├── images/
│   ├── executive_dashboard.png
│   ├── sales_funnel.png
│   ├── portfolio_quality.png
│   └── customer_insight.png
│
└── README.md
```

---

## 💡 Tools Used
| Tool | Purpose |
|------|---------|
| Python | Synthetic data generation & preprocessing |
| SQL | Data joining & transformation |
| Excel | Manual data cleaning |
| Power BI | Data visualization & storytelling |
| GitHub | Documentation & version control |

---

## 🧑‍💻 Author
**Abiyyu Anel**
Data Analyst & BI Developer

📧 abiyyuanel@gmail.com
