# Supply_Chain_Analytics-Excess_Inventory_Optimization-Teradyne
Welcome to the Excess Inventory Management System! This project aims to streamline the process of managing excess inventory by analyzing demand and calculating suggested needs and potential excess inventory.

# Table of Contents
- Features
- Getting Started
- Usage
- Functions Overview
- Data Sources
- Contributing
- License

# Features
- Load and clean excess inventory, demand, and part data from Excel files.
- Filter inventory data based on specific date ranges.
- Calculate adjusted dates considering lead times.
- Compute monthly demand and excess inventory.
- Generate detailed reports with suggested need quantities.
- Export results to CSV files for further analysis.

## Getting Started
# Prerequisites
To run this project, you will need the following:
- Python 3.x
- Pandas library
- NumPy library
- Tabulate library
- Access to required Excel files

# Usage
1. Update the excess_inventory_filepath variable in the main_process() function with the correct path to your Excel files.
2. Specify the months you want to analyze in the months list.
3. Run the main process:
   ------ python main.py
4. Check the output CSV files in the specified output directory.

# Functions Overview
'load_clean_data(month, excess_inventory_filepath)'
- Loads and cleans data from specified Excel files.
- Returns cleaned DataFrames for inventory, demand, and part data.
'filter_data_by_date(Inv_df, year, month_num)'
- Filters the inventory DataFrame based on the requested date range.
'adjusted_dates(Inv_df_filtered, LTP_df_filtered)'
- Merges inventory and part data to calculate adjusted dates and lead times.
'demand_calculation(Demand_filtered, merged_df)'
- Calculates monthly demand and potential excess inventory.
'excess_inv_cost(Monthly_Excess, Inv_df, merged_df, month_num, year)'
- Merges monthly excess data with relevant inventory data and prepares the final report.

# Data Sources
This project relies on the following Excel files:
- Excess Inventory Purchase Data
- Demand Data
- Part Data
Make sure these files are correctly formatted and accessible for the scripts to function properly.

# Contributing
Contributions are welcome! If you have suggestions for improvements or find a bug, please open an issue or submit a pull request.

1. Fork the repository
2. Create your feature branch:
------------git checkout -b feature/YourFeature
3. Commit your changes:
-----------------git commit -m "Add your feature description"
4. Push to the branch:
------------------------git push origin feature/YourFeature
5. Open a pull request.
