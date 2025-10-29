# SuperMart Sales Performance Analysis Dashboard

## 📊 Project Overview

This interactive sales performance dashboard provides comprehensive insights into SuperMart's business operations for the year 2023-2025. The dashboard enables stakeholders to monitor key performance indicators, identify best-selling products, analyze sales trends, and understand customer demographics across different store locations.

![Sales Performance Dahboard For the Year 2025](/Visuals/SuperMart%20Sales%20Analysis%20Dashboard.png)
*Sales performance dashboard for the year 2025. [Click here](/SuperMart%20Sales%20Dashboard/SuperMart%20Sales%20Dashboard.pbix) to go to Dashboard 🔍.*
## 🎯 Business Questions Answered

This dashboard was designed to address the following critical business questions:

### 1. **Overall Business Performance**
   - What are the total sales and profit figures for the selected store and time period?
   - How many products are currently listed in our inventory?
   - What is the total sales volume (number of transactions)?

### 2. **Product Performance Analysis**
   - Which products are generating the highest sales revenue?
   - What is the sales distribution across different product categories?
   - Which product categories should we focus on for maximum profitability?

### 3. **Sales Trend Analysis**
   - How have sales performed month-over-month throughout the year?
   - Are there any seasonal patterns or trends in our sales data?
   - When do we experience peak sales periods?

### 4. **Customer Demographics**
   - What is the gender distribution of our customer base?
   - Are there any significant differences in purchasing patterns between male and female customers?

### 5. **Customer Segmentation**
   - Which age groups are our primary customers?
   - How do different age demographics contribute to overall sales?
   - Which age segments should we target for marketing campaigns?

### 6. **Category Performance**
   - What percentage of sales comes from Fashion, Electronics, and Groceries?
   - Which category has the highest revenue contribution?
   - How balanced is our revenue stream across categories?

## 📈 Dashboard Components

### Key Metrics Cards
- **Total Sales**: $952.12K - Overall revenue generated
- **Total Profit**: $253.98K - Net profit after production cost
- **Total Products Listed**: 50 - Number of products in the inventory
- **Total Sales Volume**: 1,026 - Number of transactions completed

### Visualizations

1. **Best Selling Products (Horizontal Bar Chart)**
   - Ranks top 10 products by sales revenue
   - Helps identify star performers and inventory priorities
   - Led by Ariel Footwear ($70K), Boat Accessories ($68K), and Set Dairy ($64K)

<p align="center">
  <img src="Visuals/Best Selling Products.png" alt="Bar chart showing best selling products by revenue" width="50%">
  <br>
  Analysis of Best Selling Products for the year 2025
</p>

2. **Sales Trend (Line Chart)**
   - Monthly sales progression from January to September 2025
   - Identifies seasonal patterns and growth trends
   - Shows peak performance in May 2025 (~$150K)


3. **Best Selling Product Category (Pie Chart)**
   - Revenue distribution across three main categories
   - Fashion: 51% (largest segment)
   - Electronics: 32%
   - Groceries: 17%


4. **Male vs Female Customer Transactions (Donut Chart)**
   - Customer base composition by gender
   - Female customers: 157 transactions
   - Male customers: 194 transactions
   - Helps tailor marketing strategies

<p align="center">
<br>
<img src="Visuals\Male V Female Customers Chart.PNG" alt="Donut chart showing Male VS Female Customer Transactions" width="40%">
<br>
Male VS Female Customer Transactions
</p>

5. **Who's Buying the Most? (Bar Chart)**
   - Purchase frequency across age groups
   - Primary customers: 60-70 age group (85 purchases)
   - Secondary segment: 20-30 years (75 purchases)
   - Declining engagement in older demographics despite 60-70 age group having the most transactions

<p align="center">
<br>
<img src="Visuals\Best Buyers.png" alt="Bar chart showing Customer Demographics With Most Transactions" width="65%">
<br>
Customer Transactions by Age
</p>


## 🎨 Features

### Interactive Slicers
- **Store Selection Slicer**: 
  - Filters data across 5 SuperMart store locations
  - Enables location-specific performance analysis
  - Currently displaying: SuperMart Peckmouth
  
