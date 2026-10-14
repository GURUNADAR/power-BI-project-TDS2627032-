# power-BI-project-TDS2627032-
Interactive Power BI dashboard analyzing electronic sales, product performance, monthly trends, and city-wise sales using data visualization and KPI metrics.
# Electronic Sales Dashboard | Power BI

## Project Overview
The **Electronic Sales Dashboard** is an interactive business-intelligence report built in Microsoft Power BI using electronic-sales transaction data. It presents sales performance through KPI cards, time-based charts, product comparisons, a city map, and interactive filters.

The goal is to turn transaction-level data into a clear overview that can help users explore sales value, quantity sold, product contribution, and geographic distribution.

## Objectives
- Monitor total sales and quantity ordered.
- Compare sales across electronic products.
- Explore monthly and quarterly sales patterns.
- Review sales distribution by city.
- Filter the report by city, month, and product.
- Identify products and locations that contribute more to sales.

## Dataset
The project uses `data.csv`, containing order-level and product-level sales information.

| Column | Description |
|---|---|
| `Order ID` | Order identifier |
| `Product` | Electronic product name |
| `Quantity Ordered` | Number of units ordered |
| `Price Each` | Price per unit |
| `Order Date` | Date and time of the order |
| `Purchase Address` | Purchase address recorded in the source |
| `Month` | Numeric month field |
| `Sales` | Sales value for the row |
| `City` | City associated with the purchase |
| `Hour` | Hour of the day |
| `Unnamed: 0` | Index-like column from the source export |

### Data Summary
After excluding one incomplete row, the supplied dataset contains:
- **17,097 valid rows**
- **19 distinct products**
- **9 distinct city labels**
- **16,419 distinct order IDs**
- **Total sales:** 3,158,134.51
- **Total quantity ordered:** 19,272 units

These totals are calculated from the supplied CSV and may differ if the report uses different filters, data-cleaning steps, or measure definitions.

## Dashboard Components
| Visual / Control | Purpose |
|---|---|
| **Total Sales KPI** | Displays aggregate sales value. |
| **Total Quantity KPI** | Displays the total number of units ordered. |
| **Profit Margin KPI** | Displays a margin measure defined in the Power BI model; its exact formula should be documented and verified. |
| **Monthly Sales Trend** | Shows sales across the available months. |
| **Quantity by Product** | Compares units ordered for each product. |
| **Sales by City Map** | Shows geographic distribution of sales. |
| **Sales by Product Treemap** | Compares product contributions to sales. |
| **Sales by Quarter** | Compares sales by quarter in the available data. |
| **City Slicer** | Filters the report by city. |
| **Month Slicer** | Filters the report by month. |
| **Product Slicer** | Filters the report by product. |

## Sample Findings
Based on the supplied CSV:
- **Macbook Pro Laptop** has the highest sales value among the listed products.
- **AAA Batteries (4-pack)** has the highest quantity ordered.
- **San Francisco** has the highest city sales total in this dataset.
- Sales value and quantity are different measures: higher-priced products can contribute more revenue even when they sell fewer units.

The dataset spans **December 2019 to the beginning of January 2020**, so it is too limited to support broad conclusions about full-year seasonality or long-term trends.

## Tools and Technologies
- **Microsoft Power BI Desktop** — dashboard design and visualization
- **CSV** — source dataset
- **Power Query** — data cleaning and transformation, if applied
- **DAX** — measures and calculations used in the report, if applicable

## How to Open the Project
1. Download or clone this repository.
2. Open `ESalesDashboard.pbix` in Microsoft Power BI Desktop.
3. If Power BI asks for the source file, point it to `data.csv` in the repository.
4. Refresh the data if required.
5. Use the city, month, and product slicers to interact with the dashboard.

## Suggested Repository Structure
```text
electronic-sales-dashboard/
├── README.md
├── ESalesDashboard.pbix
├── data.csv
└── screenshots/
    └── dashboard-overview.png
```

## Data Preparation and Limitations
- The CSV includes one incomplete row; check missing values before analysis.
- The city field contains leading whitespace in some raw values, so trimming and standardizing text is recommended.
- The `Unnamed: 0` column appears to be an index-like field and may not be needed for analysis.
- Repeated order IDs can be valid because one order may contain multiple product rows.
- The CSV does not include a direct `Profit` or `Profit Margin` column. Confirm the DAX definition and underlying assumptions before interpreting the Profit Margin KPI as actual profitability.
- The dataset covers only a short period around the end of 2019 and beginning of 2020.

## Future Improvements
- Add more months of data for stronger trend analysis.
- Document the DAX formula for Profit Margin.
- Add average order value, product sales share, and sales growth measures where supported by the data.
- Improve data cleaning and standardize city names.
- Add drill-through pages for detailed product or city analysis.
- Include a clear report title, currency/unit labels, and date coverage on the dashboard.

## Project Report
A separate Word document, **Electronic Sales Dashboard – Project Description**, provides a fuller explanation of the project, dataset, visuals, findings, limitations, and recommendations. Add that document to the repository if you want to include it with the project files.

## Author
**Jayaguru Nadar**  
B.Sc. Data Science Student

## License
This repository is shared for educational and portfolio purposes. Check the original dataset's license and usage terms before redistributing the data.
