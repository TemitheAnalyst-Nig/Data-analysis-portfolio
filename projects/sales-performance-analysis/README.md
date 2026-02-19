## 🔗 Live Dashboard
View the interactive Power BI report here:  
https://app.powerbi.com/links/LrKKpYQxKl?ctid=05d71bc3-f39b-4a76-b03f-9d628db42845&pbi_source=linkShare
# Northwind Sales & Operations Intelligence Dashboard

### Customer Analytics Case Study (Power BI)

## 1. Project Overview
<img width="1232" height="684" alt="Screenshot 2026-02-07 170737" src="https://github.com/user-attachments/assets/e326961b-1b85-4f49-8cef-ec021c78a4fe" />

In the competitive landscape of international food distribution, organizations must continuously optimize revenue, strengthen customer retention, and identify emerging growth opportunities.

This project develops a **Sales and Operations Intelligence Dashboard in Power BI** to transform transactional data into **actionable business insights**. The solution enables stakeholders to:

* Understand customer purchasing behavior
* Segment high-value and at-risk customers
* Monitor operational performance and delivery efficiency
* Support data-driven revenue and retention strategies

At the core of the analysis is **RFM segmentation (Recency, Frequency, Monetary)**, a proven customer analytics framework used to classify customers by engagement and value.

Key insight:

* **VIP/Champion customers contribute disproportionate revenue**, while
* **Core/Regular customers represent the largest share of the base (~35%)**,
  highlighting clear opportunities for **targeted retention and upsell strategies**.

---

## 2. Data Source & Preparation

### Dataset

The dashboard uses the **Northwind Traders relational dataset**, provided as CSV extracts representing real-world ERP/CRM transaction structures:

* **orders.csv** – order lifecycle, freight, customers, employees
* **order_details.csv** – product-level quantity, price, discount
* **employees.csv** – sales staff hierarchy
* **shippers.csv** – logistics providers
* **categories.csv** – product groupings

**Scope:**

* Period: **2013 – 2015**
* Customers: **91**
* Orders: **830**
* Total Revenue: **≈ $1.27M**

---

### Data Cleaning (Power Query)

Key preprocessing steps:

* Data type standardization (dates, decimals, text IDs)
* Missing shipment handling for delivery analysis
* Duplicate validation of order IDs
* **Net revenue calculation:**
  `Unit Price × Quantity × (1 − Discount)`
* Delivery delay calculation using date differences
* Outlier validation without artificial capping

These steps mirror **real-world ETL and BI data quality practices**.

---

## 3. Data Modeling

A **star schema** was implemented for performance and scalability.

### Fact Table

**Sales Fact**

* Revenue
* Quantity
* Order count

### Dimension Tables

* Customers
* Products & Categories
* Date
* Employees
* Shippers

This structure enables **fast OLAP-style analysis**, dynamic filtering, and scalable reporting aligned with **Kimball dimensional modeling best practices**.

---

## 4. Key DAX Analytics

### Customer Metrics

* **Recency:** Days since last purchase
* **Frequency:** Number of orders
* **Monetary:** Net customer revenue

### RFM Scoring

Customers were ranked into **quartiles (1–4)** across R, F, and M to normalize comparisons and support segmentation.

### Customer Segments

Final segments include:

* **VIP / Champions** – high RFM, major revenue drivers
* **Loyal / High Value** – strong repeat purchasing
* **At Risk** – declining engagement
* **Lost / Inactive** – churned customers

This segmentation converts raw data into **targeted business actions**, enabling:

* Personalized marketing
* Retention campaigns
* Revenue optimization

---

## 5. Business Impact

The dashboard demonstrates how customer analytics can:

* Reveal **high-value revenue drivers**
* Detect **early churn signals**
* Improve **marketing efficiency and ROI**
* Support **strategic, data-driven decision-making**
<img width="1194" height="684" alt="Screenshot 2026-02-07 170800" src="https://github.com/user-attachments/assets/8b65caec-dcb5-4d05-91c8-e35080da287f" />
<img width="1213" height="681" alt="Screenshot 2026-02-07 170813" src="https://github.com/user-attachments/assets/58a88172-d152-41f7-a742-fbce07abbca8" />
<img width="1222" height="685" alt="Screenshot 2026-02-07 170825" src="https://github.com/user-attachments/assets/ca84d208-caaa-4dd3-aeb0-c01b321c1f22" />
<img width="1231" height="669" alt="Screenshot 2026-02-07 170835" src="https://github.com/user-attachments/assets/5539aa64-ff03-4ee9-867e-47c4044e5d8e" />

---

## 6. Tools & Technologies

* **Power BI** – dashboard development & DAX analytics
* **Power Query** – ETL and transformation
* **Dimensional Modeling** – star schema design
* **RFM Segmentation** – customer analytics framework
# Author

**Kehinde Daodu**
Data Analyst | Business Intelligence | Health & Operations Analytics
