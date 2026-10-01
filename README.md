# Samsung Supply Chain Analytics Dashboard

An interactive **Supply Chain Analytics Dashboard** built with **Power BI** to analyze supplier performance, manufacturing operations, shipment efficiency, sales, and customer performance.

The project transforms a public training dataset into an interactive Business Intelligence solution using **data modeling, DAX, KPI analysis, data visualization, and data storytelling**.

> **Dataset:** Publicly available training dataset used for analytics practice and portfolio development.

---

## 📌 Project Overview

Supply chain performance depends on multiple interconnected areas, including procurement, manufacturing, inventory, logistics, sales, and customers.

This dashboard brings these areas together into a single analytical solution, providing a structured view of operational and commercial performance.

The dashboard is organized into four main business areas:

* **Supplier**
* **Manufacturer**
* **Shipment**
* **Sales & Customers**

An **Executive Overview** provides a high-level summary of the overall performance.

---

## 🎯 Business Objectives

The dashboard was designed to answer key business questions such as:

* How are suppliers performing in terms of cost, quality, and lead time?
* How efficiently are manufacturing facilities operating?
* How is production volume related to product quality?
* What are the main causes of shipment delays?
* How are carriers performing in terms of on-time delivery?
* How does shipment weight relate to shipping cost?
* How are revenue and profitability changing over time?
* How do discounts relate to profitability?
* Which products contribute most to revenue?
* How is revenue distributed across different sales channels?

---

# 📊 Dashboard Pages

## 1. Executive Overview

Provides a high-level overview of supply chain and business performance.

### Key Performance Indicators

* **Total Revenue:** $176.95M
* **Total Profit:** $48.56M
* **Profit Margin:** 27.44%
* **Total Logistics Cost:** $97.55M
* **On-Time Delivery:** 75.29%
* **Total Quantity:** 129K
* **Avg Lead Time:** 11.53 Days

### Supply Chain Overview

The page provides a snapshot of four major areas:

**Supplier**

* Total Quantity
* Avg Lead Time
* Product-level supplier analysis

**Manufacturer**

* Current Stock
* Inventory distribution by product

**Shipment**

* Total Quantity Delivered
* On-Time Delivery %

**Sales & Customers**

* Avg Discount %
* Revenue by Product

---

# 2. Supplier Details

This page analyzes supplier performance and procurement operations.

### Key Performance Indicators

* **Total Suppliers:** 7
* **Total Procurement Cost:** $78.13M
* **Total Order Quantity:** 129K
* **Avg Quality Score:** 96.63
* **Avg Lead Time:** 11.53 Days

### Key Analysis

**Procurement Cost Trend**

Tracks how procurement costs change over time.

**Procurement Cost by Supplier**

Compares procurement spending across suppliers.

**Supplier Performance**

Analyzes supplier performance across different component types and supplier tiers.

**Supplier Quality by Country**

Compares supplier quality scores across countries.

---

# 3. Manufacturer Details

This page focuses on production performance, manufacturing quality, facilities, and inventory.

### Key Performance Indicators

* **Total Quantity Produced:** 4M
* **Avg Defect Rate:** 0.68%
* **Total Defective Units:** 24K
* **Total Production Batches:** 4,500
* **Total Facilities:** 6

### Key Analysis

**Production Trend**

Tracks production volume over time.

**Production Volume vs Quality**

Analyzes the relationship between production volume and defect rate.

**Production by Facility**

Compares production output across manufacturing facilities.

**Stock vs Reorder Point**

Compares current inventory levels against reorder points to identify inventory conditions.

---

# 4. Shipment Details

This page analyzes shipment volume, delivery performance, carriers, delays, and logistics costs.

### Key Performance Indicators

* **Total Shipments:** 7,500
* **Total Quantity Delivered:** 129K
* **On-Time Delivery:** 75.29%
* **Total Shipping Cost:** $19.42M
* **Avg Delivery Time:** 14.19 Days

### Key Analysis

**On-Time Delivery Trend**

Tracks delivery performance over time.

**Carrier Performance**

Compares carriers based on their on-time delivery performance.

**Delay Reasons**

Analyzes the main reasons behind shipment delays, including:

* Carrier capacity
* Documentation issues
* Port congestion
* Customs clearance
* Weather
* Other operational factors

**Shipping Cost vs Weight**

Explores the relationship between shipment weight and shipping cost.

---

# 5. Sales & Customers

This page focuses on commercial performance, profitability, products, discounts, and sales channels.

