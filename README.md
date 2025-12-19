# -Coffee-Shop-Sales-Analysis-Power-BI-2023-
This project analyzes transaction-level sales data of a Coffee Shop for the year 2023 using Power BI. The dashboard focuses on sales performance, order volume, product demand, store comparison, and time-based sales behavior to support data-driven business decisions.
🗂 Dataset Description

Data Granularity: One row per transaction
Time Period: January 2023 – December 2023

Key Columns:

transaction_id

transaction_date

transaction_time

transaction_qty

store_id, store_location

product_id

unit_price

product_category

product_type

product_detail

📌 Sales Value Calculation:

Gross Sales = unit_price × transaction_qty

🎯 Business Objectives

Track overall sales performance in 2023

Analyze Month-over-Month (MoM) growth

Identify top performing stores and products

Understand weekday vs weekend sales behavior

Discover peak sales hours for operational planning

📊 Key KPIs

Total Sales

Total Orders

Total Quantity Sold

MTD Sales vs Previous MTD

MoM Growth %

📈 Dashboard Features

✔ Month & Year slicer
✔ KPI cards with MoM comparison
✔ Sales trend with average reference line
✔ Store-wise sales comparison
✔ Product category contribution
✔ Top 10 products by sales
✔ Weekday vs weekend analysis
✔ Hour-wise sales heatmap

🧠 Key Business Insights

Weekend sales contribute significantly higher revenue compared to weekdays

Certain stores consistently perform above the overall average

Coffee products generate the highest share of total revenue

Sales peak during specific morning and afternoon hours

MoM analysis highlights growth and decline patterns across months

🛠 Tools & Technologies

Power BI Desktop

DAX (Measures & Calculated Columns)

Power Query

Date Dimension Table

📐 DAX Measures Used (Highlights)
Total_Sales =
SUM('Coffee Shop Sales_csv'[Gross_Sale])

Total_orders =
DISTINCTCOUNT('Coffee Shop Sales_csv'[transaction_id])

total_qty_sold =
SUM('Coffee Shop Sales_csv'[transaction_qty])

MTD_Sales =
TOTALMTD(
    [Total_Sales],
    Date_table[Date]
)

P_MTD_Sale =
CALCULATE(
    [MTD_Sales],
    DATEADD(Date_table[Date], -1, MONTH)
)

MoM_Growth =
DIVIDE(
    [MTD_Sales] - [P_MTD_Sale],
    [P_MTD_Sale],
    0
)

🗓 Date Table Logic

Year, Month, Month Name

Week Number & Day Name

Quarter Calculation

Weekday vs Weekend Classification

Month-Year formatting for slicers

📁 Project Structure
Coffee-Shop-Sales-Analysis-PowerBI/
│
├── Data/
│   └── Coffee_Shop_Sales.csv
│
├── PowerBI/
│   └── Coffee_Shop_Sales_Analysis.pbix
│
├── DAX/
│   └── Measures_and_DAX_Used.xlsx
│
├── Dashboard/
│   ├── Dashboard_Screenshot.png
│   └── Coffee_Shop_Monthwise_Sales_Analysis.pdf
│
├── README.md

📌 Conclusion

This project demonstrates practical use of Power BI, DAX time intelligence, and business analytics to convert raw transactional data into actionable insights for sales and operations teams.

🔗 Connect with Me

LinkedIn: https://www.linkedin.com/in/akshath-shetty-updatedprofile/

⭐ If you find this project useful, feel free to star the repository!
