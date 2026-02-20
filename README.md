## Data
- Raw dataset: 12.7 MB
- Clean dataset: 6.7 MB
- Data source: NYC Property Sales Open Data



## Folder structure

nyc-property-sales/
├── data/
│   ├── raw/raw.csv
│   └── clean/clean.csv
├── notebooks/
│   ├── 01_explore.ipynb
│   ├── 02_clean.ipynb
│   └── 03_analysis.ipynb
├── dashboard.pbix
├── requirements.txt
└── README.md



Column	                    Description	                                Data Analyst's Verdict
BOROUGH	            Numeric code (1-5) for the NYC area.	          Keep (Use it to link to your Borough Names).
NEIGHBORHOOD	   Specific area name (e.g., ALPHABET CITY).	      Keep (Crucial for "Drill-down" charts).
ZIP CODE	            5-digit location code.	                  Keep (Essential for Power BI Maps).
RESIDENTIAL UNITS	Number of apartments/homes in the sale.	      Keep (Useful for "Price per Unit" math).
COMMERCIAL UNITS	Number of stores/offices in the sale.	      Keep (Helps identify Mixed-Use buildings).
TOTAL UNITS	            Sum of Res + Comm units.	                      Keep (Good for general building size analysis).
LAND SQUARE FEET	The area of the plot of land ("The Dirt").    Keep (Important for Standalone Houses).
GROSS SQUARE FEET	Total interior building area ("The Space").	  Keep (Your most important metric for price).
YEAR BUILT	           When the structure was finished.	                  Keep (Use to filter "Old vs. New" buildings).
TAX CLASS...	    Tax category at the time of the transaction.	  Keep (Good for verifying the data).
SALE PRICE	        What the buyer paid (Filtered $10k-$10M).	   Keep (Your Y-Axis for almost every chart).
SALE DATE	           The exact day of the sale.	               Keep (The foundation for your time series).
SALE MONTH/YEAR	          Extracted time parts.	                   Keep (Makes building Bar Charts much easier).
MONTH_YEAR	        A string version (e.g., "2025-12").	                   Keep (Perfect for X-Axis labels in Line Charts).
PROPERTY_GROUP	    Your custom group (House, Apartment, etc.).	       Keep (Your main "Slicer" in the dashboard).
TAX_CLASS_NAME	    Cleaned version (Residential vs. Commercial).	   Keep (Highly readable for non-experts).
BUILDING_CAT_FINAL	Final readable category (e.g., "Walk-up").	   Keep (This is the "Star" of your bar charts).

📊 NYC Property Sales Analysis
📌 Overview

This project analyzes New York City property sales data to explore pricing patterns, borough trends, property types, and building characteristics.

The goal of this project was to:

Clean messy real-world real estate data

Perform feature engineering

Conduct exploratory data analysis (EDA)

Prepare structured data for future dashboarding

📂 Data

Raw dataset: 12.7 MB

Clean dataset: 6.7 MB

Source: NYC Property Sales Open Data

The cleaned dataset is generated using 02_clean.ipynb.

🗂 Project Structure
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
🧹 Data Cleaning

Key cleaning steps:

Removed missing ZIP CODE and YEAR BUILT

Converted square footage columns to numeric

Removed formatting issues (commas in numbers)

Converted SALE DATE to datetime

Filtered unrealistic sale prices
(kept transactions between $10,000 and $10,000,000)

Converted ZIP codes to string (for correct categorical handling)

🧠 Feature Engineering

To improve analysis and readability, several new columns were created:

BOROUGH_NAME (mapped from numeric codes)

PRICE_PER_SQFT

PROPERTY_GROUP (House, Apartment, Rental, Land, Commercial)

BUILDING_CATEGORY_FINAL

TAX_CLASS_NAME

SALE MONTH, SALE YEAR, MONTH_YEAR

These features enable clearer comparisons, trend analysis, and category-level insights.

📊 Exploratory Analysis

Analysis includes:

Log-scaled sale price distribution

Borough-level comparisons

Property type comparisons

Price per square foot analysis

Monthly and yearly trend analysis

Boxplots for distribution comparisons

🛠 Tech Stack

Python

Pandas

NumPy

Seaborn

Matplotlib

🎯 What This Project Demonstrates

Ability to clean and structure messy public datasets

Strong feature engineering skills

Practical exploratory data analysis

Understanding of real estate pricing metrics