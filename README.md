# Cyclistic-BI-Project

### Business Intelligence Project

---

## Project Overview

Cyclistic is a fictional bike-share company operating across New York City. This Business Intelligence project was developed for Cyclistic's **Customer Growth Team** to support their annual business planning process.

The core objective is to understand **how customers use Cyclistic bikes** and identify **demand patterns across station locations** — so leadership can make data-driven decisions about where to grow their station network.

Using **BigQuery (SQL)** for data engineering and **Tableau** for visualization, this project consolidates millions of trip records into an interactive dashboard that surfaces trends by location, time, season, and weather.

---

## 📊 Interactive Tableau Dashboard

**[▶ Click here to view the Live Cyclistic Dashboard](https://public.tableau.com/app/profile/sharat.r6013/viz/Cyclistic_FinalProject/Cyclistic)**

---

## Business Questions Answered

- How are customers currently using Cyclistic bikes?
- Which station locations experience the highest demand?
- How does usage vary by time of day, season, and weather?
- What is the year-over-year growth in trip volume?
- How do subscriber vs. non-subscriber usage patterns differ?
- Which destinations attract the longest trips (by total minutes)?

---

## Technical Workflow

### 1. Requirement Gathering
Collaborated with stakeholders including the VP of Marketing, VP of Product Development, and the Director of Customer Data to define KPIs and dashboard requirements. The primary goal was to surface insights that inform **new station growth decisions**.

### 2. Data Engineering (BigQuery)

**Primary Dataset:** NYC Citi Bike Trips (public)  
**Secondary Dataset:** Census Bureau US Boundaries (for zip code, neighborhood, and borough mapping)

Two SQL queries were executed in BigQuery to prepare the data:

- **Full-Year Summary:** JOINs the NYC Citi Bike Trips dataset with the zip code table to produce a consolidated target table covering all of 2019–2020.
- **Summer Season Summary:** Same JOIN with an added filter for June–September to isolate peak-season trends.

Both scripts are available in the `SQL/` folder.

### 3. Data Visualization (Tableau)

Connected Tableau to the consolidated BigQuery target tables and built a **three-tab interactive dashboard**:

| Tab | Title | Purpose |
|-----|-------|---------|
| 1 | **Summer Trends** | Map of seasonal trip trends across NYC boroughs (July–September focus) |
| 2 | **Seasonality** | Trip totals and trip counts by starting neighborhood across 2019–2020 |
| 3 | **Top Trips** | Comparison of total trip minutes by starting and ending neighborhood |

### 4. Executive Reporting
Findings were synthesized into a PowerPoint presentation with actionable recommendations for the Customer Growth Team.

---

## Key Business Insights

- **Peak Season:** May–October accounts for the majority of trips; usage drops sharply in colder months.
- **Top Neighborhoods:** The **Lower East Side** and **Chelsea & Clinton** are the most active stations for both starting and ending trips.
- **Subscriber Dominance:** Subscribers make up a significantly larger share of users than one-time customers year-round.
- **Weather Impact:** Trip volume is lower on days with precipitation, confirming that weather meaningfully affects demand.
- **Summer Surge:** July, August, and September are the three highest-traffic months — key for station capacity planning.
- **Congestion Signals:** Net analysis of bikes arriving vs. departing per station reveals which locations consistently run low on available bikes.

---

## 📂 Repository Structure

```
├── Data/                   # Raw and processed trip data (CSV)
├── Documents/              # Project planning and requirements
│   ├── Stakeholder_Requirements_Document.docx
│   ├── Project_Requirements_Document.docx
│   └── Strategy_Document.docx
├── Presentation/           # Executive summary for stakeholders
│   └── Cyclistic_Final.pptx
├── SQL/                    # BigQuery ETL scripts
│   ├── full_year_summary.sql
│   └── summer_season_summary.sql
└── README.md               # Project overview (this file)
```

---

## Tech Stack

| Tool | Purpose |
|------|---------|
| Google BigQuery | SQL-based data engineering and JOIN operations |
| Tableau Public | Interactive dashboard and data visualization |
| Google Sheets / CSV | Raw data staging |
| PowerPoint | Executive stakeholder presentation |

---

## Project Metadata

| Field | Detail |
|-------|--------|
| BI Analyst | Sharath Rao |
| Client / Sponsor | Jamal Harris, Director, Customer Data |
| Dashboard Deadline | 6 weeks |
| Primary Dataset | NYC Citi Bike Trips |
| Secondary Dataset | Census Bureau US Boundaries |
| Visualization Tool | Tableau Public |
