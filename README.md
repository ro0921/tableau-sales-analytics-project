# 📊 Retail Sales & Customer Intelligence Dashboard Suite
### Tableau | Business Analytics | KPI-Driven Decision Support | 2023 vs. 2022

---

## 🧭 Business Problem

A retail business generating hundreds of thousands in annual revenue lacked a consistent, self-service way for leadership to understand whether growth was actually profitable — and which customers and product categories were driving outcomes.

Month-end reviews relied on spreadsheet exports that showed totals but offered no narrative: *Was the growth in the right categories? Were high-volume subcategories margin-positive or margin-draining? Were customers becoming more loyal, or was the revenue base shallow?*

This project was built to eliminate that ambiguity. Two purpose-built dashboards — one focused on commercial performance, one on customer behavior — give stakeholders the ability to answer these questions in seconds, not hours.

---

## 🎯 Project Objective

Design and deliver a two-dashboard Tableau analytics suite that:

- Tracks and contextualizes core sales and profit KPIs against the prior year
- Identifies which product subcategories are profitable versus margin-dilutive
- Reveals customer loyalty patterns, purchase frequency distributions, and top-account profitability
- Enables leadership to make faster, more confident decisions about where to invest, where to protect, and where to course-correct

The project followed a structured 4-phase BI delivery methodology: requirements analysis, data source construction, chart development, and dashboard assembly — mirroring professional BI project standards.

---

## 📐 Dashboard Overview

### Dashboard 1 — Sales Dashboard | 2023

Designed for **sales leadership, category managers, and finance teams**.

| Visual Component | Purpose |
|---|---|
| Total Sales BAN + Sparkline | Top-line revenue health with monthly trend and YoY % change |
| Total Profit BAN + Sparkline | Margin performance; growth quality indicator |
| Total Quantity BAN + Sparkline | Volume signal; flags discounting risk when growing faster than profit |
| Sales & Profit by Subcategory | Dual-bar visual isolating profitable vs. loss-generating product categories |
| Sales & Profit Trends over Time | Period-level trend chart with average benchmarks; blue = above average, orange = below |

**2023 Headline Numbers:** $733K in Sales (▲20.4%), $93K Profit (▲12.5%), 12K Units (▲26.8%)

---

### Dashboard 2 — Customer Dashboard | 2023

Designed for **CRM teams, account managers, and commercial strategy leads**.

| Visual Component | Purpose |
|---|---|
| Total Customers BAN + Sparkline | Customer base growth; acquisition health signal |
| Sales Per Customer BAN + Sparkline | Revenue efficiency per relationship; rising = better monetization |
| Total Orders BAN + Sparkline | Engagement depth; faster growth than customers = increased purchase frequency |
| Customer Distribution by Nr. of Orders | Histogram revealing loyalty depth — shape of distribution tells the retention story |
| Top 10 Customers by Profit | Named account ranking with last order date, 2023 profit, 2023 sales, and order count |

**2023 Headline Numbers:** 693 Customers (▲8.6%), $1,058 Sales/Customer (▲10.8%), 1,687 Orders (▲28.3%)

---

## 🛠️ Tools & Technologies Used

| Tool | Usage |
|---|---|
| Tableau Desktop | Dashboard design, chart development, interactivity, calculated fields |
| Tableau Public | Publication and portfolio hosting |
| Microsoft Excel / CSV | Data source preparation |
| Hand-drawn wireframing | Dashboard mockup design before Tableau build |

---

## 📁 Dataset Information

- **Source:** Superstore Retail Dataset (transactional retail data)
- **Scope:** 2022–2023 (two fiscal years for YoY comparison)
- **Key Dimensions:** Order Date, Category, Sub-Category, Customer Name, Region, City
- **Key Measures:** Sales, Profit, Quantity, Orders
- **Granularity:** Order line level

---

## 🧹 Data Cleaning & Preparation

The data preparation phase followed a structured process before any visualization was built:

- **Connected** the data source and validated the relationship between order and customer tables
- **Renamed fields** to business-friendly labels (e.g., "Sales" instead of raw column headers)
- **Validated data types** — ensuring date fields parsed correctly for time intelligence calculations
- **Checked for nulls and anomalies** — particularly in profit columns where negative values required validation against expected subcategory behavior
- **Created calculated fields** for all KPIs requiring derived logic:
  - YoY Sales Growth %
  - YoY Profit Growth %
  - Sales Per Customer (FIXED LOD expression)
  - Highest/Lowest Month flags for sparkline dot encoding
  - Above/Below Average flags for trend chart color encoding

