# 🎬 Netflix Userbase Data Analysis Dashboard

### A Power BI Subscription & Engagement Analytics Project

---

## 📌 Table of Contents

1. [Project Overview](#-project-overview)
2. [Dashboard KPIs](#-dashboard-kpis)
3. [Dashboard Architecture](#-dashboard-architecture)
4. [Detailed Findings](#-detailed-findings)
5. [Key Insights & Narrative](#-key-insights--narrative)
6. [Data Validation Notes](#-data-validation-notes)
7. [Recommendations](#-recommendations)
8. [Tools & Tech Stack](#-tools--tech-stack)
9. [How to Use This Repo](#-how-to-use-this-repo)
10. [Author](#-author)
11. [Disclaimer](#-disclaimer)

---

## 🎯 Project Overview

This project analyzes a **2,500-user Netflix subscriber dataset** using Power BI, producing a single-page interactive dashboard that covers revenue performance, subscription tier distribution, user demographics, device usage patterns, geographic reach, and year-over-year growth. The goal is to give a Netflix-style subscription business a fast, visual read on **where revenue comes from, who the users are, and how engagement is trending** — the three pillars any subscription-based streaming platform needs to monitor to manage growth and monetization.

---

## 📊 Dashboard KPIs

<img width="1426" height="799" alt="Netflix dashboard" src="https://github.com/user-attachments/assets/d02f2dd3-3e14-4bdd-932a-b3db0e31648c" />

Dashboard Link: https://app.powerbi.com/view?r=eyJrIjoiOTVkZmRlOWMtZGJjYy00OWRjLWJlMDctY2FhZjNiM2VhYmM0IiwidCI6ImU2M2U3ZmQyLTk4ZjktNDNhMS1iNmU4LTg5ZDE1M2Q1OTg5MCJ9

Four headline KPI cards summarize platform performance:

| KPI | Value |
|---|---|
| **Total Revenue** | $31.27K |
| **Total Users** | 2,500 |
| **ARPU (Average Revenue Per User)** | $12.51 |
| **Premium Users %** | 29.32% |

**Quick math check:** Total Revenue ÷ Total Users = $31,270 ÷ 2,500 = **$12.51**, which reconciles exactly with the displayed ARPU — confirming the KPI card math is internally consistent.

---

## 🏗️ Dashboard Architecture

The dashboard is a **single interactive canvas**, organized into five zones plus global filters:

### Global Slicers
- **Age Group:** Select All, Adult, Senior, Young Adult
- **Subscription Type:** Select All, Basic, Premium, Standard
- **Country:** Select All, Australia, Brazil, Canada, France, Germany, Italy, Mexico, Spain, United Kingdom, United States

### Revenue by Subscription Type
Vertical bar chart comparing total revenue contribution across the three subscription tiers (Basic, Standard, Premium).

### Users by Age Group
Donut chart breaking the user base down into Adult, Young Adult, and Senior segments.

### Revenue by Country
World map visual showing geographic revenue concentration, with visibly stronger shading over North America and Europe.

### Device Usage Analysis
Bar chart comparing user counts across Laptop, Tablet, Smartphone, and Smart TV.

### Yearly Growth
A triangular area/line chart plotting revenue across 2021, 2022, and 2023.

---

## 🔎 Detailed Findings

### Revenue by Subscription Type
| Tier | Revenue | Share of Total |
|---|---|---|
| **Basic** | $12.5K | ~40% |
| Standard | $9.6K | ~31% |
| Premium | $9.2K | ~29% |

The three tiers sum to approximately $31.3K, closely matching the $31.27K Total Revenue KPI. **Basic is the single largest revenue contributor**, despite presumably carrying the lowest per-user price point — meaning the platform's revenue is being driven primarily by *volume* in the entry-level tier rather than by upselling users into higher-value plans.

### Users by Age Group
| Age Group | Share |
|---|---|
| **Adult** | 59.64% |
| Young Adult | 36.64% |
| Senior | 3.72% |

Nearly 96% of the user base falls into the Adult or Young Adult segments, with Seniors representing a small minority (3.72%) of total users — a clear demographic concentration in the working-age population.

### Device Usage Analysis
| Device | User Count |
|---|---|
| Laptop | 636 |
| Tablet | 633 |
| Smartphone | 621 |
| Smart TV | 610 |

These four device counts sum to **exactly 2,500** — matching the Total Users KPI precisely, confirming this visual represents each user's single primary/registered device rather than overlapping multi-device usage. Usage is tightly clustered (a spread of only 26 users, or ~4%, between the highest and lowest device), indicating no single device type dominates access to the platform.

### Revenue by Country
The map visual shows a global footprint across at least 10 countries (Australia, Brazil, Canada, France, Germany, Italy, Mexico, Spain, United Kingdom, United States), with visibly heavier shading concentrated over North America and parts of Europe — consistent with those being more mature, higher-revenue markets for the platform.

### Yearly Growth
| Year | Revenue |
|---|---|
| 2021 | $176 |
| **2022** | **$30,635** |
| 2023 | $460 |

This is the most striking pattern in the dashboard: revenue surged from a near-zero base of $176 in 2021 to **$30,635 in 2022** — representing the vast majority of the platform's cumulative $31.27K in total recorded revenue — before collapsing back down to $460 in 2023. In practical terms, **2022 alone accounts for roughly 98% of all revenue captured in this dataset.**

---

## 💡 Key Insights & Narrative

**Monetization is volume-driven, not value-driven.** With Basic contributing the most total revenue ($12.5K) despite being the lowest-priced tier, and Premium trailing at $9.2K despite carrying the highest per-user price, the platform's revenue engine currently runs on subscriber count in the cheapest tier rather than on converting users into higher-value plans. Combined with a Premium penetration of 29.32% of the user base, this points to real headroom in upselling and plan-conversion strategy.

**The user base skews working-age, with a Senior gap.** Adults (59.64%) and Young Adults (36.64%) together represent 96.28% of users, while Seniors sit at just 3.72%. This suggests content curation, UX, and pricing are currently tuned for younger and middle-aged audiences — and that Senior engagement represents an underexplored growth segment rather than a saturated one.

**Device access is genuinely balanced.** With device counts ranging narrowly between 610 and 636 (and summing exactly to the 2,500-user base), the platform isn't dependent on any single access point. This is a strength: any UX or performance investment needs to be spread evenly across Laptop, Tablet, Smartphone, and Smart TV rather than prioritized toward one channel.

**Geographic reach is broad but revenue is concentrated in mature markets.** The stronger shading over North America and Europe on the revenue map suggests these regions are the primary monetization engines today, while other represented countries (Brazil, Mexico) may reflect real user acquisition without matching revenue — a signal worth investigating for pricing sensitivity or localization gaps.

**2022 was an outlier year, not a growth trajectory.** The yearly revenue pattern ($176 → $30,635 → $460) is not a steady growth curve — it's a single dramatic spike. Whatever drove 2022's revenue (content releases, promotional pricing, a data collection artifact, or a genuine one-off surge) did not carry into 2023. This is the single most important trend for stakeholders to interrogate before drawing any growth conclusions from this dashboard.

---

## ⚠️ Data Validation Notes

In the interest of a fully robust GitHub report, one figure discrepancy is worth flagging explicitly:

- **Premium Users % discrepancy:** The dashboard's KPI card clearly displays **29.32%**, while the accompanying narrative text describes Premium penetration as **26.32%**. These are close but not identical — likely a transcription difference between the live dashboard and the written summary rather than two different calculations. **This report uses the dashboard's displayed 29.32% as the primary figure**, since it can be directly verified against the visual; the 26.32% figure should be reconciled against the underlying `.pbix` file before being cited externally.
- **Background/overlapping page content:** The dashboard screenshot shows faint overlapping text and imagery in places (e.g., partial references to "Release Calendar," "The Witcher," "Money Heist," "Top Genres," and a "860h" watch-time figure) that appear to belong to a *different* report page (likely a content/catalog page) bleeding through behind the userbase analytics page in the exported image, rather than being part of the Userbase Data Analysis page itself. This report does not treat that bled-through content as authoritative data for the userbase dashboard — it's flagged here for transparency and should be double-checked against the live `.pbix` file, where each page should render cleanly on its own.
- **Revenue-by-tier reconciliation:** Basic + Standard + Premium ($12.5K + $9.6K + $9.2K = $31.3K) is very close to, but not exactly equal to, the $31.27K Total Revenue KPI — a difference of about $30, consistent with normal display rounding at the "K" level rather than a data integrity issue.

---

## 🧭 Recommendations

1. **Investigate the 2022 revenue spike and 2023 decline** as the top priority — understanding whether this reflects genuine user behavior (a churn event, a pricing change, a content-driven surge) or a data collection artifact is essential before this dashboard is used to inform any growth strategy.
2. **Design a Premium upsell strategy** targeting Basic-tier users, given that Basic drives the most total revenue but Premium penetration sits at under 30% — small conversion gains here could meaningfully shift the Basic/Standard/Premium revenue mix.
3. **Build a Senior-focused content and pricing pilot**, given this segment's near-3.72% share may reflect an underpenetrated opportunity rather than genuine disinterest.
4. **Compare user acquisition vs. revenue by country** directly (rather than only revenue), to identify whether markets like Brazil and Mexico have real user bases that are simply monetizing at lower ARPU — a localization/pricing opportunity rather than a growth ceiling.
5. **Reconcile the Premium % discrepancy** between the dashboard (29.32%) and the written summary (26.32%) against the source data model before this report is published externally.
6. **Verify page isolation in the exported dashboard** to eliminate the cross-page visual bleed-through noted above, ensuring the published screenshot cleanly represents only the Userbase Analysis page.

---

## 🛠️ Tools & Tech Stack

| Tool | Purpose |
|---|---|
| **Microsoft Power BI** | Dashboard build, DAX measures (Total Revenue, ARPU, Premium %), map and donut visualizations |
| **Power Query** | Data cleaning and transformation prior to modeling |
| **DAX** | Total Revenue, Total Users, ARPU, Premium Users % calculated measures |
| **Slicers** | Interactive filtering across Age Group, Subscription Type, and Country |

---

## 📂 How to Use This Repo

```
├── data/
│   └── netflix_userbase_dataset.csv
├── dashboard/
│   └── netflix_userbase_dashboard.pbix
└── README.md
```

1. Clone or download this repository
2. Open `netflix_userbase_dashboard.pbix` in **Power BI Desktop** to explore the live dashboard
3. Use the **Age Group / Subscription Type / Country** slicers to filter all visuals interactively
4. Cross-check the Premium Users % and Yearly Growth figures against the raw dataset before citing them externally, per the [Data Validation Notes](#-data-validation-notes) above

---

## 👤 Author

**(Yusuf Shotunde, LinkedIn: www.linkedin.com/in/yusuf-shotunde / GitHub: https://github.com/Yusinho / CV: https://github.com/Yusinho/my-portfolio/blob/main/Yusuf_Lanre_Shotunde_CV.pdf )**

---

## 📄 Disclaimer

This project was built for **portfolio and educational demonstration purposes** using a simulated Netflix-style userbase dataset. It is not affiliated with or endorsed by Netflix, Inc. All figures in this report are drawn directly from the dashboard visuals and accompanying narrative; the discrepancies and overlapping-content artifacts noted in the Data Validation Notes section should be resolved against the source `.pbix` file before any figures here are used in an external or professional context.



