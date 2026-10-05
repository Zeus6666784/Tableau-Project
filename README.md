# Coca-Cola Sales Performance Analysis Dashboard

An interactive sales analytics project built with **Tableau Desktop** using an Excel dataset. The dashboard explores sales performance, operating profit, units sold, beverage brands, geographic regions, states, and retailer performance.

> **Project type:** Data Visualization & Business Intelligence  
> **Tools:** Tableau Desktop, Microsoft Excel  
> **Dataset file:** `excel dashboard- coca cola.xlsx`  
> **Packaged workbook:** `PROJECT.twbx`

---

## Table of Contents

- [Project Overview](#project-overview)
- [Objectives](#objectives)
- [Tools and Technologies](#tools-and-technologies)
- [Dataset](#dataset)
- [Dashboard Worksheets](#dashboard-worksheets)
- [Calculated Fields](#calculated-fields)
- [Key Findings](#key-findings)
- [How to Open the Project](#how-to-open-the-project)
- [Repository Structure](#repository-structure)
- [Limitations and Notes](#limitations-and-notes)
- [Future Improvements](#future-improvements)

---

## Project Overview

This project uses Tableau to turn the supplied Coca-Cola sales dataset into an interactive dashboard. It is designed to help users explore overall sales and profitability, compare beverage brands, examine regional and state performance, track sales over time, and identify leading retailers.

The workbook contains KPI views, comparative charts, geographic analysis, and interactive filters. The findings depend on the data and filters selected in Tableau.

## Objectives

- Summarize total sales, operating profit, and units sold using KPI cards.
- Calculate the operating profit-to-sales ratio.
- Analyze sales over time using invoice dates.
- Compare sales performance across beverage brands.
- Explore sales across regions and states.
- Rank retailers by sales.
- Provide interactive filtering by year, region, and beverage brand.
- Present findings in a clear, consistent dashboard.

## Tools and Technologies

| Tool | Purpose |
|---|---|
| Tableau Desktop / Tableau Public | Build calculated fields, worksheets, filters, and dashboard views |
| Microsoft Excel | Store and provide the source dataset |
| Tableau Packaged Workbook (`.twbx`) | Share the workbook together with packaged data where supported |
| GitHub | Version control and project sharing |

## Dataset

**Source file:** `excel dashboard- coca cola.xlsx`

The workbook's `Data Table1` data source contains **9,648 rows and 12 fields**, as shown in Tableau's Data Source page.

Fields used in the analysis include:

- `Retailer`
- `Retailer ID`
- `Invoice Date`
- `Region`
- `State`
- `City`
- `Beverage Brand`
- `Price per Unit`
- `Units Sold`
- `Total Sales`
- `Operating Profit`
- `Operating Margin`

The dataset spans invoice dates in **2022 and 2023**. Monetary values are shown as dollars in the project analysis; confirm the source dataset's currency definition before treating the values as a verified currency denomination.

## Dashboard Worksheets

| Worksheet / View | Purpose |
|---|---|
| KPI - Total Sales | Displays aggregated total sales |
| KPI - Total Profit | Displays aggregated operating profit |
| KPI - Units Sold | Displays the total units sold |
| KPI - Profit Ratio | Shows operating profit as a proportion of sales |
| Sales Trend | Shows how sales change over invoice dates |
| Sales by Beverage Brand | Compares sales among beverage brands |
| Sales by Region | Compares sales across regions |
| Sales by State | Shows state-level sales where geographic mapping is supported |
| Top Retailers by Sales | Ranks retailers by total sales |
| Interactive Filters | Allows exploration by year, region, and beverage brand |

## Calculated Fields

Create these fields in Tableau using **Data pane → Create Calculated Field**.

### Total Sales KPI

```tableau
SUM([Total Sales])
```

### Total Profit KPI

```tableau
SUM([Operating Profit])
```

### Total Quantity KPI

```tableau
SUM([Units Sold])
```

### Profit Ratio

```tableau
IF SUM([Total Sales]) != 0 THEN
    SUM([Operating Profit]) / SUM([Total Sales])
END
```

Format this field as a percentage. It is an aggregate operating profit-to-sales ratio.

### Average Sales

```tableau
AVG([Total Sales])
```

This is the average value of `Total Sales` per source row, not necessarily average sales per invoice.

### Invoice Year

```tableau
YEAR([Invoice Date])
```

Use this field if a separate year filter is needed.

## Key Findings

The following are summary figures previously calculated from the supplied dataset. Recheck them against the final workbook, particularly if filters or aggregation settings differ.

- **Overall performance:** Approximately **$12.02 million** in total sales, **$4.72 million** in operating profit, and **24.79 million units sold**.
- **Profit ratio:** Approximately **39.30%**, calculated as total operating profit divided by total sales.
- **Beverage brands:** Coca-Cola was reported as the highest-selling brand at approximately **$2.77 million**; Dasani Water followed at approximately **$2.39 million**. Fanta was reported as the lowest-selling brand at approximately **$1.43 million**.
- **Regional performance:** The West region was reported as the highest-selling region at approximately **$3.64 million**. The Midwest was reported as the lowest at approximately **$1.67 million**.
- **Retailers:** West Soda was reported as the highest-selling retailer at approximately **$3.24 million**.
- **Sales by year:** Approximately **$2.42 million** was reported for 2022 and **$9.59 million** for 2023. Confirm that the periods are comparable before describing this difference as year-over-year growth.

## How to Open the Project

1. Download or clone this repository.
2. Open `PROJECT.twbx` in Tableau Desktop or a compatible Tableau application.
3. If prompted, confirm the data connection and refresh the data if needed.
4. Open the dashboard tab to explore the visualizations.
5. Use the year, region, and beverage brand filters to examine different subsets of the data.
6. Save a copy of the workbook if you make changes.

The `.twbx` file is the recommended file to share. The `.twb` file stores the workbook definition and may depend on a separately available data source.

## Repository Structure

A suggested repository layout is:

```text
coca-cola-sales-dashboard/
├── README.md
├── PROJECT.twbx
├── PROJECT.twb
├── excel dashboard- coca cola.xlsx
└── dashboard-screenshot.png
```

Add only files you intend to share. If you publish a screenshot or video, add its path or URL to this README.

## Limitations and Notes

- The dataset has six distinct beverage brands, so it cannot produce a true Top 10 beverage-brand ranking. The project uses **Top Retailers by Sales** as an alternative.
- The source does not include a separate `Category` field. `Beverage Brand` is used for brand-level comparisons and as a practical filter substitute; it should not be described as an original category field.
- State maps depend on Tableau correctly recognizing the geographic locations. If locations are unresolved, use a state-level bar chart or correct the geographic roles.
- Sales values and rankings may change when filters are applied.
- The reported findings should be validated against the final workbook before submission.
- Do not interpret the 2022–2023 difference as a growth rate until the date coverage for both years has been checked.

## Future Improvements

- Add a dedicated category field if a validated source dataset becomes available.
- Use a dataset with at least ten distinct products if a strict Top 10 products chart is required.
- Add a sales-versus-profit comparison and a monthly profit trend.
- Improve tooltips with concise contextual details.
- Publish the dashboard to Tableau Public if permitted, and add the published URL here.
- Add a short demonstration video and link it below.

## Project Links

- **Dashboard screenshot:** `dashboard-screenshot.png` (add after capturing the final dashboard)
- **Demonstration video:** Add your video URL here.
- **Tableau Public:** Add your published dashboard URL here, if applicable.

---

*Created as a Tableau data visualization and dashboarding project using the supplied Coca-Cola sales workbook.*
"# Tableau-Project" 
# Tableau-Project
