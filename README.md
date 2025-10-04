 
**Objective:** Build a modular data pipeline using custom Python functions to extract, transform, aggregate, and load grocery sales data for analytical purposes.

**Tools Used:** Python, pandas, SQL (query execution), and basic file I/O operations.

**1. Data Extraction:**

- A SQL query retrieves raw sales data from a database.

- The result is stored in a pandas DataFrame named grocery_sales.

- The extract() function handles this step (already implemented).

**2. Data Transformation (transform()):**

- Fills missing numerical values using a chosen imputation method (e.g., median).

- Adds a "Month" column derived from the "Date" field.

- Filters rows where "Weekly_Sales" exceeds $10,000.

- Drops unnecessary columns to streamline the dataset.

- Returns a cleaned DataFrame stored as clean_data.

**3. Data Aggregation (avg_weekly_sales_per_month()):**

- Selects "Month" and "Weekly_Sales" columns.

- Groups by "Month" and calculates average weekly sales.

- Applies groupby(), agg(), reset_index(), and round() in a method chain.

- Renames "Weekly_Sales" to "Avg_Sales" for clarity.

- Returns the aggregated DataFrame.

**4. Data Loading (load()):**

- Saves both clean_data and the aggregated data to CSV files (clean_data.csv and agg_data.csv).

- Ensures files are saved without index values.

**5. Validation (validation()):**

- Checks whether the output CSV files exist in the current working directory.

- Confirms successful execution of the pipeline.

