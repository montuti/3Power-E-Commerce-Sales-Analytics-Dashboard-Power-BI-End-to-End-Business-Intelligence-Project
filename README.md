# 📊 PR3 - Brazilian E-Commerce Sales Analytics Dashboard

## 📌 Project Overview

This project analyzes the Brazilian E-Commerce Public Dataset by Olist using Microsoft Power BI. The dashboard transforms raw transactional data into meaningful business insights through interactive visualizations, KPI cards, geographic analysis, payment trends, and customer satisfaction metrics.

The project demonstrates professional data modeling, Power Query transformations, DAX calculations, and dashboard design using a Star Schema architecture.

---

# 📁 Repository Structure

```
PR3-Olist-Ecommerce/
│
├── PR3-Olist-Ecommerce.pbix
│
├── Dataset/
│   ├── olist_orders_dataset.csv
│   ├── olist_order_items_dataset.csv
│   ├── olist_customers_dataset.csv
│   ├── olist_products_dataset.csv
│   ├── olist_sellers_dataset.csv
│   ├── olist_order_payments_dataset.csv
│   ├── olist_order_reviews_dataset.csv
│   ├── olist_geolocation_dataset.csv
│   └── product_category_name_translation.csv
│
├── Screenshots/
│   ├── After-Dataset-PowerQuery.png
│   ├── Before-Rename-Dataset-PowerQuery.png
│   ├── Olist-Ecommerce-Sales-Dashboard.png
│   ├── Geographical-Analysis-Dashboard.png
│   ├── Payment-and-Reviews.png
│   ├── Seller-Performance-Dashboard.png
│   └── Payment-and-Delivery-Dashboard.png
│
└── README.md
```

---

# 📂 Dataset

**Dataset Name**

Brazilian E-Commerce Public Dataset by Olist

**Source**

https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce

The dataset contains 9 CSV files representing customers, orders, products, sellers, payments, reviews, and geographical information.

---

# 🛠 Tools Used

- Microsoft Power BI Desktop
- Power Query
- DAX
- Microsoft Excel
- Kaggle Dataset

---

# ⭐ Data Model

The project follows a Star Schema design.

```
                    DimDate
                       |
                DimOrders
               /    |     \
              /     |      \
     FactPayments FactOrderItems FactReviews
                     /      \
                    /        \
           DimProducts     DimSellers
                    |
              DimCustomers
```

> Replace the above diagram with your actual **Model View Screenshot**.

---

# 🔗 Relationships

| No | From Table | Column | To Table | Column | Cardinality |
|----|------------|--------|----------|--------|-------------|
| 1 | FactOrderItems | order_id | DimOrders | order_id | *:1 |
| 2 | FactOrderItems | product_id | DimProducts | product_id | *:1 |
| 3 | FactOrderItems | seller_id | DimSellers | seller_id | *:1 |
| 4 | DimOrders | customer_id | DimCustomers | customer_id | *:1 |
| 5 | DimDate | Date | DimOrders | Order_Date | 1:* |
| 6 | FactPayments | order_id | DimOrders | order_id | *:1 |
| 7 | FactReviews | order_id | DimOrders | order_id | *:1 |

### Inactive Relationship

DimDate[Date] → DimOrders[order_delivered_customer_date]

Used for delivery date analysis using **USERELATIONSHIP()**.

---

# 📊 Dashboard Pages

## 1️⃣ Executive Sales Dashboard

### Key Insights

- Displays Total Orders, Revenue, Average Order Value, and Customer Rating.
- Tracks monthly order trends to identify business growth and seasonal demand.
- Highlights top-performing product categories and overall sales performance.

---

## 2️⃣ Geographic Analysis

### Key Insights

- Visualizes customer and seller distribution across Brazilian states.
- Identifies the Top 10 seller cities generating the highest revenue.
- Compares revenue contribution by seller state for regional performance analysis.

---

## 3️⃣ Payments & Reviews

### Key Insights

- Analyzes payment methods and their contribution to overall revenue.
- Compares yearly payment trends using an interactive matrix visualization.
- Evaluates customer satisfaction through average review scores by product category.

---

# 🚀 Dashboard Features

- Executive KPI Cards
- Interactive Slicers
- Drill Down Hierarchies
- Geographic Maps
- Matrix Visual
- Bar & Column Charts
- Donut Chart
- Cross Filtering
- Star Schema Model
- Calendar Table (DimDate)
- Product Hierarchy
- Customer Location Hierarchy
- Seller Location Hierarchy

---

# 📷 Screenshots

Include these screenshots inside the **Screenshots** folder.

- After Dataset Power Query
- Before Rename Dataset Power Query
- Executive Sales Dashboard
- Geographic Analysis Dashboard
- Payments & Reviews Dashboard
- Seller Performance Dashboard
- Payment & Delivery Dashboard

---

# ▶️ How to Run

1. Clone or download this repository.
2. Open **PR3-Olist-Ecommerce.pbix** using Power BI Desktop.
3. Keep all CSV files inside the Dataset folder.
4. Refresh the data.
5. Explore all dashboard pages using filters and slicers.

---

# 🎯 Project Objectives

- Design a professional Star Schema model.
- Build fact and dimension relationships.
- Perform ETL using Power Query.
- Create DAX measures and KPIs.
- Develop interactive business dashboards.
- Analyze sales, customers, products, sellers, payments, and reviews.

---

# 📹 Demonstration Video

**Video Link**

Add your YouTube or Google Drive project demonstration link here.

---

# 💼 Skills Demonstrated

- Power BI
- Power Query
- DAX
- Data Modeling
- Star Schema
- Business Intelligence
- Dashboard Design
- Data Visualization
- KPI Development
- Business Analytics

---
Aothor 
name montu mali

## ⭐ If you like this project, please give it a Star.
