# Smartphone Data Cleaning

This repository contains a Jupyter notebook (`data_cleaning_smartphone_data.ipynb`) that documents the process of cleaning a smartphone dataset (`smartphones.csv`). 

## Data Overview

The original `smartphones.csv` dataset contains 1020 rows and 9 columns of data on various smartphone models.

The columns are:

- `model` - the smartphone model name 
- `price` - the phone's price in Indian Rupees
- `ratings` - the average user rating out of 5 stars
- `sim` - SIM card details (5G, NFC, IR blaster, etc.)
- `processor` - the phone's processor name, cores, and speed
- `ram` - RAM capacity and internal storage capacity  
- `battery` - battery capacity and fast charging details
- `display` - screen size, resolution, and refresh rate
- `camera` - rear and front camera megapixels and features
- `card` - external storage support

## Data Cleaning 

The Jupyter notebook performs the following data cleaning tasks:

- Fix formatting issues:
  - Remove currency symbol and commas from `price`
  - Standardize brand name capitalization in `model`
- Handle missing values:
  - Impute missing `ratings` as the mean rating
- Filter outliers:
  - Remove one suspicious price outlier
- Split columns:
  - Extract 5G, NFC, IR blaster flags from `sim` 
  - Break out processor details from `processor`
  - Separate RAM and internal storage in `ram`
  - Split battery capacity and charging in `battery` 
  - Parse screen details from `display`
  - Get front/rear camera counts from `camera`
- Fix invalid values:  
  - Correct errors in `processor`, `ram`, `battery`, etc. 
  - Standardize OS names in `os`
- Create final cleaned CSV:
  - `smartphone_cleaned_v2.csv` with 24 columns

The notebook documents all data issues found, cleaning steps performed, and results.


