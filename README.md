
# Data Cleaning in Pandas

This project demonstrates how to clean and preprocess a customer call list stored in an Excel sheet using **pandas**. The dataset contains various types of errors such as missing values, inconsistent formats, and incorrect data types across multiple fields. This project focuses on transforming the raw data into a cleaned and structured format suitable for analysis.

## Project Overview

The dataset includes the following fields:
- **CustomerID**: Unique identifier for each customer.
- **First_Name**: Customer's first name.
- **Last_Name**: Customer's last name.
- **Phone_Number**: Contact number of the customer, often found in different formats or with special characters.
- **Address**: Full address of the customer, which may contain inconsistencies or require splitting into components.
- **Paying_Customer**: A boolean field indicating whether the customer has made payments.

The goal of this project is to:
- Identify and correct errors in the data.
- Standardize inconsistent formats.
- Remove or handle missing values.
- Ensure the data is structured and cleaned for further analysis or reporting.

## Steps Performed

1. **Data Import**:
   - Loaded the customer call list from an Excel file into a pandas DataFrame.
   
2. **Data Exploration**:
   - Reviewed the structure of the dataset, checked for missing values, and observed the types of errors present (e.g., invalid phone numbers, incorrect casing in names, extra spaces in addresses).

3. **Data Cleaning**:
   - **Missing Values**: Handled missing values by either filling with appropriate values or dropping records, depending on the field.
   - **String Formatting**:
     - Standardized customer names (First_Name and Last_Name) to proper casing (e.g., `john` to `John`).
     - Removed special characters and spaces from the `Phone_Number` field to create a consistent numeric format.
   - **Address Formatting**: Split the address field into multiple components (`Street Address`, `City`, `State`, `Zip_Code`) where necessary, and cleaned up whitespace.
   - **Data Type Correction**: Ensured fields like `CustomerID` are integers and `Paying_Customer` is a boolean.
   
4. **Error Handling**:
   - Identified and corrected erroneous or outlier data, such as phone numbers with invalid lengths and duplicate records.

5. **Exporting Cleaned Data**:
   - After cleaning, the processed dataset was exported back to an Excel or CSV file for further use or analysis.

## Tools Used
- **Python**: For scripting and data manipulation.
- **Pandas**: The main library used for data cleaning and transformation.
- **Jupyter Notebook**: To document and visualize the data cleaning process.
- **Excel/CSV**: Source of the input dataset and format for saving the cleaned data.

## How to Run the Project

1. Clone the repository:
   ```bash
   git clone https://github.com/firdoush01/Data_Cleaning_in_Pandas.git
   ```
   
2. Install the required libraries:
   ```bash
   pip install pandas
   ```
   
3. Place your Excel file with the customer call list in the project directory.

4. Run the Jupyter Notebook or Python script:
   ```bash
   jupyter notebook
   ```
   or 
   ```bash
   python data_cleaning.py
   ```

## Future Enhancements

- Automate the process to handle a wide variety of input formats.
- Extend the cleaning process to handle more complex datasets with additional fields.
- Integrate data validation for real-time feedback during data entry.

## Conclusion

This project highlights the importance of data cleaning in any data analysis pipeline. Using pandas, we were able to efficiently clean and prepare customer data, making it ready for future use in marketing, sales, or customer service initiatives.
