# 📊 Superstore Sales Data Analysis & Power BI Implementation

**Digital Egypt Pioneers Initiative (DEPI) — Data Analysis Track Graduation Project**  
**Supervisor:** Eng. Amir Ahmed Shehata

---

## 📌 Project Overview
This end-to-end Business Intelligence project transforms raw historical US Superstore transactional data into an interactive, three-page Power BI executive reporting suite. The solution provides C-level executives and sales managers with real-time visibility into revenue growth, seasonality, customer repeat behavior, regional performance, and product revenue concentration.

---

## 👥 Project Team & Roles
| Team Member | Role | Core Responsibilities |
| :--- | :--- | :--- |
| **Ola Essam Gheta Hussein** | Data Cleaning Specialist | Power Query preprocessing, context-based null handling, duplicate removal, and strict data typing. |
| **Hagar Khaled Mohamed Abdallah** | Data Modeling Specialist | Star Schema design (1 Fact + 4 Dimensions), 1:Many single-direction relationships, role-playing `DimDate`, and key governance. |
| **Aya Refaat Mohamed Elammary** | DAX & Analytics Specialist | Centralized `_Measures` engine covering Time Intelligence (`YoY %`, `YTD`), customer retention, and Pareto concentration (`Top 10%`). |
| **Abdelrahman Gomaa Abdelaziz** | Business Analyst | Framed 11 dashboard-aligned strategic business questions across 4 operational pillars and defined v1 analytical scope boundaries. |
| **Adham Ahmed Nabli** | Dashboard & UX Specialist | Designed **Executive Overview** & **Sales Analysis** pages, KPI layouts, and universal slicer architecture. |
| **Hind Samir Saad** | Dashboard & UX Specialist | Designed **Product Analysis** page, dynamic ranking tables, and cross-filtering navigation flow. |

---

## 🏗️ Data Architecture & Methodology
1. **Data Preparation (Power Query):** Audited raw columns, handled nulls according to field context, purged duplicate sales lines, and enforced explicit data types (`Date`, `Decimal/Currency`, `Whole Number`, `Text`).
2. **Star Schema Modeling:** Normalized flat data into a central `Superstore Sales Dataset` fact table connected via `1:Many` single-direction relationships to `DimDate`, `DimCustomers`, `DimProducts`, and `DimGeography`, using an active link on `Order Date` and an inactive link on `Ship Date`.
3. **DAX Engine (`_Measures`):** Built safe-division (`DIVIDE`) calculations for `Total Sales`, `Sales YoY %`, `Sales YTD`, `Orders Count`, `Unique Customers`, `Avg Orders Value (AOV)`, `Repeat Customer Rate`, `Sales % of Total`, and `Top 10% Revenue Share`.
4. **3-Page Power BI Suite:**
   - **Page 1 — Executive Overview:** High-level KPIs, monthly trend, quarterly YoY comparison, and regional/category splits.
   - **Page 2 — Sales Analysis:** YTD tracking, day-of-week revenue patterns, regional category mix, and customer segment breakdown.
   - **Page 3 — Product Analysis:** Top 10 products bar chart, category comparison, and sortable Product Ranking table.

---

## 💡 Key Findings (2018 & Overall Dataset)
- **Revenue & Growth:** Generated **$722.1K** in 2018 (**+20.3% YoY** after **+30.6%** in 2017), reaching **$2.26M** overall.
- **Seasonality & Weekdays:** Revenue climbs steadily through Q3 to a **Q4 peak** (led by a November surge); **Saturday ($141.9K)** and **Tuesday ($133.2K)** generate the highest weekday sales.
- **Product Concentration (Pareto):** The **top 10% of products** account for **67.0% of 2018 revenue** (**59.2% overall**), led by the *Canon imageCLASS 2200 Advanced Copier* ($35.7K). Technology leads categories at **36.6% ($269.4K)**.
- **Customers & Regions:** **690 unique customers** in 2018 with a **70.7% Repeat Customer Rate** and **$434.71 AOV**. **West ($248.1K)** and **East ($210.1K)** lead regional sales.

---

## 📂 Repository Structure
```text
├── data/            # Raw Superstore transactional dataset (.csv)
├── docs/            # Business questions framework, DAX documentation & cleaning/modeling notes
├── powerbi/         # Power BI report file (.pbix) & dashboard screenshots
├── presentation/    # Final DEPI graduation defense presentation (.pptx & .pdf)
└── README.md        # Project documentation and executive summary