
# Data Quality Contract

## Dataset
Retail Orders Dataset

## Decision Owner
Head of Sales / Sales Operations Manager

## 1. Completeness
Rule: Required fields should not contain missing values.
Threshold: Maximum 1% missing values.
Failure Action: Flag the dataset for review and notify the data owner.

## 2. Uniqueness
Rule: order_id must be unique.
Threshold: 0 duplicate order IDs.
Failure Action: Duplicate records must be investigated and removed or corrected before KPI reporting.

## 3. Validity
Rule: quantity must be greater than 0.
Threshold: 100% valid quantity values.
Failure Action: Invalid records must be quarantined and corrected.

Rule: discount_pct must be between 0 and 100.
Threshold: 100% valid discount values.
Failure Action: Invalid discount records must be reviewed before reporting.

## 4. Consistency
Rule: Categorical values must use consistent capitalization and approved values.
Threshold: 100% consistency.
Failure Action: Standardize inconsistent values before KPI calculation.

## 5. Freshness
Rule: order_date must be a valid date.
Threshold: 100% valid and non-missing dates.
Failure Action: Records with invalid or missing dates must be investigated before use in reporting.

## Escalation
Any quality rule failure should be reported to the Data Owner / Sales Operations Manager.
Critical failures should block the affected data from KPI reporting until remediation is completed.
