# Auto Insurance Claims: A Fraud Analysis

This project looks at 1,000 auto insurance claims to understand claim patterns and how reported fraud differs across categories such as incident severity, incident type, vehicle make and policy state.

## Dataset

The dataset contains 1,000 claims with 40 columns covering customer details, policy information, incident details, claim amounts and whether fraud was reported. It was taken from Kaggle.

## Data Cleaning

* Replaced "?" with missing values and dropped the empty `_c39` column
* Filled missing collision types with "Not Applicable", since they only occurred in parked car and vehicle theft claims
* Labelled missing property damage and police report values as "Unknown"
* Kept "None" in authorities contacted, because it means no authorities were contacted
* Corrected one negative umbrella limit
* Removed one record where the policy start date was after the incident date
* Checked for duplicates (none found) and converted date columns
* Added new columns for customer tenure, incident day, age group and a numeric fraud flag

After cleaning, 999 claims were used for the analysis.

## Key Findings

* The overall fraud rate is 24.7%
* Major Damage claims have the highest fraud rate at 60.5%, far above every other severity level
* Single vehicle and multi vehicle collisions have much higher fraud rates than parked car and theft claims
* Fraudulent claims have higher average injury, property and vehicle claim amounts than genuine claims
* Vehicle claims make up around 72% of the total claim amount for both genuine and fraudulent claims
* Age and annual premium show almost no relationship with claim amount
* Fraud rates are fairly similar across Ohio, Indiana and Illinois

## Tools Used

Python, Pandas, NumPy, Matplotlib, Seaborn, Kaggle Notebooks

## Files

* `EDA_Automotive_Analysis` : the full analysis notebook
* `images/` : charts from the analysis
