# 🍕 Pizza Sales Analysis

This project showcases my ability to work with raw data using SQL and Excel. It began with a CSV file, which was uploaded to SQL Server for querying. From there, I exported the insights to Excel where I used pivot tables and pivot charts to create a professional, interactive dashboard.

The goals of this project were:
- ✅ Demonstrate proficiency in writing SQL queries for business insight extraction.
- ✅ Showcase the ability to transform and visualize data using Excel dashboards.

---

## 🛠️ Tools Used

- **SQL Server 2022**
- **SQL Server Management Studio (SSMS)**
- **Microsoft Excel**
- **Data Source**: Sample pizza sales dataset (accessed via YouTube tutorial)

---

## 📂 Project Workflow

1. **Data Upload**: The original `.csv` file was uploaded into SQL Server as a table.
2. **Querying in SQL**: I wrote SQL queries to extract business metrics and answer key sales questions.
3. **Data Export**: Queried results were exported to Excel.
4. **Transformation in Excel**: Pivot tables were created for each metric.
5. **Visualization**: A dashboard was built using pivot charts and slicers for dynamic filtering.

---

## 🔍 Key Metrics & Questions Answered

### Using SQL Queries

- **Total Revenue**

  SELECT SUM(total_price) AS Total_Revenue from pizza_sales
  
  <img width="229" height="88" alt="image" src="https://github.com/user-attachments/assets/0e182ecc-4b20-46fc-9746-9a1d32279adb" />

- **Average Order Value**  
- **Total Pizzas Sold**  
- **Total Orders**  
- **Average Pizzas per Order**

   SELECT CAST(CAST(SUM(quantity) AS DECIMAL(10,2))/CAST(COUNT(DISTINCT order_ID) AS DECIMAL(10,2)) AS DECIMAL(10,2)) AS Avg_Pizzas_Per_Order FROM pizza_sales

  <img width="233" height="94" alt="image" src="https://github.com/user-attachments/assets/502b6f3d-2f25-43c6-96e6-5b5fe45fb51b" />

- **Daily Trend for Total Orders**  
- **Hourly Trend for Total Orders**  
- **% of Sales by Pizza Category**

  SELECT pizza_category, CAST(SUM(total_price) AS DECIMAL(10,2)) AS Total_Sales, CAST(SUM(total_price) * 100 / (SELECT SUM(total_price) FROM pizza_sales) 
AS DECIMAL(10,2)) AS Percentage_Total_Sales
FROM pizza_sales
GROUP BY pizza_category

<img width="466" height="160" alt="image" src="https://github.com/user-attachments/assets/36f957dc-1933-4b4e-914b-b9d704cfaab4" />

- **% of Sales by Pizza Size**  
- **Total Pizzas Sold by Pizza Category**  
- **Top 5 Bestsellers**

  SELECT Top 5 pizza_name, SUM(quantity) AS Total_Pizza_Sold
FROM pizza_sales
GROUP BY pizza_name
ORDER BY Total_Pizza_Sold DESC

<img width="414" height="194" alt="image" src="https://github.com/user-attachments/assets/7361ed5f-7fb9-457f-bc89-40f3b68765d3" />

 
- **Bottom 5 Sellers**


---

## 📊 Excel Dashboard

After exporting the results to Excel, I created multiple pivot tables and charts to visualize the data. These visuals were compiled into a comprehensive dashboard with slicers for interactivity.

📸 *Sample Pivot Tables and Pivot Charts:*  

<img width="1369" height="436" alt="image" src="https://github.com/user-attachments/assets/39467d9c-5590-4948-b07c-8751f840627b" />

📸 *Full Dashboard Screenshot:*  

<img width="1252" height="624" alt="image" src="https://github.com/user-attachments/assets/5fb236a2-bd4b-4850-8d0f-5586e1df04e8" />

---

## 💡 Key Insights from the Dashboard

- **Sales peak on Friday and Saturday evenings**, with the **busiest hour between 12–1 PM**.
- **Classic category and large-sized pizzas contribute most to total revenue.**
- **Top sellers** include Classic and Barbecue Chicken pizzas.
- **Bottom sellers** include Mediterranean and Brie Carre pizzas.

---

## 🚀 What I Learned

- How to structure SQL queries for business intelligence reporting.
- How to connect SQL insights into Excel for further analysis.
- How to use pivot tables and slicers for building dynamic dashboards.
- Reinforced best practices for data storytelling with limited tools.

---

