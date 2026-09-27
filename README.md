# Retail KPI Data Quality & Profiling

A data analytics project focused on defining business KPIs, profiling retail order data, identifying data-quality issues, and establishing a practical data-quality contract for reliable business reporting.

## 📌 Project Overview

This project analyzes a retail orders dataset to translate business requirements into measurable KPIs and evaluate the reliability of the underlying data.

The project covers:

- KPI definition and documentation
- Data completeness analysis
- Data uniqueness analysis
- Data validity checks
- Data consistency checks
- Data freshness validation
- Data-quality contract creation

## 🎯 Objectives

The main objectives of this project are to:

1. Define measurable business KPIs for retail operations.
2. Identify missing and duplicate records.
3. Detect invalid and inconsistent data values.
4. Establish data-quality rules and acceptable thresholds.
5. Document actions required when quality rules fail.
6. Provide a reliable foundation for KPI reporting and business analysis.

## 📊 KPI Dictionary

The KPI dictionary contains eight business metrics:

| KPI | Description |
|---|---|
| Gross Sales | Total sales value before discounts |
| Net Sales | Sales value after applying order discounts |
| Total Orders | Number of unique customer orders |
| Total Units Sold | Total number of units purchased |
| Average Order Value | Average net sales generated per order |
| Discount Amount | Total monetary discount applied |
| Paid Order Rate | Percentage of orders with Paid status |
| Refund Rate | Percentage of orders marked as Refunded |

Each KPI is documented with its definition, formula, grain, filters, owner, and refresh cadence.

## 🔍 Data Quality Analysis

The profiling notebook evaluates the dataset across five major dimensions.

### 1. Completeness

Identifies missing values in important fields such as:

- `order_date`
- `city`
- `discount_pct`

### 2. Uniqueness

Checks whether `order_id` values are unique.

A duplicate order ID was identified during profiling.

### 3. Validity

Checks whether numerical and categorical values follow defined business rules.

Examples identified during profiling include:

- Negative quantity
- Non-numeric quantity value
- Discount percentage above 100%
- Invalid order date

### 4. Consistency

Checks categorical fields for inconsistent capitalization and formatting.

Examples include:

- `Student` vs `student`
- `Paid` vs `paid`

### 5. Freshness

Validates the order-date field and identifies invalid or missing dates.

## 📋 Data Quality Contract

The project includes a data-quality contract defining:

- Data-quality rules
- Quality thresholds
- Failure conditions
- Remediation actions
- Escalation procedures

Critical data-quality failures should be investigated and resolved before the affected data is used for KPI reporting.

## 🛠️ Tools & Technologies

- Python
- Pandas
- Google Colab
- Microsoft Excel / WPS Office
- GitHub
- Data Profiling
- Data Quality Analysis
- KPI Documentation

## 📁 Project Structure

```text
retail-kpi-data-quality/
│
├── KPI_Dictionary.xlsx
├── Data_Profiling_Notebook.ipynb
├── Data_Quality_Contract.md
└── README.md
```
```
## 📈 Key Findings

The profiling process identified issues related to:
Missing values
Duplicate order IDs
Invalid quantities
Non-numeric quantities
Invalid discount percentages
Inconsistent categorical values
Invalid or missing order dates

These findings demonstrate why data-quality validation is important before using operational data for KPI reporting and business decisions.

```
## 👨‍💻 Author
Gautam Kumar Dutta
B.Tech Computer Science Engineering
```
