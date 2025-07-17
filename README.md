## 🍪 Cookie Sales Report – Power BI Dashboard

#### Project Overview
This Power BI dashboard project provides a concise and interactive overview of cookie sales performance using a simplified dataset consisting of Orders and Customers tables. By implementing effective data modeling, DAX measures, and user-friendly visuals, the report helps stakeholders monitor sales trends, identify top customers, and make data-driven decisions based on clear KPIs.

![Cookie Sales - Power BI Dashboard](https://github.com/user-attachments/assets/8d1cacb1-dd9d-4028-9ddb-36b5e3bdfacc)




### Project Workflow

1. Data Preparation

- Imported two core datasets: Orders and Customers.
- Removed unnecessary columns to simplify the data model and improve performance.
- Ensured data types were consistent and accurate for analysis.

2. Date Table Creation
- To enable proper time intelligence functions and filtering, a dynamic date table was created:


  ```dax
  Dim_Date = 
    CALENDAR(
    DATE(2024, 12, 01), 
    CALCULATE(MAX('Orders'[Order Date]))
    )
  ```


- Established a one-to-many relationship between dim_Date[Date] and Orders[Order Date].


3. DAX Measures

   Created below given essential key measures:


```dax
Total Orders = COUNTROWS(Orders)
Total Sales = SUM(Orders[Revenue])
```


4. Visualizations

- Built an interactive dashboard using the following visuals:
- Line Chart: Visualizes sales trends over time.
- Bar Chart: Compares sales by country
- KPI Cards: Highlights key figures such as Total Sales, Total Orders, and Cookies Shipped.
- Table: Displays Top 20 customers by sales, allowing for easy identification of high-value clients.

#### Enhancements added:

- Zoom sliders for better time-range navigation.
- Data labels for clarity in trend and comparison visuals.

### Outcome / Stakeholder Value

- This dashboard provides a real-time, at-a-glance view of cookie sales performance. Stakeholders such as sales managers, marketing teams can:
- Track overall sales volume and order count instantly.
- Identify top-performing customers to focus retention and upselling efforts.
- Observe sales trends over time, helping with seasonal planning and performance reviews.

✅ The dashboard’s clean layout and interactivity make it ideal for quick reviews and in-depth analysis, empowering stakeholders to make faster and more informed decisions.

**Project files are attached for reference**
