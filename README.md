# 📊 Pizza Sales Analytics Dashboard (SQL + Excel)

An end-to-end analysis of pizza sales data using SQL Server and Excel to identify revenue drivers, customer ordering patterns, and product performance.

---

## 🚀 Business Problem

Food service and retail teams need visibility into:

- revenue and order volume trends  
- peak sales periods  
- top-performing and underperforming products  
- category and size contribution to overall sales  

This analysis consolidates transactional data into actionable insights to support inventory planning, staffing, and product strategy.

---

## 📌 Key Insights

- **Peak demand:** Friday and Saturday evenings, with highest order volume between 12–1 PM  
- **Revenue drivers:** Classic category and large-sized pizzas contribute the largest share of sales  
- **Top-performing products:** Classic and Barbecue Chicken pizzas lead in total sales volume  
- **Underperforming products:** Mediterranean and Brie Carre pizzas show consistently low demand

---

## 📈 Analytical Capabilities

- Revenue and order volume tracking  
- Time-based trend analysis (daily and hourly patterns)  
- Product performance:
  - category-level contribution  
  - size distribution  
  - top and bottom sellers  
- Average order behavior:
  - average order value  
  - average pizzas per order

---

## 🧠 Analytical Approach

- Ingested raw CSV data into SQL Server for structured querying  
- Developed SQL queries to calculate key business metrics, including:
  - total revenue  
  - average order value  
  - sales distribution by category and size  
  - top and bottom performing products  

- Exported aggregated results to Excel for reporting  
- Built an interactive dashboard using:
  - PivotTables and PivotCharts  
  - slicers for dynamic filtering
 
---

## 📊 Dataset

- Transactional pizza sales dataset  
- Includes order details, product types, quantities, pricing, and timestamps

---

## 🎯 Business Impact

This analysis enables:

- identification of peak demand periods for staffing and operations planning  
- optimization of product offerings based on performance  
- improved inventory planning using category and size demand trends  
- visibility into customer ordering behavior  

---

## ⚙️ Tools & Technologies

- SQL Server  
- SQL  
- Microsoft Excel (PivotTables, PivotCharts, slicers)  

---

## 👤 Role

**Data Analyst**  
- Performed data ingestion, querying, and transformation in SQL  
- Translated query outputs into a structured Excel dashboard  
- Delivered a reporting tool to support operational decision-making  

---

## 🖼️ Dashboard Preview

<img width="1252" height="624" alt="image" src="https://github.com/user-attachments/assets/5fb236a2-bd4b-4850-8d0f-5586e1df04e8" />

---

## 📄 Sample SQL Queries

```sql
SELECT SUM(total_price) AS total_revenue
FROM pizza_sales;

SELECT pizza_category,
       SUM(total_price) AS total_sales,
       SUM(total_price) * 100.0 / (SELECT SUM(total_price) FROM pizza_sales) AS percentage_total_sales
FROM pizza_sales
GROUP BY pizza_category;

SELECT TOP 5 pizza_name,
       SUM(quantity) AS total_pizza_sold
FROM pizza_sales
GROUP BY pizza_name
ORDER BY total_pizza_sold DESC;
```
---

## 🔗 Contact

**Sandra Igboanugo**  
[LinkedIn Profile](https://www.linkedin.com/in/sandraigboanugo/)
