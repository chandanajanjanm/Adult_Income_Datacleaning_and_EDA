# Adult Income Data Cleaning & Exploratory Data Analysis

## 📌 Project Overview

This project performs data cleaning and exploratory data analysis (EDA) on
the UCI Adult Income dataset.

The objective is to understand which demographic, education, employment,
working-hour, and financial characteristics are associated with annual income
above $50K.

This project focuses on descriptive analysis and does not establish causal
relationships.

---

## 🎯 Business Question

Which demographic, education, and work characteristics are associated with
annual income above $50K in this census dataset?

---

## 📊 Dataset

The project uses the Adult Income dataset from the
UCI Machine Learning Repository.

The original dataset is provided in two partitions:

- `adult.data`
- `adult.test`

After combining both partitions, the dataset contains:

- **48,842 records**
- **15 original variables**

The dataset includes demographic, employment, education, working-hour,
capital, and income information.

---

## 🧹 Data Cleaning

The following data-cleaning steps were performed:

- Combined the training and test partitions
- Standardized column names
- Removed unnecessary whitespace from text values
- Converted `?` missing-value markers to `NaN`
- Replaced missing categorical values with `Unknown`
- Normalized income labels
- Created a binary `high_income` indicator
- Validated numeric data types
- Validated core numeric ranges
- Audited duplicate records

Duplicate records were retained because the dataset does not contain a unique
identifier for individuals.

---

## 🔧 Feature Engineering

The following features were created:

- `source_split` — identifies the original train/test partition
- `high_income` — binary indicator for income above $50K
- `age_group` — grouped age categories
- `hours_group` — grouped weekly working-hour categories
- `net_capital` — capital gain minus capital loss

---

## 📈 Exploratory Data Analysis

The analysis examines income patterns across:

- Sex
- Education
- Occupation
- Workclass
- Age groups
- Weekly working hours
- Capital gain and capital loss
- Numeric variables
- Correlations between numeric variables and income

---

## 🔍 Key Findings

- **76.07%** of records belong to the `<=50K` income group, while **23.93%**
  belong to the `>50K` group.

- Higher education levels generally show a greater proportion of records
  earning above $50K.

- Income distribution varies substantially across occupation categories.

- Income distribution also differs across workclass categories.

- The **46-55 age group** has the highest observed proportion of records
  earning above $50K at **39.24%**.

- The `>50K` income group has a greater representation in higher weekly
  working-hour categories.

- `education_num` has the strongest positive linear correlation with
  `high_income` among the numeric variables examined, with a correlation of
  **0.33**.

- Non-zero capital gain and capital loss are more prevalent among records in
  the `>50K` income group.

---

## ⚠️ Limitations

- The analysis is descriptive and does not establish causation.
- The dataset represents census information from a specific historical period.
- Missing categorical values were grouped as `Unknown`.
- Duplicate records were retained because no unique individual identifier is
  available.
- Income is represented as two categories rather than exact income values.
- Correlation measures only linear relationships between numeric variables.
- Predictive modeling is outside the scope of this project.

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook
- VS Code

---

## 📁 Project Structure

```text
Adult_income_Project/
│
├── data/
│   ├── raw/
│   │   ├── adult.data
│   │   └── adult.test
│   │
│   └── processed/
│       └── adult_income_cleaned.csv
│
├── adult-income.ipynb
├── README.md
└── .gitignore
