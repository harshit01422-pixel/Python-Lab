# Experiment 10: Create Dataset and Load Dataset

## 1. Aim
To apply Pandas concepts for creating custom datasets, exporting data to external files, and loading large-scale real-world datasets for comprehensive analysis.

## 2. Objectives
* To create a structured DataFrame from scratch using Python dictionaries.
* To learn how to export DataFrames to CSV format for data persistence.
* To apply data manipulation techniques (adding/dropping columns, filtering) on custom data.
* To load and analyze a real-world external dataset (`Cars93.csv`) using `pd.read_csv()`.
* To utilize `info()` and `describe()` for deep structural and statistical summaries.

---

## 3. Theory: Application of Previous Learning

This experiment serves as a practical synthesis of the concepts studied in the previous two modules (NumPy and Pandas).

### A. From Creation to Persistence
In previous studies, we created DataFrames that existed only in the computer's temporary memory. In this experiment, we utilize the `.to_csv()` function. This bridges the gap between coding and data storage, allowing us to save our work as a permanent file for future use.

### B. Statistical Validation
We apply the statistical operations learned in the NumPy study (Experiment 8)—such as `mean`, `median`, and `mode`—directly to specific Pandas columns. This allows us to find the average CGPA or identify the "topper" in a student dataset.

### C. Real-world Data Analysis
By loading the `Cars93.csv` dataset, we move from small, perfect datasets to larger, real-world data. We apply the "Data Cleaning" concepts from Experiment 9 by using `df.info()` to identify missing values (NaN) in columns like `AirBags` or `Luggage.room`.



---

## 4. Algorithms

### 1. Custom Dataset Creation and Export
1. Define a dictionary where keys represent headers (Roll No, Gender, Dept, CGPA) and values represent the records.
2. Convert this dictionary into a DataFrame using `pd.DataFrame()`.
3. Save the data to a local file using `df.to_csv("student.csv", index=False)`.

### 2. Targeting Specific Information
1. **Row Filtering:** To find a specific student (e.g., Roll No 65), apply a condition: `df[df["Roll No."] == 65]`.
2. **Column Access:** Isolate specific categories using `df["Department"]` or `df["CGPA"]`.

### 3. External Data Loading
1. Use `pd.read_csv('Cars93.csv')` to load the external file into a DataFrame.
2. Use `display(df.head())` and `display(df.tail())` to inspect the first and last five rows of the data.

### 4. Comprehensive Data Summarization
1. Use `df.info()` to view the data type (Dtype) of every column and check for missing (non-null) values.
2. Use `df.describe()` to generate a statistical summary including the mean, standard deviation, and quartiles for all numerical columns like `Price` and `Horsepower`.



### 5. Column Manipulation
1. **Insert:** Add a "Grade" column by assigning a list of values to `df["Grade"]`.
2. **Delete:** Remove unwanted columns (e.g., "Gender") using `df.drop(axis=1, inplace=True)` to streamline the dataset.

---

## 5. Conclusion
This experiment successfully demonstrated the end-to-end process of data handling. We transitioned from manually creating structured data to loading and summarizing large-scale external datasets. This practical application confirmed that the statistical and cleaning methods studied previously are essential for making sense of real-world information.

---

