# 📊 Customer Churn Analysis — Power BI Dashboard

An end-to-end **customer churn analytics** dashboard built in **Power BI** to analyze attrition patterns in the banking sector.  
This project helps stakeholders identify churn drivers, monitor retention performance, and design targeted intervention strategies.

---

## 📌 Problem Statement

Banks face growing challenges in retaining customers due to competition, service expectations, and product differentiation.  
This project analyzes customer behavior, demographics, and product usage patterns to identify churn risks and support data-driven retention strategies.

---

## 🛠 Tools & Technologies

- **Power BI** — Data modeling & dashboard development  
- **DAX** — KPI and churn calculations  
- **Power Query (M)** — Data cleaning & transformation  
- **SQL Server** — Data extraction  
- **Python** — Exploratory analysis (ad-hoc)

---

## 📂 Project Overview

The dashboard analyzes customer churn using key behavioral and demographic dimensions:

- Total vs Active vs Inactive Customers  
- Credit Card vs Non-Credit Card Customers  
- Monthly churn and retention trends  
- Customer distribution by geography & tenure  
- Impact of balance, tenure, and service usage on churn  

---

## 🧩 Data Model

![Data Model](https://github.com/user-attachments/assets/0188685a-59f4-48bb-895d-ed11087146bc)

---

## 📊 Dashboard Preview

![Customer Churn Dashboard](https://github.com/user-attachments/assets/26829471-d15e-43dc-bb3a-7513b4c3f885)

![KPI Overview](https://github.com/user-attachments/assets/3c9d207f-2af4-4ea9-8360-47b141f0b66d)

---

## 📈 Key KPIs Tracked

- Total Customers  
- Active vs Inactive Customers  
- Credit Card Holders  
- Exit (Churned) Customers  
- Retained Customers  
- Monthly Churn Trends  
- Churn by Geography, Gender, and Age  
- Tenure & Balance Impact  

---

## 🔍 Key Insights

- Higher churn observed among **inactive members** and **non-credit card customers**  
- Customers with lower tenure show higher exit probability  
- Regional differences indicate operational or service variation  
- Monthly churn spikes highlight seasonal behavioral patterns  

---

## 📊 Visualizations Used

- **Bar & Column Charts** — Churn by demographics  
- **Line Charts** — Monthly churn trends  
- **Donut Charts** — Customer distribution  
- **Cards** — KPI monitoring  
- **Slicers** — Geography, Gender, Credit Card filters  

---

## ⚙️ Features

- Fully interactive filters & slicers  
- Drill-down capabilities for granular analysis  
- Executive-ready layout  
- Scalable KPI framework using DAX  

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
📂 Repository Structure
```
customer-churn-analysis/
│
├── customer-churn-analysis.pbix
├── screenshots/
└── README.md
```
👤 Author
```
Avinash Dubey — Data Analyst (≈3 YOE)

📧 dubeyavinash157@gmail.com

🔗 LinkedIn: https://www.linkedin.com/in/avinash7007/

🌐 Portfolio: https://avinash7007.github.io/avinash-portfolio/

🐙 GitHub: https://github.com/Avinash7007

