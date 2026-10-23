# power-bi-cohort-retention-analysis
 Power BI cohort analysis exploring customer retention and performance across monthly cohorts.

 ##Project Overview

This project explores customer retention and performance across monthly cohorts using Microsoft Power BI.

The analysis uses order data from January to December 2024 to examine how customer activity changes across subsequent periods. An interactive cohort matrix allows users to switch between customer counts and percentage-based metrics to explore cohort performance.

The project demonstrates data preparation, calculated columns, DAX measures, field parameters, matrix visualizations, and conditional formatting in Power BI.

🎯 Business Objectives

- Analyze customer behavior across monthly cohorts.
- Understand how customer counts change across subsequent periods.
- Examine percentage-based performance across cohorts.
- Compare cohort performance using a matrix visualization.
- Make cohort patterns easier to interpret through conditional formatting.
- Provide a foundation for data-driven customer retention analysis.

🗂️ Project Structure

power-bi-cohort-retention-analysis/
│
├── README.md
│
├── data/
│   └── cohort_orders_dataset.xlsx
│
├── powerbi/
│   └── cohort_retention_analysis.pbix
│
├── screenshots/
│   ├── cohort_customers.png
│   ├── cohort_conversion_rate.png
│   └── dataset_preview.png
│
└── insights.md

Note: The filenames above are suggested examples. Rename the links and files to match your actual GitHub repository.

📁 Dataset

The project uses an order-level dataset containing the following fields visible in the source dataset:

Column| Description
"order_date"| Date associated with the order
"customer_id"| Customer identifier
"order_id"| Order identifier
"store_id"| Store identifier
"store_order"| Numeric order value shown in the dataset

The dataset is used to prepare customer cohort information and analyze customer counts and percentage-based metrics over time.

Dataset: "View the dataset" (data/cohort_orders_dataset.xlsx)

🛠️ Tools & Technologies

- Microsoft Power BI Desktop — report development and visualization
- DAX — calculated columns and measures
- Power BI Field Parameters — switching between displayed metrics
- Power BI Matrix Visual — cohort analysis
- Conditional Formatting — visual comparison of cohort values
- Excel — viewing the source dataset

🔄 Data Preparation & DAX

1. Calculated Columns

Three calculated columns were created in the "orders" table.

First Purchase Date

Identifies the first purchase date associated with a customer. This field is used to establish the customer's starting point for cohort analysis.

Cohort Date

Groups customers according to their first-purchase month, allowing monthly cohorts to be compared.

Period

Represents the period elapsed between a customer's cohort and a subsequent period of activity. It is used to position values in the cohort matrix.

The exact DAX expressions and full field names will be documented once the formulas are added.

2. DAX Measures

Customers

The "customers" measure is used to display customer counts across cohort periods.

It supports the customer-count view of the cohort matrix.

Conversion Rate

The "conversion rate" measure displays percentage-based values across cohort periods.

It supports the percentage view of the cohort matrix.

Metric clarification: The displayed percentage is currently documented as a conversion rate because that is the label shown in the report. Its exact business definition depends on the DAX formula and denominator used. It should only be described as a retention rate if the calculation measures returning customers against the appropriate cohort baseline.

3. Field Parameters

A field parameter named "status" was created to switch the matrix between the available measures:

- "customers"
- "conversion rate"

This allows users to explore customer counts and percentage-based performance within the same report visual.

📈 Dashboard & Visualizations

Customer Cohort Matrix

The customer-count matrix displays monthly cohorts from January to December 2024, with period columns ranging from 0 to 11.

The matrix uses conditional formatting to help distinguish higher and lower customer counts. Blank future periods remain unpopulated where data is not available.

"Customer Cohort Matrix" (screenshots/cohort_customers.png)

"Open the customer cohort screenshot" (screenshots/cohort_customers.png)

Percentage-Based Cohort Matrix

The percentage view displays the "conversion rate" measure across the same monthly cohort structure.

The field parameter allows users to switch from customer counts to percentages without requiring a separate matrix for each measure.

"Conversion Rate Cohort Matrix" (screenshots/cohort_conversion_rate.png)

"Open the percentage cohort screenshot" (screenshots/cohort_conversion_rate.png)

Dataset Preview

The source dataset contains order dates, customer identifiers, order identifiers, store identifiers, and order values.

"Dataset Preview" (screenshots/dataset_preview.png)

"Open the dataset screenshot" (screenshots/dataset_preview.png)

🔍 Initial Observations

Based on the customer-count matrix displayed in Power BI:

- The total displayed customer count for period 0 is 835.
- The displayed totals decrease across later periods.
- Period 1 shows a total of 326, compared with 835 in period 0.
- Period 5 shows a total of 140.
- Period 9 shows a total of 29.
- Period 10 shows a total of 4, and period 11 shows a total of 1.

These are the totals displayed in the current matrix. They should be interpreted in the context of the underlying data, cohort maturity, and measure definition.

The percentage matrix displays the following total percentages by period:

Period| Displayed percentage
0| 16.7%
1| 6.5%
2| 5.4%
3| 4.0%
4| 2.8%
5| 2.8%
6| 1.8%
7| 1.1%
8| 1.1%
9| 0.6%
10| 0.1%
11| 0.0%

These percentages are reproduced from the displayed report. Their precise interpretation requires validation of the "conversion rate" measure.

💡 Business Value

Cohort analysis helps businesses understand how customer activity evolves after an initial purchase or other defined starting event.

Potential business applications include:

- Identifying cohorts with stronger subsequent customer activity.
- Comparing customer behavior across acquisition months.
- Investigating periods where customer activity declines.
- Supporting customer engagement and retention initiatives.
- Monitoring customer performance over time.

The results can support further investigation into customer behavior, but business recommendations should be based on validated metric definitions and the underlying data.

📚 Key Power BI Concepts Demonstrated

- DAX calculated columns
- DAX measures
- First-purchase and cohort-date logic
- Period calculations
- Field parameters
- Matrix visualizations
- Conditional formatting
- Customer-count analysis
- Percentage-based performance analysis
- Interactive report design

🚀 Future Improvements

- Document the complete DAX formulas and their logic.
- Validate the percentage measure and its denominator.
- Add KPI cards for key cohort metrics.
- Add slicers for relevant business dimensions.
- Include a written summary of validated insights and recommendations.
- Improve the report with additional cohort comparisons where the dataset supports them.

📂 Project Files

- "Source Dataset" (data/cohort_orders_dataset.xlsx)
- "Power BI Report" (powerbi/cohort_retention_analysis.pbix)
- "Customer Cohort Screenshot" (screenshots/cohort_customers.png)
- "Percentage Cohort Screenshot" (screenshots/cohort_conversion_rate.png)
- "Dataset Preview" (screenshots/dataset_preview.png)
- "Business Insights" (insights.md)

👤 Author

Data Analyst Portfolio Project

Developed using Microsoft Power BI, DAX, and Excel to explore monthly customer cohorts and customer performance.

---

This project is intended for learning, portfolio development, and demonstrating practical data analytics skills.
