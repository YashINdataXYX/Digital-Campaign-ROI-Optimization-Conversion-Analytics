# 📊 Digital Campaign ROI Optimization & Conversion Analytics

> **A full-stack Data Analytics portfolio project** — Meta (Facebook & Instagram) ad performance dashboard built in Power BI, covering the complete marketing funnel from impressions to purchases.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Yashraj-0A66C2?style=flat&logo=linkedin)](https://www.linkedin.com/in/yashraj33/)
[![GitHub](https://img.shields.io/badge/GitHub-YashINdataXYZ-181717?style=flat&logo=github)](https://github.com/YashINdataXYZ)
![Domain](https://img.shields.io/badge/Domain-Digital%20Marketing%20Analytics-1A56DB?style=flat)
![Tool](https://img.shields.io/badge/Tool-Power%20BI-F2C811?style=flat&logo=powerbi)
![Status](https://img.shields.io/badge/Status-Completed-0E9F6E?style=flat)

---

## 🗂️ Repository Structure

```
Digital-Campaign-ROI-Optimization-Conversion-Analytics/
│
├── 📄 README.md
│
├── 📁 docs/
│   ├── 01_Project_Explanation_Interview.docx
│   ├── 02_Domain_Knowledge_Document.docx
│   ├── 03_Dashboard_Insights.docx
│   └── 04_Business_Requirements_Document.docx
│
├── 📁 dashboard/
│   └── Meta_Ad_Performance_Dashboard.pbix   ← Power BI file
│
├── 📁 data/
│   ├── ad_events.csv
│   ├── ads.csv
│   ├── campaigns.csv
│   └── users.csv
│
└── 📁 screenshots/
    └── dashboard_preview.png
```

---

## 🎯 Project Overview

This project analyzes **Meta (Facebook & Instagram) advertising campaign performance** using a Power BI dashboard. It tracks the full marketing funnel — from ad impressions and clicks through to final purchases — and surfaces insights across demographics, geography, time, and ad formats.

### Business Problem
The marketing team needed a centralized view of campaign performance to answer:
- Are our ads reaching the right audience?
- Where is the funnel losing efficiency?
- Which ad formats and platforms deliver the best ROI?
- When and where should we concentrate ad spend?

---

## 📐 Data Model — Star Schema

```
        ┌─────────────┐
        │  campaigns  │ ← budget, dates, duration
        └──────┬──────┘
               │ campaign_id
        ┌──────┴──────┐
        │     ads     │ ← platform, type, targeting
        └──────┬──────┘
               │ ad_id
        ┌──────┴──────┐      ┌───────┐
        │  ad_events  │──────│ users │ ← demographics, country
        │  (FACT)     │      └───────┘
        └─────────────┘
```

| Table | Type | Key Fields |
|-------|------|------------|
| `ad_events` | Fact | event_id, ad_id, user_id, timestamp, event_type |
| `ads` | Dimension | ad_id, campaign_id, ad_platform, ad_type, target_gender |
| `campaigns` | Dimension | campaign_id, name, start_date, total_budget |
| `users` | Dimension | user_id, user_gender, age_group, country, interests |

---

## 📈 Key KPIs & Results

| KPI | Value | Benchmark | Status |
|-----|-------|-----------|--------|
| Impressions | 216,000 | — | ✅ Strong Reach |
| Clicks | 25,400 | — | ✅ High Volume |
| CTR | **11.76%** | 1–2% | 🚀 Excellent |
| Engagement Rate | **13.56%** | ~3% | 🚀 Excellent |
| Conversion Rate | 5.21% | 2–5% | ✅ Good |
| Purchase Rate | 0.61% | ~1% | ⚠️ Needs Work |
| Total Budget | 2.5M | — | — |
| Avg. Budget / Campaign | 50.7K | — | — |

---

## 💡 Key Insights

### 🔺 Funnel Analysis
- **Top of funnel is strong** — CTR of 11.76% is nearly 6× the industry average, confirming effective ad creatives and targeting.
- **Bottom of funnel is leaking** — only 0.61% of impressions convert to purchases, indicating issues with landing page experience, audience mismatch, or offer strength.

### 👥 Audience
- Females (43%) engage more than males (22%) — campaigns should lean into female-centric messaging.
- The **18–30 age group** drives the majority of interactions.

### 🌍 Geography
- **India & Brazil** — highest engagement volume → best for reach-focused campaigns.
- **Germany & UK** — higher purchasing power → best for conversion-focused premium campaigns.

### ⏰ Timing
- Peak engagement: **15:00–20:00 hrs** (afternoon & evening).
- Engagement spikes on specific calendar dates (19th–21st, 25th–27th) — likely tied to promotions.

### 📹 Ad Format Performance
| Ad Type | CTR | Conversion Rate | Engagement Rate |
|---------|-----|-----------------|-----------------|
| **Video** ⭐ | 11.9% | 5.2% | 13.7% |
| Stories | 11.8% | 5.2% | 13.6% |
| Carousel | 11.7% | 5.1% | 13.4% |
| Image | 11.7% | 4.9% | 13.5% |

---

## ✅ Recommendations

1. **Optimize the conversion funnel** — A/B test landing pages, improve CTAs, and deploy retargeting for non-converting engagers.
2. **Refine targeting** — Double down on females aged 18–30 in India and Brazil.
3. **Shift budget to Video & Stories** — They deliver the highest CTR and conversion rates.
4. **Schedule ads** for afternoon/evening slots (15:00–20:00).
5. **Segment geographic strategy** — Volume campaigns in India/Brazil; high-value conversion campaigns in Germany/UK.

---

## 📁 Project Documents

| Document | Description |
|----------|-------------|
| [📋 Project Explanation (Interview)](./docs/01_Project_Explanation_Interview.docx) | Step-by-step guide to presenting this project in a data analyst interview |
| [📚 Domain Knowledge Document](./docs/02_Domain_Knowledge_Document.docx) | Data architecture, table schemas, and star schema explanation |
| [📊 Dashboard Insights](./docs/03_Dashboard_Insights.docx) | Full KPI analysis, chart breakdowns, and business insights |
| [📝 Business Requirements Document](./docs/04_Business_Requirements_Document.docx) | Stakeholder requirements, KPI definitions, and chart specifications |

---

## 🛠️ Tools & Skills

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-0078D4?style=for-the-badge)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Excel](https://img.shields.io/badge/Excel-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white)

- **Power BI** — Dashboard design, DAX measures, dynamic parameters
- **Star Schema Modeling** — Fact + Dimension table architecture
- **DAX** — CTR, Conversion Rate, Purchase Rate, ROAS calculations
- **Marketing Analytics** — Funnel analysis, audience segmentation, ROI optimization

---

## 🤝 Connect With Me

- 💼 **LinkedIn:** [linkedin.com/in/yashraj33](https://www.linkedin.com/in/yashraj33/)
- 💻 **GitHub:** [github.com/YashINdataXYZ](https://github.com/YashINdataXYZ)

---

*Built as a portfolio project to demonstrate end-to-end data analytics skills — from business requirements through data modeling, dashboard development, and stakeholder communication.*