---

## ✨ Dashboard Features

- **YoY Comparison Sparklines** — Each KPI tile displays the full-year monthly trend for 2023 vs. 2022, with the highest month (blue dot) and lowest month (orange dot) called out automatically
- **Cross-Dashboard Navigation** — Icon-based navigation buttons allow seamless switching between Sales and Customer dashboards without leaving the workbook
- **Dynamic Filter Panel** — Category, Sub-Category, Region, and City filters apply across all charts simultaneously
- **Profit/Loss Color Encoding** — Subcategory profit bars use blue (profit) and orange (loss) to create immediate visual separation without requiring a legend
- **Average Reference Lines** — Trend charts include horizontal average benchmarks, enabling users to classify any given period as above or below typical performance
- **Custom Tooltips** — All chart elements display business-formatted tooltip information with proper currency formatting and contextual labels

---

## 📌 KPI Explanations

**Total Sales** — Gross revenue generated in the selected period. Primary indicator of commercial scale.

**Total Profit** — Net profit after costs. Profitability growing slower than revenue signals margin compression — a critical flag for category and pricing strategy.

**Total Quantity** — Number of units sold. Growing significantly faster than profit suggests discounting activity or mix shift toward lower-margin items.

**Sales Per Customer** — Total Sales ÷ Distinct Customer Count. Rising value indicates the business is extracting more value per relationship — a sign of healthier customer engagement.

**Total Orders** — Distinct transaction count. When orders grow faster than customers, existing customers are purchasing more frequently — a leading indicator of loyalty improvement.

**Customer Distribution by Nr. of Orders** — A frequency distribution of customers segmented by how many orders they placed in the year. A steep drop-off after 1-2 orders signals a loyalty conversion challenge.

**Top 10 Customers by Profit** — Ranks individual customers by the profit they contributed, surfacing account concentration risk and enabling targeted relationship management.

---

## 💡 Business Insights

**1. Revenue is growing, but profit is lagging — intentionally investigate why.**
Sales grew 20.4% while profit grew only 12.5%. The subcategory breakdown reveals that Tables and Machines are operating at a net loss. Revenue growth obscures this without category-level drill-down.

**2. Copiers deliver the strongest profit-to-sales ratio.**
Despite modest absolute sales volume, the Copiers subcategory generates disproportionate margin — a signal for where pricing power exists.

**3. Orders are growing 3× faster than customers.**
This is a positive signal — it means existing customers are re-engaging more frequently. The business is deepening relationships, not just adding new ones.

**4. Over half of customers placed only 1-2 orders in 2023.**
The loyalty distribution is front-heavy. The organization has an opportunity to convert single-purchase customers into repeat buyers — a relatively low-cost growth lever.

**5. Top 10 customers account for significant profit concentration.**
Raymond Buch alone contributed $6,781 in profit. Understanding the profile of these accounts — and building retention strategies around them — is a direct profit protection initiative.

---

## 🧱 Challenges Faced

**1. Designing two dashboards as a connected system, not two isolated reports**
The navigation and layout consistency challenge required deliberate architectural planning — shared color palettes, consistent container structures, and cross-dashboard icon navigation.

**2. YoY comparison without visual clutter**
Layering two years of trend data required clear visual hierarchy: 2023 as the dominant black line, 2022 as a subordinate grey — with the YoY delta surfaced on the BAN tile rather than requiring mental calculation.

**3. Communicating profit losses without creating an alarm-dashboard**
Orange encoding (rather than red) for loss subcategories maintains analytical urgency without triggering defensive reactions from stakeholders reviewing the dashboard.

**4. Customer-level KPI aggregation across filters**
Sales Per Customer required LOD (Level of Detail) expressions to ensure the denominator (customer count) correctly reflected the filtered dataset — not the full database.

**5. Container layout architecture**
Tableau's nested container system required planning on paper before building. The dashboard uses a main Vertical Container with nested Horizontal Containers for the title row, KPI row, and chart row — aligned with inner/outer padding calibration.

---

## ✅ Solutions Implemented