### Key Performance Indicators

* **Total Revenue:** $176.95M
* **Total Profit:** $48.56M
* **Profit Margin:** 27.44%
* **Quantity Sold:** 187K
* **Avg Discount:** 5.03%

### Key Analysis

**Revenue & Profit Trend**

Tracks revenue and profit performance over time.

**Discount vs Profitability**

Analyzes the relationship between discounts and profitability.

**Product Performance**

Compares revenue contribution across product lines.

**Revenue by Channel**

Analyzes revenue distribution across:

* Online
* Retailer
* Direct

---

# 🧩 Data Model

The project uses a **Star Schema** approach to organize the data model and support efficient analytical reporting.

## Dimension Tables

* `dim_customer`
* `dim_date`
* `dim_facility`
* `dim_product`
* `dim_supplier`

## Fact Tables

* `fact_inventory`
* `fact_procurement`
* `fact_production`
* `fact_sales`
* `fact_shipment`

### Model Structure

<img width="952" height="471" alt="image" src="https://github.com/user-attachments/assets/7987b17f-bb00-4020-8147-7cd63cc9c8dd" />


```

The model separates **business events through fact tables** from descriptive attributes through dimension tables, enabling analysis across different supply chain processes.

---

# 📐 DAX & Measures

The dashboard uses DAX measures to calculate and analyze key business metrics.

### Key Measures

* Total Revenue
* Total Profit
* Profit Margin %
* Total Logistics Cost
* Total Procurement Cost
* Total Order Quantity
* Total Quantity Produced
* Total Defective Units
* Defect Rate %
* Total Shipments
* Total Quantity Delivered
* On-Time Delivery %
* Total Shipping Cost
* Avg Delivery Time
* Avg Lead Time
* Quantity Sold
* Avg Discount %

The measures are designed to dynamically respond to dashboard filters and user selections.

---

# 🎛️ Interactive Features

## Bookmarks

**Power BI Bookmarks** are used throughout the dashboard to provide interactive navigation and improve the user experience.

The **Landing Page** allows users to navigate between the main analytical sections.

Each analytical page also includes a **Custom Analysis** bookmark that opens an additional exploratory analysis view.

---

## 🔍 Custom Analysis — Decomposition Tree

Each analytical page includes a **Custom Analysis** section using the **Decomposition Tree** visual.

The Decomposition Tree allows users to break down a selected KPI across different dimensions and explore the factors contributing to the metric.

Depending on the analytical page, users can explore metrics across dimensions such as:

* Carrier
* Status
* Delay Reason
* Product Line
* Product Name
* Facility
* Country
* Supplier
* Tier
* Specialty

This provides an additional layer of exploratory analysis beyond the predefined dashboard visuals.

---

## 🎚️ Interactive Slicers

The dashboard includes interactive slicers that allow users to dynamically filter the analysis.

Available slicers include:

* **Year**
* **Quarter**
* **Tier**
* **Country**
* **Specialty**

These filters allow users to analyze the data from different:

* Time perspectives
* Geographic perspectives
* Supplier tiers
* Specialty categories

The selected filters dynamically update the relevant KPIs and visualizations throughout the dashboard.

---

## 🧭 Dashboard Navigation

The dashboard combines:

* Landing Page navigation
* Page-level Bookmarks
* Custom Analysis views
* Interactive Slicers
* Cross-filtering
* KPI Cards
* Tooltips
* Decomposition Trees

This creates both a **structured analytical experience** through predefined visuals and an **exploratory analytical experience** through interactive analysis.

---

# 📈 Data Visualization

Different visualization types were selected based on the analytical question being addressed.

### Line Charts

Used to analyze trends over time, including:

* Procurement Cost
* Production Volume
* On-Time Delivery
* Revenue & Profit

### Bar Charts

Used to compare:

* Suppliers
* Facilities
* Carriers
* Delay Reasons
* Products

### Scatter Charts

Used to explore relationships such as:

* Production Volume vs Defect Rate
* Shipping Cost vs Shipment Weight
* Discount vs Profitability

### KPI Cards

Used to provide a quick overview of important business metrics.

### Decomposition Tree

Used for interactive root-cause-style exploration by breaking down selected metrics across multiple dimensions.

---

# 💡 Business Analysis Areas

The dashboard enables analysis across several supply chain and commercial areas:

### Supplier Performance

* Procurement cost
* Supplier quality
* Lead time
* Supplier tier
* Component categories
* Geographic performance

### Manufacturing Performance

* Production volume
* Defect rate
* Defective units
* Facility performance
* Inventory levels
* Reorder points

### Shipment Performance

* Shipment volume
* On-time delivery
* Delivery time
* Carrier performance
* Delay reasons
* Shipping cost
* Shipment weight

### Sales & Customer Performance

* Revenue
* Profit
* Profit margin
* Product performance
* Sales channels
* Discounts
* Customer dimensions

---

# 🔎 Key Business Insights

The dashboard analysis highlighted several measurable patterns across the analyzed data:

### 1. Revenue and Profitability

The analyzed data generated **$176.95M in total revenue** and **$48.56M in total profit**, resulting in a **27.44% profit margin**.

### 2. Logistics Cost

**Total Logistics Cost reached $97.55M**, representing approximately **55.1% of total revenue**. This makes logistics a major cost component within the analyzed dataset.

### 3. Delivery Performance

The overall **On-Time Delivery rate is 75.29%**, meaning approximately three out of every four deliveries were completed on time according to the dashboard KPI.

### 4. Revenue Concentration

The leading products shown in the Executive Overview contribute a substantial share of total revenue. The two highest-revenue products shown contribute approximately **$62M**, or around **35% of total revenue**.

These findings provide a starting point for deeper analysis of product contribution, logistics efficiency, delivery performance, and supply chain costs.

---

# 🛠️ Tools & Technologies

* **Power BI**
* **DAX**
* **Power Query**
* **Star Schema Data Modeling**
* **Data Visualization**
* **Business Intelligence**
* **KPI Development**
* **Data Storytelling**
* **Decomposition Tree**
* **Power BI Bookmarks**

---

# 📁 Project Structure

```text
Samsung-Supply-Chain-Analytics/
│
├── README.md
│
├── Power BI/
│   └── Samsung_Supply_Chain_Analytics.pbix
│
├── Dataset/
│   └── dataset_file
│
└── Screenshots/
    ├── 01_Landing_Page.png
    ├── 02_Executive_Overview.png
    ├── 03_Supplier_Details.png
    ├── 04_Manufacturer_Details.png
    ├── 05_Shipment_Details.png
    └── 06_Sales_Customers.png

