# 📊 Sales Dashboard Analysis

## 📌 Project Overview
This project presents an **interactive Sales Dashboard** built using **Microsoft Power BI**.  
The dashboard provides insights into sales performance, profit analysis, customer behavior, and regional trends using a structured data model and DAX calculations.

The project was developed as part of a **Data Analytics training assignment**, covering the complete Power BI workflow:
- Data loading & cleaning
- Data modeling & relationships
- DAX calculations
- Dashboard design & visualization

---

## 📂 Datasets Used
The analysis is based on **three datasets**:

### 1️⃣ Sales Data
Contains transactional sales information.
- OrderID
- CustomerID
- ProductID
- Order Date
- Sales
- Profit
- Derived fields: Month Name, Month Number

### 2️⃣ Customer Data
Contains customer demographic and location details.
- CustomerID
- CustomerName
- Region
- City

### 3️⃣ Product Data
Contains product-level information.
- ProductID
- Category
- SubCategory
- Price

---

## 🔗 Data Model & Relationships
A **star schema** data model was implemented with the Sales table as the fact table.

### Relationships
- Customer data (CustomerID) → Sales data (CustomerID)  
  - One-to-Many (1:*), Active
- Product data (ProductID) → Sales data (ProductID)  
  - One-to-Many (1:*), Active

These relationships enable dynamic filtering across visuals using slicers for **Region** and **Category**.

---

## 🧮 DAX Measures Used
The following DAX measures were created for analysis:

```DAX
Total Sales = SUM('Sales data'[Sales])

Total Profit = SUM('Sales data'[Profit])

Profit Margin % =
DIVIDE([Total Profit], [Total Sales]) * 100

Total Orders = COUNT('Sales data'[OrderID])

Average Order Value =
DIVIDE([Total Sales], [Total Orders])


---

## 📈 Dashboard Visualizations

The dashboard includes the following visuals:

### 1. KPI Cards
- Total Sales
- Total Profit
- Profit Margin %
- Total Orders

### 2. Bar Chart
- Region-wise Sales

### 3. Donut Chart
- Profit by Category

### 4. Line Chart
- Monthly Sales Trend

### 5. Table
- Top 10 Customers by Sales

### 6. Treemap
- Category-wise Sales Distribution

### 7. Slicers
- Category
- Region

---

## 🚀 Key Insights
- **Technology** category contributes the highest share of sales
- **West** region leads in overall sales performance
- Clear **monthly sales trends** and seasonal patterns are visible
- **High-value customers** identified through Top 10 customer analysis

---

## 👤 Author
**Drishan Vig**

