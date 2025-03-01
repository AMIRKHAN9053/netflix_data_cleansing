# Netflix Data Preprocessing

## Overview
This repository contains an SQL script for preprocessing and cleaning Netflix dataset. The script handles data inconsistencies, removes duplicates, fills missing values, and performs essential transformations for better analysis. The cleaned data is then used to derive business insights.

## Project Structure
```
Netflix-Data-Preprocessing/
│-- README.md  # Documentation
│-- netflix_preprocessing.sql  # SQL Script for Data Cleaning
│-- netflix_dataset.csv  # Raw Netflix Dataset (if applicable)
```

## Preprocessing Steps
### 1. Database Setup
- Drop existing database (if any) and create a new one.
- Use the newly created database.

### 2. Table Renaming
- Rename the raw dataset table for better readability.

### 3. Handling Duplicates
- Identify duplicate `show_id` entries.
- Remove duplicates using SQL Window functions.

### 4. Handling NULL Values
- Identify missing values in critical columns.
- Populate missing values for `director` and `country` using available data.
- Replace remaining NULLs with `'Not Given'` where applicable.
- Remove rows with NULL values in crucial fields like `Release_Date`.

### 5. Data Transformation
- Extract `release_year` from `Release_Date`.
- Standardize text formatting.
- Drop unnecessary columns like `cast_members` and `description`.

### 6. Final Data Validation
- Ensure no NULL values remain in essential columns.

### 7. Business Queries
- Identify the country with the most content.
- Compare the distribution of Movies vs. TV Shows.
- Retrieve the top-rated content.
- Find the most frequent directors.
- Analyze content additions over time.
- Evaluate age rating distribution.
- Determine the most common duration for movies.

## How to Use
### 1. Clone the Repository
```sh
git clone https://github.com/yourusername/Netflix-Data-Preprocessing.git
cd Netflix-Data-Preprocessing
```

### 2. Run the SQL Script
- Open **MySQL Workbench** (or any SQL client).
- Execute `netflix_preprocessing.sql` step by step.

### 3. Verify the Cleaned Data
Run the following query:
```sql
SELECT * FROM Netflix2021 LIMIT 10;
```

## Insights & Results
- The dataset is **cleaned, structured, and ready** for visualization and further analysis.
- The SQL script efficiently **handles duplicates, missing values, and data inconsistencies**.
- Business queries provide **key insights** about content distribution, ratings, and trends.

## Technologies Used
- **SQL (MySQL)** – Data Cleaning & Preprocessing
- **MySQL Workbench** – Query Execution & Analysis
- **Python (Optional)** – Future Data Visualization



## Contributing
Pull requests are welcome! Feel free to improve or optimize the SQL queries.

