# Bike Buyers Analysis – Excel Project

## Overview
This project analyzes customer purchasing behavior using Excel-based data cleaning, transformation, PivotTables, and dashboard design.

The goal is to identify which demographic groups are most likely to purchase a bicycle and highlight key factors such as income, age, commute distance, education, and region.
The final result is an interactive Excel dashboard that enables stakeholders to explore insights through slicers and dynamic charts.

## Dataset
The dataset includes 1,000 customer records with attributes:

* Gender
* Marital Status
* Income
* Education
* Occupation
* Home Ownership
* Number of Cars
* Commute Distance
* Region
* Age & Age Bracket
* Purchased Bike (Yes/No)

## Data Cleaning & Preparation (Working\_sheet)
Data cleaning was performed directly inside Excel, including:

### Column normalization
* Standardized column names
* Fixed inconsistent category labels (e.g., gender, region, education levels)

### Handling missing & invalid values
* Checked blanks
* Replaced invalid entries
* Validated numeric formatting for income & age

### Feature engineering
* Created additional fields such as:
    * Age Bracket (Adolescent, Middle Age, Old)
    * Cleaned commute distance categories
    * Cleaned income formatting (converted text → number)

### Data restructuring
* Sorted and grouped demographic attributes
* Prepared the dataset for PivotTable analysis

## Pivot Table Analysis
Several PivotTables were created to summarize key patterns:

### 1. Average Income Per Purchase
* Compared average income between customers who purchased and did not purchase a bike
* Breakdown by Gender

**Insight:**
Male customers have higher income on average and a higher likelihood of purchasing a bike.

### 2. Customer Commute Distance vs Purchase
* Count of purchases by commute distance
* Overlayed line charts for Yes/No purchase decisions

**Insight:**
Customers in 0–1 miles and 1–2 miles commute range show higher purchase frequency.
Purchase likelihood decreases as commute distance increases.

### 3. Customer Age Bracket
* Pivot analysis by:
    * Adolescent
    * Middle Age
    * Old

**Insight:**
Middle-aged customers are most likely to purchase a bike.

## Final Dashboard (Interactive)
The dashboard includes:

* **Slicers** for Marital Status, Region, Education, Gender, Age Bracket
* **Interactive charts:**
    * Average Income Per Purchase
    * Customer Age Bracket Purchase Patterns
    * Commute Distance vs Purchase Decision

**This allows users to explore:**
* Which demographic segments are most profitable
* How income and distance impact purchase decisions
* Which groups to target for marketing campaigns

## Key Insights
From the analysis:

* Income is positively associated with bike purchasing likelihood
* Middle-aged customers are the strongest buyer segment
* Short-distance commuters (0–2 miles) buy more frequently
* Region and education level influence purchase probability
* Women buy slightly fewer bikes but trends vary across income brackets

These insights can guide targeted marketing, demographic-based promotions, and product positioning.

## Tools & Techniques Used
* Microsoft Excel
* Data Cleaning (Find & Replace, text-to-columns, data validation)
* PivotTables & PivotCharts
* Slicers & interactive filters
* Dashboard layout design
* Feature engineering (age bracket, commute distance grouping, income formatting)

`Excel_Project_Dataset.xlsx` includes:
* `bike_buyers` — raw dataset
* `Working_sheet` — cleaned dataset with engineered features
* `Pivot_Table` — all PivotTables and summary analysis
* `Dashboard` — final interactive dashboard

## How to Use
1.  Download the repository
2.  Open `Excel_Project_Dataset.xlsx`
3.  Navigate across tabs:
    * Raw data
    * Cleaned working sheet
    * PivotTable analysis
    * Final dashboard
4.  Use slicers on the dashboard to explore insights
