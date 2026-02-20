## 📊 NYC Property Sales Analysis
# 📌 Overview

This project analyzes New York City property sales data to explore pricing patterns, borough trends, property types, and building characteristics.

The goal of this project was to:

Clean messy real-world real estate data

Perform feature engineering

Conduct exploratory data analysis (EDA)

Prepare structured data for future dashboarding

# 📂 Data

Raw dataset: 12.7 MB

Clean dataset: 6.7 MB

Source: NYC Property Sales Open Data

The cleaned dataset is generated using 02_clean.ipynb.

# 🗂 Project Structure


    nyc-property-sales/
    ├── data/
    │   ├── raw/raw.csv
    │   └── clean/clean.csv
    ├── notebooks/
    │   ├── 01_explore.ipynb
    │   ├── 02_clean.ipynb
    │   └── 03_analysis.ipynb
    ├── requirements.txt
    └── README.md


# 🧹 Data Cleaning

Key cleaning steps:

Removed missing ZIP CODE and YEAR BUILT

Converted square footage columns to numeric

Removed formatting issues (commas in numbers)

Converted SALE DATE to datetime

Filtered unrealistic sale prices
(kept transactions between $10,000 and $10,000,000)

Converted ZIP codes to string (for correct categorical handling)


# 🧠 Feature Engineering

To improve analysis and readability, several new columns were created:

BOROUGH_NAME (mapped from numeric codes)

PRICE_PER_SQFT

PROPERTY_GROUP (House, Apartment, Rental, Land, Commercial)

BUILDING_CATEGORY_FINAL

TAX_CLASS_NAME

SALE MONTH, SALE YEAR, MONTH_YEAR

These features enable clearer comparisons, trend analysis, and category-level insights.



# 📊 Exploratory Analysis

Analysis includes:

Log-scaled sale price distribution

Borough-level comparisons

Property type comparisons

Price per square foot analysis

Monthly and yearly trend analysis

Boxplots for distribution comparisons

## 🛠 Tech Stack

Python

Pandas

NumPy

Seaborn

Matplotlib

# 🎯 What This Project Demonstrates

Ability to clean and structure messy public datasets

Strong feature engineering skills

Practical exploratory data analysis

Understanding of real estate pricing metrics