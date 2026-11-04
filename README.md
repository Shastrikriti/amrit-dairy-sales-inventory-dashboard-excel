# 🥛 Amrit Dairy Farms – Sales & Inventory Dashboard (Excel)

An interactive Excel dashboard that analyses four years (2019–2022) of dairy sales and inventory data: revenue, quantity sold, sales channels, geography, seasonality and stock health.

![Dashboard](assets/dashboard.png)

## Highlights

- **4,325 records**, 10 products, 11 brands, 15 states, 3 sales channels
- **₹58.7M** total revenue and **1.07M** units sold across all brands
- Revenue fell every year, from ₹15.2M (2019) to ₹14.1M (2022), driven by fewer transactions
- **21%** of records are below their minimum stock threshold; Yogurt and Buttermilk are worst
- Delhi and Chandigarh generate about **22%** of revenue; the top 4 brands hold **79%**

## What's inside

| Sheet | Purpose |
|---|---|
| `dairy_dataset` | Cleaned data table plus helper columns (Month, Year, Quarter, Reorder Flag) |
| `Filtered Data` | Rows for the brand selected on the dashboard (VLOOKUP-driven) |
| `Pivots` | 13 PivotTables feeding every chart and KPI card |
| `Dashboard` | KPI cards, 6 charts, Year/Quarter slicers, brand drop-down, Submit/Reset buttons |

## Dashboard features

- KPI cards: Revenue, Quantity Sold, Total Reorder Quantity
- Monthly revenue trend (one line per year), revenue by product, channel share, product × channel mix, top 5 states, stock vs minimum threshold
- Year and Quarter slicers, plus a brand selector with **Submit** and **Reset** macro buttons

## Dataset

`data/Amrit_dataset.csv`: 23 columns covering farm details, product and brand, production and expiry dates, quantity and price, sales channel, customer location, stock level, minimum threshold and reorder quantity. Quality checks found no missing values or duplicates. Revenue, total value and shelf-life columns are internally consistent. Three points to be aware of: 59% of sales are dated after the expiry date, 18 records have zero stock, and farm attributes (cow count, farm size) are not stable within a location. The data appears to be synthetic.

## Key insights

1. **Balanced portfolio:** Curd leads at 11.5% of revenue, Ice Cream is lowest at 9.0%.
2. **Declining trend:** revenue down 7.5% from 2019 to 2022; January is the peak month and April the trough.
3. **Channels:** Retail 35.5%, Wholesale 34.4%, Online 30.1% (lowest order value).
4. **Inventory:** about half of production is sold (49.6% sell-through) while 21% of records are below threshold.
5. **Pricing:** selling prices match list prices within 0.1%.

## Tech

Microsoft Excel · Power Query · PivotTables · Slicers · VBA macros (`.xlsm`)

## How to use

1. Download `AmritDairy_dashboard.xlsm` and open it in desktop Excel.
2. Click **Enable Content** so the Submit and Reset buttons work.
3. Pick a brand in the drop-down and press **Submit**; use the Year and Quarter slicers to narrow the period; press **Reset** to clear.

> Macros do not run in Excel for the web or in Protected View.

## Documentation

Full report: [`Amrit_Dairy_Project_Report.pdf`](Amrit_Dairy_Project_Report.pdf), covering introduction, dataset, cleaning, visualizations, insights and conclusions.

## Repository structure

```
├── AmritDairy_dashboard.xlsm
├── Amrit_Dairy_Project_Report.pdf
├── README.md
├── data/
│   └── Amrit_dataset.csv
└── assets/
    └── dashboard.png
```

## Author

[Kriti Shastri] · [https://github.com/Shastrikriti]
