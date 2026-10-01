# RetailIQ — Retail Sales & Analytics

> **End-to-end analytics project analyzing 50,000 omnichannel retail transactions to identify profit leakage, return-risk, and growth opportunities.**

## 📊 At a Glance

| KPI                 |          Result |
| ------------------- | --------------: |
| **Revenue**         |     **$2.356B** |
| **Gross Profit**    |    **$403.67M** |
| **Profit Margin**   |      **17.14%** |
| **Orders**          |      **50,000** |
| **AOV**             |     **$47,110** |
| **Return Rate**     |      **50.05%** |
| **Returned Orders** |      **25,026** |
| **Return Value**    |     **~$1.18B** |
| **CSAT**            | **3.00 / 5.00** |
| **Delivery Time**   |     **~4 Days** |

---

## 🎯 Business Objective

RetailIQ diagnoses:

* **Discount-driven margin erosion**
* **High product return rates**
* **Category and product profitability**
* **Regional revenue concentration**
* **Operational inefficiencies**
* **B2B enterprise growth opportunities**

The project combines data engineering, statistical analysis, dashboarding, data-quality auditing, and commercial strategy.

---

## 🔎 Key Findings

### 💸 Discount Leakage

* **0% discount:** ~27.6% margin
* **21%+ discount:** ~3.4% margin
* **5,057 loss-making orders**

### 🔄 Returns

* **50.05% overall return rate**
* **~$1.18B** in gross order value associated with returns
* Highest-return products include **Monitors (51.6%)** and **Laptops (51.3%)**

### 📦 Category Concentration

* **Electronics:** ~$1.13B
* **Home Appliances:** ~$472M
* Combined: **~81.5% of revenue**

### 🌍 Regional Concentration

| Region      | Revenue |
| ----------- | ------: |
| Maharashtra |  ~$252M |
| Kerala      |  ~$248M |
| Telangana   |  ~$241M |

> Geographic reporting is restricted to macro-state level because the audit identified city/state mapping inconsistencies.

---

## 💡 Strategic Recommendations

| Priority | Action                                                                      | Timeline   |
| -------- | --------------------------------------------------------------------------- | ---------- |
| **1**    | Cap promotional discounts at **10–15%** and require approval above 15%      | Day 1–30   |
| **2**    | Audit product quality, listings, packaging, delivery, and reverse logistics | Day 31–60  |
| **3**    | Expand high-margin SKUs and introduce structured **B2B enterprise tiers**   | Day 61–90+ |

### Scenario Impact

The base-case scenario models:

* **21.5% projected margin**
* **+$100M–$115M estimated annual profit lift**
* **~$590M capital liberated**

*These are scenario estimates based on stated assumptions, not realized financial outcomes.*

---

## 📈 Executive Dashboard

The Q4 dashboard provides a single-view command center with filters for:

**Category · Region · Channel · Year · Age Group**

### Six Core Visuals

1. Monthly Revenue & Profit Trend
2. Category Performance
3. Discount Band Profitability
4. Age Cohort Revenue
5. Regional Revenue
6. Product Revenue & Margin

---

## ⚙️ Data Engineering

The project uses Google Sheets `ARRAYFORMULA`, `QUERY`, `SUMIFS`, and Pivot Tables.

Eight calculated fields were created:

```text
Delivery_Days
Profit_Margin
Return_Flag
Age_Group
Order_Year
Order_Month
Order_Quarter
Discount_Band
```

Example:

```excel
=ARRAYFORMULA(IF(ISBLANK(Q2:Q),"",R2:R-Q2:Q))
```

---

## 🧪 Analysis

Methods include:

* Group-by & aggregation
* Correlation analysis
* Two-sample t-tests
* Chi-Square testing
* Trend analysis
* Margin analysis
* Return-rate analysis
* Sensitivity analysis
* Data-quality auditing

---

## 🛡️ Data Quality

The audit identified three major decision risks:

**Geographic corruption**
City/state mappings contain inconsistencies → use macro-state reporting only.

**Customer ID non-uniqueness**
Customer IDs map to multiple names/ages/states → avoid raw-ID-based CLV or churn analysis.

**Synthetic distributions**
Channel, return, and rating distributions are unusually uniform → interpret statistical relationships cautiously.

**Financial caveat:** reported profit represents gross profitability before costs such as freight, payment fees, marketing CAC, and reverse logistics.

---

## 🗂️ Repository Structure

```text
retailiq-sales-analytics/
├── data/
├── google_sheets/
├── dashboard/
├── presentation/
└── README.md
```

### Workbook

```text
Data
Calc_Data
Q1: Project Charter
Q2: Strategic Problems
Q4: Executive Dashboard
Q5: Diagnostic Q&A
Q6: Data Quality Audit
Q7: Strategic Roadmap
```

---

## 🛠️ Tech Stack

**Analysis:** Google Sheets · `ARRAYFORMULA` · `QUERY` · `SUMIFS` · Pivot Tables

**Visualization:** Google Sheets Charts · PowerPoint

**Documentation:** Markdown · Git · GitHub

---

## 🚀 Reproduce

```bash
git clone https://github.com/<your-username>/retailiq-sales-analytics.git
cd retailiq-sales-analytics
```

Then review:

```text
Calc_Data                  → Data preparation & calculations
Q4: Executive Dashboard    → Interactive analysis
Q6: Data Quality Audit     → Data limitations
Q7: Strategic Roadmap      → Recommendations
```

---

## 🔮 Next Steps

* A/B test price elasticity with controlled discount caps
* Build a true **Net Cash Realization Model**
* Clean the customer master data for reliable CLV analysis
* Expand B2B segmentation and enterprise profitability analysis

---

## 👤 Author

**Akash Ojha**
Lead Analyst — RetailIQ Sales Analytics

**Focus:** Data Analytics · Business Intelligence · Sales Analytics · B2B Opportunity Analysis

**Dataset:** Kaggle RetailIQ Omni-Channel E-Commerce Dataset

---

⭐ **If you find this project useful, consider starring the repository.**
