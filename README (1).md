# BMW Sales Dashboard (2010-2024) | Power BI

An interactive 3-page Power BI dashboard analysing **50,000 BMW sales records** across
**15 years, 6 regions, 11 models and 4 fuel types**. It tracks sales volume, revenue and
product mix, with slicers for Year, Region, Model, Fuel Type and Transmission.

![Overview](screenshots/page1_overview.png)

## Business Questions Answered
- How have total sales and revenue moved from 2010 to 2024?
- Which regions and models contribute the most volume and revenue?
- How is sales split across fuel type, transmission and color?
- How are sales classified into High and Low volume?

## Dataset
| | |
|---|---|
| Source | BMW sales data (2010-2024), public dataset (add the link where you downloaded it) |
| Size | 50,000 rows x 11 columns |
| Period | 2010 - 2024 |
| Quality | No missing values, no duplicates |

Column details: [`docs/data_dictionary.md`](docs/data_dictionary.md)

## Tools & Skills
- **Power BI Desktop**: data modelling, visuals, slicers, cards
- **Power Query**: CSV import, type conversion
- **DAX**: `SUMX` revenue measure and supporting measures ([`docs/dax_measures.md`](docs/dax_measures.md))

## Dashboard Pages

### 1. Overview
KPI cards (Total Sales, Total Revenue, Sales Volume), sales trend by year, sales by region.
![Page 1](screenshots/page1_overview.png)

### 2. Sales Mix
Sales by model, sales classification (High/Low), transmission split, fuel type, and a revenue ribbon chart by year.
![Page 2](screenshots/page2_sales_mix.png)

### 3. Revenue Analysis
Revenue by model and region, sales by color, average price trend by year.
![Page 3](screenshots/page3_revenue_analysis.png)

## Key Insights
| Metric | Result |
|---|---|
| Total units sold | **~253.4 million** |
| Total revenue | **~$19.0 trillion** |
| Average unit price | **~$75,035** |
| Peak sales year | **2022** (~17.9M units, ~$1.34T revenue) |
| Lowest sales year | **2023** (~16.3M units) |
| Top model by revenue | **7 Series** (~$1.79T, ~9.4% of revenue) |
| Top region by revenue | **Asia** (~$3.25T, ~17.1%) |
| Top fuel type | **Hybrid** (~64.5M units, ~25.5% share) |

**Takeaways**
1. **Sales are very evenly distributed.** All 6 regions sit between 16% and 17% of volume, all 11 models between 8.8% and 9.4%, and fuel types and transmissions are each close to an equal split. No segment dominates.
2. **2022 was the peak, 2023 the dip.** Volume fell about 9% from 2022 to 2023, then recovered about 8% in 2024.
3. **Hybrid leads narrowly** on volume, with Petrol, Electric and Diesel all within about one percentage point (24.6% - 25.5%).
4. **Average price is flat at about $75K every year**, so revenue growth is driven by volume, not pricing.
5. Because the spread is so uniform, the dataset looks synthetic, which suits a portfolio project but should not be read as real BMW market data.

## How to Use
1. Clone the repo: `git clone https://github.com/sahilparasar/BMW-Sales-Dashboard-PowerBI.git`
2. Open `BMW_Sales_Dashboard.pbix` in **Power BI Desktop**.
3. If prompted, update the data source: *Home > Transform data > Data source settings* and point it to `data/BMW sales data (2010-2024).csv`.
4. Refresh and explore using the slicers.

## Repository Structure
```
├── BMW_Sales_Dashboard.pbix
├── data/                # source CSV
├── docs/                # data dictionary, DAX measures, PDF export
├── screenshots/         # dashboard page images
└── README.md
```

## Future Improvements
- Replace sum-based cards with averages (price, mileage, engine size)
- Add a Date table and Year-over-Year growth measures
- Add drill-through from region to model
- Publish to Power BI Service and link the live report

## Author
**Sahil Bhardwaj**
---
*Independent analysis for learning and portfolio purposes. Not affiliated with or endorsed by BMW AG.*
