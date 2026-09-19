# Power BI Sales Performance Dashboard

## 📊 Project Overview

This project is an interactive **Sales Performance Dashboard** created using **Microsoft Power BI**.

The dashboard analyzes sales performance across products, regions, categories, and months. It demonstrates data preparation, data modeling, DAX measures, data visualization, and interactive filtering.

## 🛠️ Tools & Technologies

- Microsoft Power BI
- Power Query
- DAX
- Data Modeling
- Star Schema

## 🗂️ Data Model

The project uses a **Star Schema** consisting of one fact table and three dimension tables.

### Fact Table

**FactSales**

- Order ID
- Order Date
- Product ID
- Customer ID
- Region
- Sales
- Quantity

### Dimension Tables

**DimProduct**
- Product ID
- Product
- Category

**DimCustomer**
- Customer ID
- Customer Name
- City

**DimDate**
- Date
- Year
- Month Number
- Month Name
- Quarter

## 🔗 Relationships

The following relationships were created:

- DimProduct → FactSales
- DimCustomer → FactSales
- DimDate → FactSales

All relationships use **One-to-Many (1:*)** cardinality with **Single** filter direction.

## 🧮 DAX Measures
### Total Sales

```DAX
Total Sales = SUM(FactSales[Sales])
Total Quantity = SUM(FactSales[Quantity])
Average Sales = AVERAGE(FactSales[Sales])

## Author
RESHMA
