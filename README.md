
# Adult Income Data Cleaning and Exploratory Data Analysis

## Project Overview

This project performs data cleaning, feature engineering, and exploratory data analysis (EDA) on the UCI Adult Income dataset.

The main objective is to examine demographic, education, employment, and work-related characteristics associated with annual income above USD 50K.

## Dataset

The project uses the UCI Adult Income dataset.

- Total records: 48,842
- Original features: 14
- Target variable: Income
- Income categories: `<=50K` and `>50K`

The raw dataset is divided into training and test files:

- `adult.data`
- `adult.test`

## Project Structure

```text
Adult_income_Project/
│
├── README.md
│
├── data/
│   ├── raw/
│   │   ├── adult.data
│   │   └── adult.test
│   │
│   └── processed/
│       └── adult_income_cleaned.csv
│
├── reports/
│   ├── figures/
│   └── tables/
│
└── src/
    ├── Data Cleaning.ipynb
    └── Data Analysis.ipynb