```

---

# 🖼️ Dashboard Preview

## Landing Page

<img width="515" height="290" alt="1  Landing Page" src="https://github.com/user-attachments/assets/fe0bd84a-25a3-48ea-8f96-4b2129ef0a37" />


## Executive Overview

<img width="498" height="280" alt="2  Executive Overview" src="https://github.com/user-attachments/assets/8ff8b7ce-25d9-4d1d-8aaf-664e9e8329ad" />


## Supplier Details

<img width="499" height="280" alt="3  Supplier Details" src="https://github.com/user-attachments/assets/1d4f3d6c-d54d-413d-b7c7-09564f7aa193" />


## Manufacturer Details

<img width="499" height="279" alt="4  Manufacturer Details" src="https://github.com/user-attachments/assets/4723339a-be1b-469e-8794-6d18fb21b485" />


## Shipment Details

<img width="498" height="281" alt="5  Shipment Details " src="https://github.com/user-attachments/assets/5ffd19d3-b599-4950-86d9-b997afa7d2dc" />


## Sales & Customers

<img width="499" height="280" alt="6  Sales   Customers" src="https://github.com/user-attachments/assets/73d35f98-2525-4410-ba12-5bfd2ec1ccad" />


---

# 🔄 Analytics Workflow

The project follows an end-to-end analytics workflow:

```text
Raw Data
   ↓
Data Preparation
   ↓
Data Modeling
   ↓
Star Schema
   ↓
DAX Measures
   ↓
KPI Development
   ↓
Data Visualization
   ↓
Interactive Dashboard
   ↓
Business Analysis
   ↓
Data Storytelling

```

---

# 🎯 Project Focus

This project demonstrates an end-to-end **Data Analytics and Business Intelligence workflow**, from structuring raw data and building a Star Schema to creating DAX measures, designing interactive visuals, and presenting business-oriented analysis.

The focus was on combining **technical implementation with business thinking**, rather than creating visuals alone.

---

## 📌 Disclaimer

This project uses a **publicly available training dataset** for educational and portfolio purposes.

The dashboard and analysis were independently developed as part of a Data Analytics portfolio project.

The results shown in the dashboard should not be interpreted as internal, proprietary, or official Samsung company data.

