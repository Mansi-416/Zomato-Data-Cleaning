# Zomato Restaurant Dataset — Data Cleaning and Preprocessing

## Project Overview
This project focuses on cleaning and preparing the Zomato Restaurant Dataset using Python. The goal is to identify and handle common data-quality issues before performing exploratory data analysis (EDA).

## Objectives
- Inspect the dataset's structure and data types.
- Identify missing values and handle them appropriately.
- Check for duplicate records.
- Clean text fields by removing leading and trailing spaces.
- Convert selected columns to numeric data types.
- Standardize binary values such as `0` and `1` to `No` and `Yes`.
- Inspect categorical values for inconsistencies.
- Validate selected numerical fields.
- Save the cleaned dataset for future analysis.

## Dataset
The dataset contains restaurant information such as:
- Restaurant name and ID
- City and locality
- Cuisines
- Average cost for two
- Table booking and online delivery availability
- Price range
- Aggregate rating, rating text, and votes

The original dataset used in this project contains **9,551 rows and 21 columns**. A new `Rating Status` column is added during preprocessing, giving the prepared dataset **22 columns**.

> **Dataset source:** Add the public dataset's original source link here before publishing, if available. Make sure you have permission to redistribute the CSV; otherwise, provide the source link rather than uploading the dataset.

## Tools and Technologies
- Python
- Pandas
- NumPy
- Jupyter Notebook
- Visual Studio Code

## Data Cleaning Steps
1. **Load and inspect data** using `read_csv()`, `head()`, `shape`, `info()`, and `describe()`.
2. **Identify missing values** using `isnull().sum()`.
3. **Handle missing cuisines** by replacing missing values with `Not Specified`.
4. **Check and remove exact duplicates** using `duplicated()` and `drop_duplicates()`.
5. **Clean text fields** by stripping leading/trailing whitespace and converting blank strings to missing values.
6. **Convert numeric columns** such as coordinates, average cost, price range, rating, and votes using `pd.to_numeric()`.
7. **Standardize binary categories** by mapping `0` to `No` and `1` to `Yes` in selected booking/delivery columns.
8. **Inspect categorical values** to identify unexpected labels or formatting.
9. **Add `Rating Status`** to classify restaurants as `Rated` or `Not Rated`, based on `Rating text`.
10. **Validate numerical values** by checking rating and price-range limits and looking for negative costs or votes.
11. **Export the prepared data** to a new CSV file.

## Results
- Original dataset: **9,551 rows × 21 columns**
- Prepared dataset: **9,551 rows × 22 columns**, assuming no rows were removed during cleaning
- Missing `Cuisines` values were replaced with `Not Specified`.
- Exact duplicate records were checked; none were found in the original dataset.
- Selected numeric columns were converted to numeric types.
- Selected `0`/`1` categories were standardized to `No`/`Yes`.
- A `Rating Status` column was added.
- Validation checks were performed on selected numeric fields.

Results should be verified by running the notebook against the exact dataset version in this repository.

## How to Run
1. Clone or download this repository.
2. Make sure Python is installed.
3. Install the required libraries:

   ```bash
   pip install pandas numpy jupyter
   ```

4. Open the notebook in Jupyter Notebook or Visual Studio Code.
5. Place the original CSV in the notebook's working directory, or update the file path in the notebook.
6. Run the cells in order.
7. The cleaned dataset is exported as `Zomato_Restaurant_Dataset_Cleaned.csv`.

## Repository Structure
```text
zomato-data-cleaning/
├── README.md
├── Zomato_Data_Cleaning.ipynb
├── Zomato Restaurant Dataset.csv
└── Zomato_Restaurant_Dataset_Cleaned.csv
```

Adjust the filenames above to match the files you actually commit. Do not commit the dataset unless its license or source terms permit redistribution.

## Skills Demonstrated
- Data inspection and profiling
- Missing-value handling
- Duplicate detection
- Text cleaning and categorical standardization
- Data-type conversion
- Data validation
- CSV export with Pandas

## Next Steps
- Perform exploratory data analysis (EDA).
- Explore restaurant distributions by city and cuisine.
- Analyze ratings and price ranges.
- Visualize online-delivery and table-booking patterns.

## Author
**Mansi Jain**

This project was completed as a practical exercise in Python-based data cleaning and preprocessing.
