# Layoffs Data Cleaning & Analysis (SQL)

A complete **SQL-based data cleaning project** on a real-world **Layoffs Dataset** (2020–2023). This project demonstrates essential data cleaning techniques using MySQL.

## 📋 Project Overview

This project focuses on cleaning and standardizing a messy layoffs dataset containing information about company layoffs during the COVID-19 period and tech downturn.

### Objectives:
- Remove duplicate records
- Standardize inconsistent data
- Handle missing (NULL) values
- Remove irrelevant columns
- Prepare clean data for analysis

## 🛠 Technologies Used

- **MySQL**
- **SQL** (Data Cleaning & Transformation)
- **CSV Dataset**

## 📊 Dataset

- **File**: `layoffs.csv`
- **Rows**: ~2,000+ records
- **Columns**: Company, Location, Industry, Total Laid Off, Percentage Laid Off, Date, Stage, Country, Funds Raised

## 🔧 Data Cleaning Steps Performed

1. **Removed Duplicates**
   - Used `ROW_NUMBER()` Window Function
   - Created staging table and deleted duplicate rows

2. **Standardized Data**
   - Trimmed whitespace from company names
   - Standardized industry names (e.g., `Crypto%` → `Crypto`)
   - Cleaned country names (removed trailing periods)
   - Converted `date` column to proper `DATE` format

3. **Handled NULL & Blank Values**
   - Populated missing `industry` values using similar companies
   - Removed rows where both `total_laid_off` and `percentage_laid_off` are NULL

4. **Removed Unnecessary Columns**
   - Dropped `row_num` helper column

## 📁 Project Structure

Sql-Project/

├── sql project.sql              # Complete SQL cleaning script

└── layoffs.csv                  # Raw dataset



## 🚀 How to Run

### 1. Clone the repository
```bash
git clone https://github.com/atarek96/Sql-Project.git
cd Sql-Project
