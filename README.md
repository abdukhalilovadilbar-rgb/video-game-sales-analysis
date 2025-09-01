# Video Game Sales Analysis

## 📊 Project Overview
This project analyzes a dataset of over 16,000 video games to uncover insights on sales trends, popular genres, and top-performing platforms and publishers. The workflow demonstrates a full data analysis pipeline: from SQL data extraction to Excel visualization.

## 🛠️ Tools & Technologies
- **SQL** (SQLite): Data extraction, aggregation, and analysis.
- **Excel:** Data visualization and dashboard creation.
- **Git/GitHub:** Version control and project hosting.

## 📁 Project Structure
video_game_sales_analysis/
├── data/ # Raw data file (vgsales.csv)
├── sql/ # SQL script with queries
├── outputs/ # Exported results from SQL queries (CSV)
├── visuals/ # Excel dashboard
└── README.md # Project documentation (this file)

## 🔍 SQL Analysis
Key questions explored through SQL queries:

1.  **Top Selling Games:** What are the top 10 best-selling games of all time?
2.  **Sales by Platform:** Which console platform has the highest total sales?
3.  **Genre Popularity:** How many games were released in each genre?
4.  **Publisher Performance:** Who are the top 5 publishers by total global sales?
5.  **Regional Differences:** For the shooter genre, what percentage of total sales came from each region?

### Example Query: Top Publishers
```sql
SELECT Publisher, ROUND(SUM(Global_Sales), 2) as Total_Sales
FROM vgsales
GROUP BY Publisher
ORDER BY Total_Sales DESC
LIMIT 5;