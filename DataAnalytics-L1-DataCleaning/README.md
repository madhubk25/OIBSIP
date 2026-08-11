# Oasis Infobyte — Data Analytics Level 1 — Task 3

## Data Cleaning

### Project Overview

This project demonstrates professional data cleaning techniques using Python, Pandas, NumPy, and Jupyter Notebook.

The objective was to transform a deliberately messy crime incident dataset into a clean, consistent, and analysis-ready dataset while documenting the major cleaning decisions.

### Dataset

The dataset contains 5,250 crime incident records and 33 columns covering:

- Incident details
- Crime type
- District, city, and state
- Geographic coordinates
- Incident date and time
- Officer information
- Suspect information
- Victim information
- Weapon used
- Case severity and status
- Case resolution
- Number of arrests
- Property loss
- Online reporting status
- Incident notes

### Data Cleaning Process

#### 1. Data Quality Assessment

The original dataset was inspected for:

- Missing values
- Duplicate rows
- Incorrect data types
- Range anomalies
- Inconsistent formatting

The original dataset contained **5,250 rows and 33 columns**.

#### 2. Missing Value Handling

Missing values were handled according to the meaning of each column.

- Numerical values were handled using median imputation where appropriate.
- Missing identifiers and names were replaced with `"Unknown"` rather than creating artificial information.
- Missing phone numbers were represented as `"Unknown"`.
- Missing notes were represented as `"No notes available"`.
- Missing incident dates were filled using the median timestamp.

These decisions were documented in the Jupyter Notebook.

#### 3. Duplicate Removal

The dataset contained **200 duplicate rows**.

The duplicate records were removed to prevent repeated incidents from affecting further analysis.

#### 4. Inconsistent Formatting

Inconsistent categorical values were standardised.

Examples:

- `M`, `male`, `MALE` → `Male`
- `F`, `female`, `FEMALE` → `Female`
- `open`, `OPEN`, `Open` → `Open`
- `closed`, `CLOSED`, `Closed` → `Closed`
- `yes`, `Yes`, `YES`, `True`, `1` → `Yes`
- `no`, `No`, `NO`, `False`, `0` → `No`

Crime types were also standardised by correcting obvious spelling errors and equivalent category names.

#### 5. Data Type Correction

Important data types were corrected:

- Incident date/time → datetime
- IDs and badge numbers → string
- Latitude and longitude → numeric
- Ages → numeric
- Number of arrests → numeric
- Property loss → float

#### 6. Outlier Detection and Handling

The **Interquartile Range (IQR)** method was used to identify potential outliers in numerical columns.

Potential outliers were detected in:

- Latitude
- Longitude
- Suspect age
- Victim age
- Number of arrests
- Property loss

Not every IQR outlier was automatically removed because an extreme value can still be valid.

Clearly invalid values were corrected using domain rules, including:

- Ages below 0 or above 100
- Latitude outside -90 to 90
- Longitude outside -180 to 180
- Negative arrest counts
- Negative property loss

Invalid values were replaced using median imputation.

### Before vs After Summary

| Metric | Before Cleaning | After Cleaning |
|---|---:|---:|
| Row Count | 5,250 | 5,050 |
| Duplicate Rows | 200 | 0 |
| Total Missing Values | 12,499 | 0 |
| Data Type Accuracy | Incorrect types present | Correct types applied |

### Final Result

The final cleaned dataset contains:

- **5,050 rows**
- **33 columns**
- **0 missing values**
- **0 duplicate rows**
- Corrected data types
- Standardised categorical values
- Corrected invalid numerical values
- Documented cleaning decisions

The cleaned dataset is ready for further analysis.

### Files

- `crime_incidents_messy.csv` — Original messy dataset
- `cleaned_dataset.csv` — Final cleaned dataset
- `Data_Cleaning.ipynb` — Complete Jupyter Notebook
- `README.md` — Project documentation

### Technologies Used

- Python
- Pandas
- NumPy
- Jupyter Notebook

### Internship

**Oasis Infobyte — Data Analytics Internship**

**Level 1 — Task 3: Data Cleaning**