- **Year Selection Slicer**: 
  - Historical analysis from 2023 to 2025
  - Year-over-year comparison capability
  - Currently displaying: 2025 data

### Design Elements
- **Color-Coded Insights**: Turquoise and dark gray theme for clear data distinction
- **Responsive Layout**: Clean, professional design suitable for presentations
- **Real-time Filtering**: All visualizations update dynamically based on slicer selections

## 💾 About the Dataset

**Data source**:  [Kaggle.com](https://www.kaggle.com)

**Time Period**: 2023 - 2025 (3 years of historical data)

**Store Locations**: 5 SuperMart stores across different locations

The dataset includes:
- Transaction records with dates and amounts
- Product information (names, categories, prices)
- Customer demographics (age, gender)
- Store location data

## 🗂️ Database Schema

### Database Structure
The database follows a Star Schema design with four tables:
<p align="center">
<br>
<img src="Visuals\Star schema.png" alt="Database Schema" width="100%">
<br>
</p>

 **Customers (Dimension Table)**

- CustomerID (PK), First_Name, Gender, Age, Age_Group, Birth_Date, City

**Products (Dimension Table)**

- Product_ID (PK), Product_Name, Category, SubCategory, Unit_Price, Cost_Price

**Stores (Dimension Table)**
- Store_ID (PK), Store_Name, City, Region

**Transactions (Fact Table)**

- Transaction_ID (PK), Customer_ID (FK), Product_ID (FK), Store_ID (FK), Date, Quantity, Discount, Payment_Method

### Relationships

- Customers (1) → Transactions (M)
- Products (1) → Transactions (M)
- Stores (1) → Transactions (M)

The Transactions table serves as the central fact table, connecting all dimension tables for efficient analytical queries.

## 🛠️ Technical Implementation

**Visualization Tool**: Power BI Desktop

**Data Processing**: 
- Data Cleaning and Transformation: Power Query Editor

<p align="center">
<br>
<img src="Visuals\Applied Steps to the Customer Table.PNG" alt="Applied Steps in Power Query for the Customer Table" width="45%">
<br>
Applied Steps In Power Query
</p>

- DAX (Data Analysis Expressions) for calculated measures and columns


<p align="center">
<br>
<img src="Visuals\DAX.PNG" alt="Applied Steps in Power Query for the Customer Table" width="45%">
<br>
Calculated Measures Using DAX
</p>

**Data Source**: Excel Workbook file from Kaggle

**Key Features Implemented**:
- Interactive slicers for dynamic filtering (Store and Year)
- Custom color theme (Turquoise and Dark Gray)
- Calculated measures for KPIs (Total Sales, Total Profit, Sales Volume)
- Conditional formatting for enhanced visual appeal
- Responsive dashboard layout optimized for presentation

## 📋 Key Insights

1. **Fashion dominates revenue** with 51% of total sales, indicating strong performance in apparel and accessories
2. **Young adults (20-30 years)** are in the primary customer base, suggesting opportunities for youth-focused marketing
3. **Sales volatility** is evident with peaks in May and troughs in June, requiring inventory management strategies
4. **Balanced gender distribution** (slightly male-skewed) indicates broad market appeal
5. **Top 3 products** account for a significant portion of revenue, highlighting dependency on star products

## 🎯 Business Recommendations

- Focus inventory investment on top-performing Fashion category
- Develop targeted campaigns for the 20-30 age demographic
- Investigate the May sales spike to replicate success factors
- Diversify product portfolio to reduce dependency on top sellers
- Explore strategies to engage the 50+ demographic

## 📝 Future Enhancements

- Add store-to-store comparison dashboard page
- Include profit margin analysis by product and category
- Implement geographic heat maps for regional performance analysis
- Add forecasting models for sales prediction using time series analysis
- Create customer lifetime value metrics
- Develop drill-through functionality for detailed transaction analysis
- Add monthly/quarterly/yearly view toggle options
- Include inventory turnover rate calculations

---

**Last Updated**: October 2025  