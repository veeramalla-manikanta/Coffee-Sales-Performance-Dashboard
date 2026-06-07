# ☕ Coffee Sales Performance Dashboard

## 📌 Overview

The **Coffee Sales Performance Dashboard** is an interactive Power BI project designed to analyze and visualize sales performance for a coffee shop chain. The dashboard provides insights into sales trends, customer purchasing behavior, product performance, and store-wise revenue generation.

Using Power BI, SQL, and DAX, this dashboard transforms raw transactional data into actionable business insights, helping stakeholders make data-driven decisions to improve sales and operational efficiency.

---

## 🚀 Features

* Interactive KPI tracking for business performance
* Month-wise sales analysis with dynamic filtering
* Product category and product type performance evaluation
* Store location comparison and trend analysis
* Weekday vs Weekend sales analysis
* Daily sales trend visualization
* Hourly and daily sales heatmap analysis
* Month-over-Month (MoM) performance comparison
* User-friendly and interactive dashboard design

---

## 📊 Dashboard KPIs

### Total Sales

Measures total revenue generated during the selected period.

```DAX
Total Sales = SUM(Transactions[Sales])
```

### Total Orders

Calculates the total number of unique customer orders.

```DAX
Total Orders =
DISTINCTCOUNT(Transactions[transaction_id])
```

### Total Quantity Sold

Measures total units sold.

```DAX
Total Quantity Sold =
SUM(Transactions[transaction_qty])
```

### Average Daily Sales

```DAX
Average Sales =
AVERAGEX(
    ALLSELECTED(Transactions[transaction_date]),
    [Total Sales]
)
```

### Previous Month Sales

```DAX
Previous Month Sales =
CALCULATE(
    [Current Month Sales],
    DATEADD('Date Table'[Date], -1, MONTH)
)
```

### Previous Month Orders

```DAX
Previous Month Orders =
CALCULATE(
    [Current Month Orders],
    DATEADD('Date Table'[Date], -1, MONTH)
)
```

### Previous Month Quantity Sold

```DAX
Previous Month Quantity Sold =
CALCULATE(
    [Current Month Quantity Sold],
    DATEADD('Date Table'[Date], -1, MONTH)
)
```

---

## 📂 Dataset Information

The dashboard uses transactional sales data with the following fields:

| Column Name      | Description                   |
| ---------------- | ----------------------------- |
| transaction_id   | Unique transaction identifier |
| transaction_date | Date of purchase              |
| transaction_time | Time of purchase              |
| transaction_qty  | Quantity sold                 |
| store_id         | Unique store identifier       |
| store_location   | Store location                |
| product_id       | Unique product identifier     |
| unit_price       | Price per unit                |
| product_category | Product category              |
| product_type     | Product type                  |
| product_detail   | Product details               |

---

## 🛠️ Tools & Technologies

* **Power BI Desktop**
* **Microsoft Excel / CSV**
* **SQL**
* **DAX (Data Analysis Expressions)**
* **Data Modeling**
* **Data Visualization**

---

## 📈 Dashboard Components

### 1. Month Filter

Allows users to select a specific month for analysis.

### 2. KPI Cards

Displays:

* Total Sales
* Total Orders
* Total Quantity Sold
* Month-over-Month Growth Metrics

### 3. Sales Trend Analysis

Line chart showing daily sales trends and average sales performance.

### 4. Weekday vs Weekend Sales

Donut chart highlighting sales contribution by weekdays and weekends.

### 5. Product Category Analysis

Comparison of sales across categories such as:

* Coffee
* Tea
* Bakery
* Drinking Chocolate
* Flavours

### 6. Product Type Analysis

Detailed analysis of individual product types contributing to revenue.

### 7. Store Location Performance

Sales comparison across different store locations with growth analysis.

### 8. Sales Heatmap

Visualizes customer purchasing behavior by:

* Day of Week
* Hour of Day

---

## 📷 Dashboard Preview

### Executive Dashboard

* Total Sales Performance
* Order Analysis
* Quantity Sold Metrics
* Sales Trend Visualization
* Product Performance Analysis
* Store Performance Comparison

(Add dashboard screenshots here)

---

## ⚙️ Installation

### Clone Repository

```bash
git clone https://github.com/veeramalla-manikanta/Coffee-Sales-Performance-dashboard.git
```

### Open Power BI File

Open:

```text
CoffeeSalesPerformanceDashboard.pbix
```

using Power BI Desktop.

### Import Dataset

1. Home → Get Data
2. Select CSV/Excel source
3. Load dataset
4. Map fields with existing data model
5. Refresh dashboard

---

## ▶️ Usage

1. Open the dashboard in Power BI Desktop.
2. Select a month using the filter.
3. Analyze KPIs and sales trends.
4. Explore product and store performance.
5. Publish to Power BI Service for sharing.
6. Export reports as PDF or PowerPoint.

---

## 📊 Business Insights Generated

* Identified top-performing products and categories.
* Analyzed peak sales hours and customer traffic patterns.
* Compared store performance across locations.
* Evaluated Month-over-Month growth trends.
* Enabled data-driven decision-making for inventory and staffing.

---

## 🎯 Project Outcome

The Coffee Shop Sales Analysis Dashboard provides a comprehensive view of business performance, helping stakeholders monitor revenue, understand customer behavior, optimize inventory planning, and improve operational efficiency through data-driven insights.

---

## 👨‍💻 Author

**Manikanta Veeramalla**

* Power BI Developer
* Data Analyst
* SQL & Business Intelligence Enthusiast
---

## ⭐ If you found this project useful, please consider giving it a star on GitHub!
