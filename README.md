# 📊 Customer Churn Segmentation & Retention

An end-to-end **Customer Churn Segmentation & Retention** project focused on analyzing customer attrition patterns and identifying key churn drivers.  
This project helps stakeholders monitor churn behavior, evaluate retention performance, and design targeted intervention strategies.

---

## 📌 Problem Statement

Organizations often struggle with customer retention due to changing behavior patterns, service expectations, and competitive pressure.  
This project analyzes customer demographics, engagement behavior, tenure, and financial attributes to identify churn risks and support data-driven retention strategies.

---

## 🛠 Tools & Technologies

- **SQL** — Data extraction and segmentation  
- **Power BI** — Data modeling and analysis  
- **DAX** — KPI and churn calculations  
- **Power Query (M)** — Data cleaning and transformation  
- **Excel** — Data validation and quick analysis  

---

## 📂 Project Overview

The analysis evaluates churn behavior using key customer and behavioral dimensions:

- Total vs Active vs Inactive Customers  
- Monthly churn and retention trends  
- Customer distribution by geography, gender, and tenure  
- Impact of balance, tenure, and engagement on churn  
- Segment-level churn risk identification  

---

## 📊 Data Scope

- **30K+ customers analyzed**  
- Multi-dimensional segmentation across demographics and behavior  
- Identified high-risk segments with **>20% churn rate**  
- Supported retention strategies improving retention by **~12%**

---

## 📊 Dashboard Preview

### Data Model
![Data Model](https://github.com/user-attachments/assets/cd563acf-5694-4583-8427-87318602a1a4)

### Customer Churn Dashboard
![Customer Churn Dashboard](https://github.com/user-attachments/assets/1b151f46-cb8d-4b73-bab0-6c011710b9e2)

### KPI Overview
![KPI Overview](https://github.com/user-attachments/assets/7b9b9155-fa2a-422d-90ff-606dafc87e95)

## 🔍 Key Insights

- Higher churn observed among **inactive customers**  
- Customers with shorter tenure showed higher churn probability  
- Regional variation suggested operational and engagement differences  
- Behavioral indicators strongly correlated with churn outcomes  

---

## 📈 Analysis Techniques Used

- Cohort-style behavioral analysis  
- Customer segmentation using SQL logic  
- Trend and variance analysis  
- Risk-based customer profiling  

---

## 🧮 Sample SQL Queries

```sql
-- Exit Customers
SELECT COUNT(*) AS exit_customers
FROM CustomerData
WHERE Exited = 1;

-- Retained Customers
SELECT COUNT(*) AS retained_customers
FROM CustomerData
WHERE Exited = 0;

-- Churn Rate Calculation
SELECT 
    COUNT(CASE WHEN Exited = 1 THEN 1 END) * 100.0 / COUNT(*) AS churn_rate
FROM CustomerData;

-- High-Risk Segment Identification
SELECT Geography, COUNT(*) AS churned_customers
FROM CustomerData
WHERE Exited = 1
GROUP BY Geography
ORDER BY churned_customers DESC;
```

---

## 🧮 Sample DAX Measures

```dax
Exit Customers =
CALCULATE(
    COUNTROWS(CustomerData),
    CustomerData[Exited] = 1
)

Retained Customers =
CALCULATE(
    COUNTROWS(CustomerData),
    CustomerData[Exited] = 0
)

Churn Rate (%) =
DIVIDE([Exit Customers], [Total Customers]) * 100
```

---

## ⚙️ Features

- Interactive filters and slicers  
- Drill-down capability for granular insights  
- Executive-ready layout  
- Scalable KPI framework using DAX  

---

## 📂 Repository Structure

```
customer-churn-segmentation-retention/
│
├── customer-churn-analysis.pbix
├── screenshots/
│   ├── churn-dashboard.png
│   └── kpi-overview.png
└── README.md
```

---

## 👤 Author

**Avinash Dubey — Data Analyst (≈3 YOE)**  

📧 dubeyavinash157@gmail.com  
🔗 LinkedIn: https://www.linkedin.com/in/avinash7007/  
🌐 Portfolio: https://avinash7007.github.io/avinash-portfolio/  
🐙 GitHub: https://github.com/Avinash7007
