## E-Commerce-Sales-Analysis
## Table of Content
-[The Problem](#the-problem)
-[objectives](#objectives)
-[Import and Clean Data](#import-and-clean-data)
-[Create Pivot Table](#create-pivot-table)
-[Key Insights](#keys-insights)
-[Actionable Recommendations](#actionable-recommendations)

### Project Title: “Analyzing E-Commerce Sales Performance to Drive Strategic Decisions”

### The Problem
In a competitive e-commerce landscape, businesses struggle to understand which products perform best, how customer behavior evolves, and which regions or strategies yield the highest return. Without actionable data insights, decisions around inventory, marketing, and customer retention are often based on guesswork.

### Objectives
In this project, l explore the e-commerce transactional dataset to analyze customer behavior and purchasing patterns across product categories, regions, and time periods.  The primary goal of this Exploratory Data Analysis (EDA) on e-commerce transaction data is to: 

- Understand sales performance across product categories and regions
- Identify customer purchasing patterns and top spenders
- Uncover high-performing and underperforming areas of the business
- Provide strategic recommendations to improve revenue, retention, and marketing efforts

Through detailed exploratory data analysis (EDA), the project aims to highlight high-performing product segments, seasonal sales trends, and payment preferences. By using Excel for pivot-based EDA and Power BI for interactive dashboards, this project demonstrates both spreadsheet-based analysis and modern data visualization capabilities suitable for business intelligence roles.

### Import and Clean Data
#### In Excel:
I loaded the ecommerce.csv file into Excel.

<img width="602" height="322" alt="ecommerce screenshot raw" src="https://github.com/user-attachments/assets/c53b891d-5d1d-494e-96f5-417b5039b794" />

Before l jump into analysis, l took time to familiarize myself with the dataset. Asking myself the following questions:
- What are the key variables (e.g., product, region, price, etc)?
- Are there categorical or numerical data?
- Are there missing or inconsistent values?

Next, l jumped into cleaning using:

-	Filter, Sort, Remove Duplicates
-	Data Types: Ensure dates, currencies, and numbers are correct
-	Create calculated columns for:   Total Sales = Price * Quantity

<img width="602" height="321" alt="ecommerce screenshot 1" src="https://github.com/user-attachments/assets/5bb999bc-ef99-49ae-bafb-079f3cdf7c09" />
<br></br>
<img width="602" height="322" alt="ecommerce screenshot 2" src="https://github.com/user-attachments/assets/f8748e76-819f-4d48-8fe7-182ec9fd90aa" />

#### Power BI:
In Power BI, l used the Power Query to:

- Clean column names (Transform > Clean)
- Change data types (date, text, number)
- Remove nulls or outliers
- Create custom columns (Add Column > Custom Column)
- Format OrderDate, create Year, Month, Week columns

<img width="467" height="250" alt="power bi cleaning1" src="https://github.com/user-attachments/assets/3925c4fe-f58c-44fa-9ac3-8639603660c1" />
<br></br>
<img width="476" height="254" alt="power bi cleaning2" src="https://github.com/user-attachments/assets/e293bb1b-c338-4162-a6cb-f0f78cd8d59c" />

### Create Pivot Tables (Excel) 
#### In Excel
l created:

- Pivot table: Total sales by Category, Region, CustomerID
- Pivot charts: Sales trends, top-selling products

<img width="431" height="229" alt="pivot1" src="https://github.com/user-attachments/assets/22a12470-6ab6-4d73-8c11-0a18e4716f7b" /> 
<br></br>

##### Pivot charts: Sales trends.
<img width="427" height="213" alt="pivot2" src="https://github.com/user-attachments/assets/e488f352-e11d-46e6-82d8-9b3c72fb05af" />
<br></br>

##### Pivot charts: Top-selling products
<img width="503" height="269" alt="pivot3" src="https://github.com/user-attachments/assets/9baa67e9-1cfb-4d56-98ba-b196591130fe" />

#### In Power BI:
Key metrics are calculated as follows using New Measure:
- Total Revenue = SUM(ecommerce_dataset[TotalAmount])
- Avg Order Value = DIVIDE([Total Revenue], COUNT(ecommerce_dataset[OrderID]))
- Unique Customers: DISTINCTCOUNT(CustomerID)

<img width="602" height="319" alt="power bi measure" src="https://github.com/user-attachments/assets/3eb54abb-ed37-4ff1-a2c8-b9147c7cd5eb" />

### Key Insights
1. Total Revenue Generated:  £463,900.97
   
<img width="192" height="151" alt="card total revenue" src="https://github.com/user-attachments/assets/bddb979c-a2b8-494b-82aa-70689e42dd7d" />

2. Top Product Categories by Revenue are:
-	Clothing
- Electronics
- Home & Kitchen
- Books
- Toys
<img width="334" height="222" alt="total revenue by category" src="https://github.com/user-attachments/assets/e2490feb-c0a1-484d-8a2f-307055c3c59f" />

3. Top-Selling Products are:
Jeans, Laptop, Jacket, Blender, Phone

<img width="405" height="294" alt="top selling products" src="https://github.com/user-attachments/assets/8f3c1678-3ffd-4894-add5-29bffbc8e729" />

4. Customer Overview: 240 unique customers and average of 3.12 orders per customer
<img width="353" height="134" alt="card unique customer" src="https://github.com/user-attachments/assets/ebef2fe0-085c-4a28-96ae-99bdcb864bdf" />

5. Preferred Payment Methods are:
-	Bank Transfer (most common)
-	Digital Wallet
-	PayPal
<img width="221" height="163" alt="payment method" src="https://github.com/user-attachments/assets/a75ecc13-013a-4e1b-98c1-a2438530c283" />

6. Regional Performance: are:
- East & North regions have the most orders
- North, West, South regions generate the lowest revenue

<img width="265" height="164" alt="region" src="https://github.com/user-attachments/assets/ac2465d4-1e78-45e8-9568-734359157303" />

#### Actionable Recommendations
Based on this analysis:

- Focus on top-performing categories e.g. Clothing & Electronics for future promotions and bundling.
- Investigate underperforming regions with localized marketing and possible logistical improvements.
- Enhance the checkout process by prioritizing Digital Wallet and Bank Transfer options.
- Introduce loyalty or referral programs for the 240 unique customers to drive repeat purchases.
- Leverage top-selling products in advertisements and cross-selling opportunities.
- Use historical trends to forecast demand and optimize inventory before peak seasons.