| Challenge | Solution |
|---|---|
| Cross-dashboard navigation | Shared icon buttons with dashboard navigation actions |
| YoY visual hierarchy | Primary year in black; prior year in grey; delta on BAN tile |
| Profit loss encoding | Blue = profit, Orange = loss — analytical flag, not alarm signal |
| Customer KPI aggregation | FIXED LOD expressions for denominator accuracy |
| Layout consistency | Container mockup sketched before build; inner/outer padding standardized |
| Highest/Lowest month flags | Calculated fields using WINDOW_MAX / WINDOW_MIN logic |

---

## 🎓 Key Learnings

- **Container architecture must be planned before building.** A 15-minute wireframe sketch prevented hours of layout debugging.
- **Chart selection is a storytelling decision, not a technical one.** The customer distribution histogram was chosen because its shape communicates the loyalty insight better than any alternative.
- **Color hierarchy matters more than color variety.** Two-color systems (blue/orange, black/grey) communicate more clearly than multi-color palettes.
- **KPI design is a business conversation, not a data conversation.** The question is always: "What decision will this metric enable?" — not "What can I calculate?"
- **Tooltip quality reflects dashboard professionalism.** Custom-formatted tooltips with business labels are not optional for portfolio-grade work.

---

## 🔮 Future Improvements

- [ ] **Geographic analysis layer** — Map visual showing sales and customer distribution by region to add spatial intelligence
- [ ] **Customer cohort retention view** — Tracking 2022 customers who returned in 2023 vs. newly acquired, enabling churn and retention measurement
- [ ] **Discount impact analysis** — Correlating discount rate with profit margin per subcategory to quantify the true cost of promotional activity
- [ ] **Forecasting layer** — Using Tableau's built-in forecasting to project Q1/Q2 2024 trajectory based on 2023 trend data
- [ ] **Executive annotation callouts** — Embedding written insight flags directly on dashboard elements to guide non-analytical stakeholders
- [ ] **Mobile-optimized layout** — A device-responsive version for leadership access during meetings and travel

---

## 🖼️ Dashboard Screenshots

### Sales Dashboard | 2023
![Sales Dashboard](screenshots/sales_dashboard_2023.png)

> *Total Sales: $733K | Total Profit: $93K | Total Quantity: 12K | All metrics vs. 2022 prior year*

### Customer Dashboard | 2023
![Customer Dashboard](screenshots/customer_dashboard_2023.png)

> *Total Customers: 693 | Sales Per Customer: $1,058 | Total Orders: 1,687 | All metrics vs. 2022 prior year*

---

## 🧭 How to Use the Dashboard

1. **Open the Tableau workbook** (`.twbx` file) in Tableau Desktop, or access via the Tableau Public link
2. **Start on the Sales Dashboard** for macro business performance
3. **Use the top-right icons** to switch between the Sales and Customer dashboards
4. **Apply filters** (Category, Sub-Category, Region, City) using the filter panel — all charts update simultaneously
5. **Hover on any data point** for custom tooltips with contextual business information
6. **Note the highlighted dots** on sparklines — blue = highest month, orange = lowest month
7. **Use the trend chart reference lines** as benchmarks to classify individual periods as above or below average performance

---

## 📂 Repository Structure

```
📁 tableau-sales-customer-dashboard/
│
├── 📁 workbook/
│   └── Sales_Customer_Dashboard_2023.twbx      # Tableau packaged workbook
│
├── 📁 data/
│   └── superstore_dataset.xlsx                  # Source dataset
│
├── 📁 screenshots/
│   ├── sales_dashboard_2023.png                 # Sales Dashboard screenshot
│   └── customer_dashboard_2023.png              # Customer Dashboard screenshot
│
├── 📁 design/
│   ├── dashboard_mockup.pdf                     # Hand-drawn wireframe mockups
│   └── project_phases.pdf                       # Dashboard design process documentation
│
└── README.md                                    # This file
```

---

## 🏁 Conclusion

This project demonstrates what a business intelligence analyst actually does: not just build charts, but ask the right questions, design the right structure, and deliver a system that helps decision-makers see what they could not see before.

The Sales and Customer dashboards are not data displays — they are analytical arguments. The Sales Dashboard argues that 2023 growth carries a margin efficiency risk that deserves attention. The Customer Dashboard argues that loyalty depth is shallow and concentration risk is real. Both arguments are made visually, clearly, and in a format that a non-technical executive can act on without a data team in the room.

That is the definition of effective business intelligence.

---

*Built as part of the Tableau Ultimate Course — Section 15 Capstone Project | Data With Baraa methodology*

*🔗 LinkedIn: https://www.linkedin.com/in/rohan-bhanushali-234807218/*
