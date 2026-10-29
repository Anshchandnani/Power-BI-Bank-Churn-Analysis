# Bank Customer Churn Analysis \| Power BI

## Overview

This is my third Power BI dashboard project, built using a provided bank
customer churn dataset containing 10,000 customer records. I
independently explored the data, cleaned and transformed it, created
charts without following a reference dashboard, and practised DAX and
drill-through functionality.

## Project Objectives

-   Explore customer churn patterns.
-   Clean and transform the provided data.
-   Design visualizations independently, without a reference dashboard.
-   Practise DAX measures and calculated columns.
-   Use drill-through to navigate from summary insights to more detailed
    report views.

## Dataset

The repository includes: - `Bank_Churn(1).csv` --- customer churn
dataset. - `Bank_Churn_Data_Dictionary(1).csv` --- descriptions of the
dataset fields.

The dataset includes fields such as credit score, geography, age,
tenure, balance, number of products, active membership, estimated
salary, and whether a customer exited.

## Skills Practised

### Data Preparation

-   Inspected the provided dataset.
-   Cleaned and transformed data in Power Query.
-   Prepared fields for analysis and visualization.

### DAX

DAX (Data Analysis Expressions) is the formula language used in Power BI
to create measures and calculated columns.

Examples of churn-related measures that can be used if they match the
definitions in the report:

**Total Customers**

``` dax
Total Customers = COUNTROWS('Bank_Churn')
```

**Churned Customers**

``` dax
Churned Customers =
CALCULATE(
    COUNTROWS('Bank_Churn'),
    'Bank_Churn'[Exited] = 1
)
```

**Churn Rate**

``` dax
Churn Rate =
DIVIDE(
    [Churned Customers],
    [Total Customers],
    0
)
```

These are illustrative examples based on the provided dataset schema.
The measures actually used in the PBIX may differ.

### Calculated Columns

Calculated columns evaluate an expression row by row and store the
result in the model. Measures calculate results dynamically according to
the filter context of a report.

### Drill Through

Drill-through lets users right-click a data point and open a detail page
filtered to the selected item or category. It helps users move from a
high-level summary to a more detailed view.

## Tools Used

-   Microsoft Power BI Desktop
-   Power Query
-   DAX
-   CSV

## Project Files

-   `Bank_Churn_Dashboard.pbix` --- Power BI report file.
-   `Bank_Churn(1).csv` --- source dataset.
-   `Bank_Churn_Data_Dictionary(1).csv` --- data dictionary.

## How to Open

1.  Download or clone this repository.
2.  Open `Bank_Churn_Dashboard.pbix` in Power BI Desktop.
3.  If prompted, update the data source path to the included CSV file.
4.  Explore the report pages, visuals, and drill-through interactions.

## Learning Journey

This is my third dashboard in my Power BI learning journey. I was given
the dataset and independently handled data preparation, visualization
choices, chart creation, and DAX practice without following a reference
dashboard.

## Note

The DAX measures shown above are examples for the supplied churn
dataset, not a claim that these exact formulas are already present in
the PBIX file. Verify the final report's measure names and definitions
before publishing.
