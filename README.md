# Sales Data Cleaning and CSV Manipulation

A beginner-friendly Python project that uses Pandas to clean a sales
dataset, calculate revenue, create charts, and update a separate CSV
file.

## Project overview

This project has two parts:

-   **Part A: Data Quality and Basic Insights** - inspect the original
    data, clean common data-quality issues, calculate revenue, group
    sales, and create two charts.
-   **Part B: CSV File Handling and Manipulation** - calculate 5% tax,
    increase Books prices by 10%, remove one selected transaction, and
    save the updated CSV.

## Project files

  -----------------------------------------------------------------------
  File                                Description
  ----------------------------------- -----------------------------------
  `sales_raw.csv`                     Original input dataset. The
                                      notebook does not overwrite it.

  `Sales_Data_Project.ipynb`          Notebook containing the Part A and
                                      Part B code.

  `cleaned_sales.csv`                 Cleaned data with a `revenue`
                                      column.

  `sales_updated.csv`                 Updated data with `revenue` and
                                      `tax_amount`.

  `revenue_by_region.png`             Chart of revenue by region.

  `revenue_by_category.png`           Chart of revenue by category.
  -----------------------------------------------------------------------

## Requirements

-   Python 3
-   Jupyter Notebook or Google Colab
-   Pandas
-   NumPy
-   Matplotlib

## How to run

1.  Download or clone this repository.

2.  Keep `Sales_Data_Project.ipynb` and `sales_raw.csv` in the same
    folder.

3.  Install the required libraries:

    ``` bash
    pip install pandas numpy matplotlib notebook
    ```

4.  Start Jupyter Notebook:

    ``` bash
    jupyter notebook
    ```

5.  Open `Sales_Data_Project.ipynb` and run the cells from top to
    bottom.

You can also upload both the notebook and `sales_raw.csv` to Google
Colab. The notebook uses relative file paths, so it expects the CSV file
in the notebook's working folder.

When the notebook runs, it creates `cleaned_sales.csv`,
`sales_updated.csv`, `revenue_by_region.png`, and
`revenue_by_category.png`. The original `sales_raw.csv` remains
unchanged.

## Data cleaning rules

The notebook follows these rules:

1.  Removes extra spaces and standardizes the text in the `region` and
    `category` columns.
2.  Replaces missing region names with `Unknown`.
3.  Converts the date, quantity, and unit-price columns to suitable data
    types.
4.  Removes exact duplicate rows.
5.  Treats zero or negative quantities as invalid and fills missing
    quantities with the median.
6.  Treats invalid prices and unusually high prices as missing values.
7.  Fills missing prices with the median price for the same category. If
    that is not available, it uses the overall median price.
8.  Calculates revenue by multiplying quantity by unit price.

The notebook also explains these choices in the cleaning section.

## Part B operations

-   Adds `tax_amount`, equal to 5% of revenue.
-   Uses `.loc[]` to increase the `unit_price` of Books items by 10%.
-   Recalculates revenue and tax after the price change.
-   Removes the selected transaction with ID `1002`.
-   Creates a temporary `review_status` column and then removes it.
-   Saves the result as `sales_updated.csv`, reads it again, and checks
    the output.

## Results

The notebook displays revenue summaries by region and category, creates
two labelled charts, and includes two findings based on the data.

## GitHub repository

https://github.com/muhammad-ammar-tahir/AI-Engineering-Bootcamp-Module-02

## Author details

-   **Name:** MUHAMMAD AMMAR TAHIR
-   **Training ID:** TRN-2026-003614
-   **Program:** AI Engineering Bootcamp
-   **Module:** Module 02
