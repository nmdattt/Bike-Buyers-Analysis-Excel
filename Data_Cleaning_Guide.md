# Data Cleaning Guide – Bike Buyers Dataset
This document outlines the complete data cleaning and preparation workflow performed in Excel to transform the raw `bike_buyers` dataset into an analysis-ready format for PivotTables and dashboard visualization.

## 1. Create a Working Copy of the Dataset
To preserve the original data:

* Open the `bike_buyers` sheet (raw dataset).
* Select all rows and columns (Ctrl + A).
* Copy the data and paste it into a new sheet named `Working_sheet`.
* All cleaning steps are performed in `Working_sheet` to ensure the raw dataset remains unchanged.

## 2. Remove Duplicate Records
* Go to the `Working_sheet`.
* Select the entire table (Ctrl + A).
* Navigate to:
    * **Data → Remove Duplicates**
* Select all columns and confirm.

This step eliminates any duplicated customer entries that may skew results.

## 3. Standardize Categorical Variables
Several columns use abbreviations. These are cleaned using **Find & Replace (Ctrl + H)** to ensure consistency across the dataset.

### Marital Status
* M → Married
* S → Single

### Gender
* M → Male
* F → Female

This improves clarity for dashboards and avoids confusion in PivotTables.

## 4. Fix Formatting for Numeric Fields (if applicable)
Some fields such as Income or Age may appear as text depending on data source formatting.
Check and correct them:

* Select the column
* Use **Home → Number Format → Number**
* Remove commas or symbols if needed
* Convert text to numbers using:
    * **Data → Text to Columns → Finish**

This ensures calculations and charts work correctly.

## 5. Create Derived Fields (Feature Engineering)
### Create Age Brackets
A new column called `Age Brackets` is added to segment customers into meaningful groups.

Formula (assuming Age is in column L):
```excel
=IF(L2>54,"Old",IF(L2>=31,"Middle Age",IF(L2<31,"Adolescent","Invalid")))
```

Resulting groups:
* **Old:** Age > 54
* **Middle Age:** 31–54
* **Adolescent:** Age < 31
* **Invalid:** Catch-all for unexpected values

This field is crucial for demographic segmentation in PivotTables and dashboards.

## 6. Validate Remaining Columns
Perform a final pass through the dataset:

* Check for spelling inconsistencies
* Ensure Region (Europe / Pacific / North America) is standardized
* Verify Commute Distance categories (e.g., 0–1 Miles, 2–5 Miles, 10 Miles +)
* Confirm all Yes/No fields are consistent (Home Owner, Purchased Bike, etc.)

This step guarantees clean dimensions for dashboards and avoids fragmented categories.

## Final Outcome
After completing all steps:

* The `Working_sheet` contains a clean, standardized, analysis-ready dataset.
* The data can now be used reliably in:
    * PivotTables
    * PivotCharts
    * Interactive Dashboard
    * Segmentation Analysis

This cleaning process ensures accurate and meaningful insights for the final Bike Buyers Dashboard.
