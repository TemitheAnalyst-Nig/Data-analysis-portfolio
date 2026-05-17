# 🏥 HealthClaim Analytics — Healthcare Claims Power BI Dashboard

> A 6-page interactive Power BI dashboard analysing **52,000+ synthetic 
> patient claims** across **20 Nigerian healthcare providers** (2020–2024).  
> Built to surface cost drivers, fraud patterns, and operational bottlenecks 
> in a healthcare claims processing system.
---


## 🎯 Project Objective

Healthcare insurance fraud, billing inefficiencies, and SLA breaches 
cost the system billions annually. This project simulates a real-world 
claims analytics environment to answer four critical questions:

1. **Where is the money going?** — Cost by service type and diagnosis
2. **Is fraud happening?** — Duplicate claims, outlier amounts, approval anomalies
3. **Why is processing slow?** — SLA tracking and bottleneck identification
4. **What should leadership do?** — Data-backed recommendations

---

## 📊 Dashboard Pages

| # | Page | Purpose |
|---|---|---|
| 1 | Executive Summary | KPIs, monthly trends, provider performance overview |
| 2 | Claims Performance Analysis | Cost drivers by service type, diagnosis, and provider |
| 3 | Fraud & Anomaly Detection | Outlier claims, duplicates, suspicious approval rates |
| 4 | Processing & Operational Efficiency | SLA compliance, bottlenecks, processing time breakdown |
| 5 | Key Insights | Summary of all data-driven findings |
| 6 | Recommendations | Actionable next steps for operations and leadership |

---

## 🔍 Key Findings

### 💰 Cost
- Surgery averages **₦339,262 per claim** — 16x more expensive than Consultation (₦15,097)
- Consultation is the **highest volume** service but the lowest cost per claim
- **Federal Medical Centre Owerri** leads total claim spend at ₦190M+
- **FMC Calabar** handles the highest patient volume across all providers

### 🚨 Fraud & Anomalies
- **1,400 high-value claims** flagged above the anomaly threshold
- **8 confirmed duplicate claim patterns** — same Patient ID, same date, same service type
- Example: PAT009139 submitted identical Consultation claims on June 25, 2024
- Several providers show approval rates clustering tightly around 65–67% — worth monitoring

### ⏱ Operational Efficiency
- Overall average processing time: **7.52 days** (approved claims only)
- Pending claims average **27.47 days** — nearly **4x slower** than approved
- Rejected claims average **12.02 days**
- **SLA compliance rate: only 14%** — critical gap requiring urgent intervention
- **5,139 claims delayed** beyond acceptable limits

### 📊 Volume
- 52,000 total claims | **65% Approved** | **20% Rejected** | **15% Pending**
- Claim volume stable across 2020–2024 with no major seasonal spike

---

## ✅ Recommendations

| # | Recommendation |
|---|---|
| 1 | Implement pre-authorization review for all Surgery claims above ₦500,000 |
| 2 | Create a fast-track queue for low-value Consultation and Pharmacy claims |
| 3 | Add uniqueness check (Patient_ID + Date + Claim_Type) at point of submission |
| 4 | Prioritise triage of high-value pending Surgery claims immediately |
| 5 | Conduct quarterly SLA review meetings with the bottom 5 performing providers |

---

## 🛠 Tools & Techniques

| Tool | How it was used |
|---|---|
| **Power BI Desktop** | Dashboard design, visuals, navigation, dark theme |
| **DAX** | KPI measures, SLA rate %, duplicate detection, TOPN, DIVIDE |
| **Power Query (M)** | Data cleaning, processing bucket columns, data type formatting |
| **Microsoft Excel** | Dataset generation — 52,000 rows across 3 related tables |

### DAX Measures Written
```dax
Approval Rate % = DIVIDE([Total Approved], [Total Claims], 0)
SLA Rate %      = DIVIDE([Claims Within SLA], [Total Claims], 0)
Claims Delayed  = CALCULATE(COUNTROWS('Claims Data'), 
                    'Claims Data'[Processing_Days] > 21)
High Value Claims = CALCULATE(COUNTROWS('Claims Data'), 
                    'Claims Data'[Claim_Amount] > 500000)
Fastest Provider Avg = MINX(VALUES('Claims Data'[Provider_Name]), 
                    [Avg Processing Time])
```

---

## 📁 Dataset Structure

| Table | Rows | Key Columns |
|---|---|---|
| Claims Data | 52,000 | Claim_ID, Patient_ID, Provider_Name, Claim_Date, Claim_Type, Claim_Amount, Status, Processing_Days, Diagnosis_Category |
| Provider Data | 20 | Provider_Name, Hospital_Type, Location, Total_Patients |
| Time Dimension | 1,827 | Date, Month, Quarter, Year |

**Data model:** Star schema — Claims Data as fact table, Provider Data 
and Time Dimension as dimension tables, linked by Provider_Name and Claim_Date.

---

## 💡 What This Project Demonstrates

- ✅ Full end-to-end analytics workflow — raw data → model → insight → recommendation
- ✅ Fraud detection logic using DAX and scatter plot anomaly identification  
- ✅ SLA and operational KPI tracking for executive reporting
- ✅ Professional multi-page dashboard design with consistent branding
- ✅ Data storytelling — every page answers a specific business question

---

## 📬 Connect With Me
[LinkedIn —www.linkedin.com/in/daodu-kehinde )  
Open to **Data Analyst · Business Intelligence · Healthcare Analytics** roles
