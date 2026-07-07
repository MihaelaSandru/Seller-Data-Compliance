# Seller Data Validation Project

This repository contains a Google Colab notebook designed to validate seller data from a CSV file (`seller_data.csv`) and generate a validation report.

## Project Description
The notebook automates the process of checking key fields in seller data for validity. It identifies missing or invalid entries and compiles a comprehensive report. Specifically, it validates:
- **Business Name**: Ensures the business name is not missing or empty.
- **Email**: Checks for a valid email format.
- **Phone Number**: Verifies that the phone number has a minimum length of 8 digits.
- **Insurance Expiry**: Checks if the insurance has expired or is expiring within 30 days.
- **VAT Number**: Validates the VAT number based on the provided country (if both 'VAT' and 'country' columns are present). It supports validation for UK, DE, FR, IT, ES, NL, BE, and PL. If the 'country' column is missing but 'VAT' is present, it will log a specific issue.

## How to Use
1.  **Upload Data**: Upload your `seller_data.csv` file to the Colab environment.
2.  **Run Cells**: Execute all cells in the notebook sequentially.
3.  **Review Report**: A `seller_validation_report.csv` will be generated, containing `supplier_id` and `Validation_Result` for each entry, indicating whether the data is 'OK' or detailing specific issues.

## Output
The primary output is `seller_validation_report.csv`, which provides a clear overview of the validation status for each seller. The report will be saved directly in your Colab environment.
