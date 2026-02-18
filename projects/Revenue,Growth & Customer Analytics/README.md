# 📊 Online Retail II – Customer Retention & Revenue Intelligence Dashboard

## 🔎 Project Overview

This project transforms the **Online Retail II** dataset into a **scalable, executive-level business intelligence system** designed to analyze:

* Customer retention
* Repeat purchase behavior
* RFM segmentation
* Customer lifetime value (CLV)
* Cohort revenue trends
* Funnel leakage points

The goal was to build a **fully reproducible analytics workflow** — from raw data acquisition to **cloud-based BI dashboarding**.

---

## 🧠 Business Problem

E-commerce revenue growth depends on the ability to:

* Retain customers
* Increase repeat purchase rates
* Identify high-value customer segments
* Detect churn risk early

This project answers **three strategic business questions**:

1. **Who drives revenue?**
2. **Will revenue sustain over time?**
3. **Where are we losing growth opportunities?**

---

## 🛠️ Tech Stack

* **Python (Pandas)**
* **Google Colab**
* **Kaggle API**
* **Google Cloud Storage**
* **BigQuery** (SQL validation & hosting)
* **Looker Studio** (Executive dashboarding)
* **RFM Modeling**
* **Cohort Retention Analysis**

---

<img width="1919" height="940" alt="Screenshot 2026-02-17 224203" src="https://github.com/user-attachments/assets/51661945-1262-4d05-a0b1-6ef2cab137fb" />
<img width="1919" height="1003" alt="Screenshot 2026-02-17 224218" src="https://github.com/user-attachments/assets/ed5b85ae-c9d5-4a8e-bdb9-a181b44738e4" />
<img width="1854" height="793" alt="Screenshot 2026-02-18 130832" src="https://github.com/user-attachments/assets/f9863337-a70a-455e-a452-be745eaba5a5" />

<img width="1858" height="771" alt="Screenshot 2026-02-18 131311" src="https://github.com/user-attachments/assets/46e13e43-a8b6-4539-8cb2-4f2d50b8ea9e" />
<img width="1464" height="943" alt="Screenshot 2026-02-18 170951" src="https://github.com/user-attachments/assets/bd5c4f9c-7e85-4250-88dd-f62b6304da67" />


## 📦 Data Pipeline Architecture

The project follows a **cloud-native, reproducible analytics pipeline**:

1. Kaggle API configured securely in **Google Colab**
2. Dataset downloaded programmatically
3. Data cleaned and validated using **Pandas**
4. Large cleaned dataset uploaded to **Google Cloud Storage**
5. Loaded into **BigQuery** for scalable querying and validation
6. Connected live to **Looker Studio**
7. Interactive executive dashboards created

This architecture ensures:

* **Reproducibility**
* **Cloud scalability**
* **Business-intelligence readiness**

---

## 🧹 Data Cleaning & Preparation

### Key Cleaning Steps

* Removed duplicate transactions
* Filtered **Quantity ≤ 0** (returns and entry errors)
* Converted **InvoiceDate → datetime format**
* Cast **CustomerID** and **Invoice** as string fields
* Filled missing product descriptions
* Excluded rows with missing **CustomerID** for customer-level analysis

**Final cleaned dataset:**
➡ **1,044,421 valid customer transactions**

---

## 📈 Analytical Framework

### 1️⃣ Cohort Retention Analysis

* Customers grouped by **first purchase month**
* Retention percentage tracked across subsequent months
* Cohort **revenue matrix** constructed

**Key Insight:**
Retention drops sharply after **Month 1**, revealing **early churn risk**.

---

### 2️⃣ RFM Segmentation

Calculated for each customer:

* **Recency**
* **Frequency**
* **Monetary Value**

Customers segmented into:

* **Champions**
* **Loyal Customers**
* **Potential Loyalists**
* **At Risk**
* **Lost**

**Key Insight:**
Revenue is **heavily concentrated** among **Champions** and **Loyal Customers**.

---

### 3️⃣ Repeat Purchase & Customer Lifetime Value (CLV)

* **Repeat Purchase Rate:** **72%**
* **Average Order Value (AOV)** computed per customer
* **CLV = AOV × Frequency**

**Key Insight:**
High-value customers generate **disproportionate revenue contribution**.

---

## 📊 Executive Dashboard
<img width="988" height="745" alt="Screenshot 2026-02-18 172518" src="https://github.com/user-attachments/assets/a812435d-d64b-4d6e-a160-10c4485d4fa3" />

**Displays:**

* Total Revenue: **20.9M**
* Active Customers: **5,882**
* Repeat Purchase Rate: **72%**
* Revenue Trend (**2009–2011**)
* Revenue by Country
* Revenue by **RFM Segment**
* Average **CLV by Segment**

**Purpose:**
Provides a **rapid strategic overview** for executive decision-makers.

---

### 🔹 Customer Behaviour & Value

<img width="993" height="747" alt="Screenshot 2026-02-18 172530" src="https://github.com/user-attachments/assets/6758d366-ba21-4b01-8c50-397a91d83fde" />


**Displays:**

* Customer segment distribution
* Repeat vs. one-time customers
* Order frequency distribution
* AOV by segment

**Purpose:**
Explains **revenue drivers** and **customer engagement depth**.

---

### 🔹 Funnel & Growth Opportunities

<img width="987" height="748" alt="Screenshot 2026-02-18 172542" src="https://github.com/user-attachments/assets/185d3826-c839-468a-8c5e-580a8f384785" />


**Displays:**

* Purchase frequency funnel
* AOV vs. frequency relationship

**Purpose:**
Identifies **retention leakages** and **scalable growth levers**.

---

## 🚀 Business Recommendations

* Improve **second-purchase conversion** to reduce early churn
* Prioritize retention of **Champions** and **Loyal Customers**
* Launch lifecycle campaigns targeting **Potential Loyalists**
* Implement **re-engagement strategies** for **At-Risk** segments

## Link to the Dashboard on Looker Studio:https://lookerstudio.google.com/reporting/cb7f0a55-6a95-495a-ba14-98f9430bcad4

