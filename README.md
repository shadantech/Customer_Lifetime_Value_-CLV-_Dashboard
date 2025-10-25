# 💼 Customer Lifetime Value (CLV) Dashboard – Tableau

## 📊 Project Overview
The **Customer Lifetime Value (CLV) Dashboard** is an advanced Tableau project designed to help businesses identify and analyze their **most valuable customers**, measure **retention performance**, and understand **revenue contribution** by different customer segments and regions.

This dashboard provides a comprehensive view of how customer behavior impacts profitability, helping teams make **data-driven marketing and retention decisions**.

---

## 🎯 Objectives
- Measure **Customer Lifetime Value (CLV)** across segments and regions.  
- Track **retention and churn trends** over time.  
- Identify **high-value customer groups** for targeted marketing.  
- Analyze **repeat purchase behavior** and **Revenue Trends** patterns.

---

## 🧩 Key Insights
- Which customer segments and regions generate the highest CLV.  
- Month-over-month **growth in customer value and retention**.  
- Top 10 **most valuable customers**.  
- Percentage of **churned vs active customers**.  
- **Cohort analysis** showing how long customers remain active after acquisition.

---

## 🧱 Dashboard Layout

### 🔹 1. Header Section
- Title and filters for:
  - Customer Active Flag
  - Region
  - Customer Segment
  - Date Range

### 🔹 2. KPI Summary Cards
| Metric | Description |
|---------|-------------|
| **Total Customers** | Unique customer count |
| **Average CLV** | Avg. lifetime revenue per customer |
| **Repeat Purchase Rate** | % of customers with >1 purchase |
| **Retention Rate** | % of retained customers |
| **Total Revenue** | Overall sales generated |

### 🔹 3. CLV & Retention Trends
| Visualization | Purpose |
|----------------|----------|
| **Line Chart** | CLV Growth Over Time |
| **Dual-Axis Chart** | Number of Orders & Average Order Value by Month |

### 🔹 4. Insights
| Visualization | Purpose |
|----------------|----------|
| **Bar Chart** | CLV by Region |
| **Table Chart** | Top 10 High-Value Customers |
| **Donut Chart** | Churn vs Retention |

---

## ⚙️ Tableau Features Used
- **LOD Expressions** – for calculating CLV per customer  
  ```tableau
  {FIXED [Customer ID] : SUM([Sales])}
  ```
- **Parameters** – to toggle between CLV metrics (Revenue / Profit / Orders)  
- **Table Calculations** – for retention and churn rates  
- **Dashboard Actions** – click-to-filter interactions  
- **Cohort Analysis** – tracking customer retention behavior  
- **Story Points** – for storytelling (Acquisition → Retention → Value Growth)

---

## 🗂️ Dataset Details
| Column Name | Description |
|--------------|--------------|
| `Customer_ID` | Unique identifier for each customer |
| `Customer_Name` | Customer name |
| `First_Purchase_Date` | Date of first purchase |
| `Last_Purchase_Date` | Most recent purchase date |
| `Total_Revenue` | Lifetime revenue per customer |
| `Number_of_Orders` | Total orders placed |
| `Average_Order_Value` | Avg. revenue per order |
| `Region` | Customer region |
| `Customer_Segment` | Customer category (Consumer, Corporate, etc.) |
| `Churn_Status` | Active / Churned |
| `Tenure_Months` | Duration since first purchase |

📁 **Dataset Source:** Custom synthetic dataset (can be simulated from E-commerce or Superstore data).

---

## 🧮 CLV Calculation Example
```tableau
[Customer Lifetime Value] = 
{FIXED [Customer ID] : SUM([Sales])}
```

**Retention Rate:**
```tableau
(SUM([Retained Customers]) / SUM([Total Customers])) * 100
```

**Repeat Purchase Rate:**
```tableau
COUNTD(IF [Order Count] > 1 THEN [Customer ID] END) / COUNTD([Customer ID])
```

---

## 🖥️ Dashboard Preview  
[CLV Dashboard Preview](CLV_Dashboard_Preview.png)

---

## 🔗 Live Preview
([Live Dashboard](https://public.tableau.com/app/profile/shadan.sarfaraz/viz/Customer_Lifetime_Value_Dashboard/CustomerLifetimeValueCLVDashboard?publish=yes))



## 🧰 Tools & Tech Stack
- **Tableau Desktop | Tableau Public**  
- **CSV Dataset**  
- **Data Preparation:** Tableau Prep  
- **Visualization Techniques:** LOD, Parameters, Cohorts, Story Points  

---

## 📸 How to View / Use
1. Download the `.twbx` Tableau packaged workbook.  
2. Open it in **Tableau Desktop** or upload to **Tableau Public**.  
3. Explore using filters and interactive parameters.

---

## 📂 Project Structure
```
Customer_Lifetime_Value_(CLV)_Dashboard/
│
├── data/
│   └── CLV_Dataset.csv
│
├── dashboard/
│   └── Customer_Lifetime_Value_Dashboard.twbx
│
├── images/
│   └── CLV_Dashboard_Preview.png
│
└── README.md
```

---

## 🏁 Conclusion
This dashboard empowers businesses to understand **customer profitability and retention behavior** through visual analytics. It’s ideal for **marketing, CRM, and business strategy teams** aiming to boost customer loyalty and maximize long-term value.

---

## 👤 Author
**Shadan Tech**   
_Data Analyst_
🔗 [LinkedIn Profile](http://www.linkedin.com/in/shadantech)  
🔗 [Tableau Public Profile](https://public.tableau.com/app/profile/shadan.sarfaraz/vizzes)

---

## ⭐ Show Your Support

If you found this project insightful, give it a **⭐ Star** on GitHub — it helps others discover it too!  
Connect on **LinkedIn** for more Power BI, Tableau, and Data Analytics projects.

---
