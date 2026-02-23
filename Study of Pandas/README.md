# Experiment 9: Tools or EDA - Study of Pandas Library

## 1. Aim
To study and understand the Pandas library in Python for handling structured data, performing Exploratory Data Analysis (EDA), and executing data cleaning tasks.

## 2. Objectives
* To understand the primary data structures in Pandas: Series and DataFrames.
* To learn how to create, inspect, and navigate DataFrames.
* To perform data manipulation, including adding, updating, and deleting columns or rows.
* To apply statistical analysis and conditional filtering on datasets.
* To identify and handle missing data (NaN values) using built-in functions.

---

## 3. Theory

### A. What is Pandas?
**Pandas** (Panel Data) is a core library used for structured data, Exploratory Data Analysis (EDA), and Data Cleaning. It provides high-performance tools for manipulating tabular data.

### B. Core Data Structures
* **Series:** A one-dimensional labeled array, essentially a column in a table.
* **DataFrame:** A two-dimensional, size-mutable tabular data structure with labeled axes (rows and columns).



### C. Key Functionalities
* **EDA:** Using functions like `head()`, `tail()`, and `shape` to quickly understand the dataset's structure.
* **Data Cleaning:** Identifying non-integer or missing numbers (NaN) and handling them to ensure data integrity.
* **Selection & Filtering:** Accessing specific rows or columns using labels (`loc`) or logical conditions.

---

## 4. Algorithms

### 1. Creating and Inspecting a DataFrame
1. Import the `pandas` library as `pd`.
2. Define a dictionary containing keys as column names and lists as data values.
3. Convert the dictionary into a DataFrame using `pd.DataFrame(data)`.
4. Use `df.head()` to view the first few entries and `df.tail()` for the last few.
5. Check metadata using `df.shape` (rows/cols), `df.size` (total elements), and `df.dtypes`.

### 2. Updating and Deleting Data
1. **Add/Update:** Use `df.loc[row_index, "Column"] = value` to modify existing data or `df["New_Column"] = [values]` to add a column.
2. **Delete:** Remove a column using `df.drop("Column_Name", axis=1, inplace=True)`.

### 3. Basic Statistical Analysis
1. Select a numerical column (e.g., `df["Marks"]`).
2. Apply statistical methods: `.mean()` for average, `.mode()` for frequency, and `.min()`/`.max()` for range.

### 4. Conditional Filtering
1. Define a condition (e.g., `df["Marks"] > 80`).
2. Pass the condition into the DataFrame: `df[df["Marks"] > 80]`.
3. This returns only the rows where the condition evaluates to `True`.



### 5. Handling Missing Data (NaN)
1. Use `df.isna()` to generate a boolean table identifying missing values.
2. Use `df.isna().sum()` to count missing values per column.
3. Use `df.dropna()` to remove all rows containing at least one `NaN` value.

---

## 5. Conclusion
Through this experiment, the Pandas library was successfully used to create and manipulate dataframes. We performed data cleaning by identifying and removing null values and gained insights through statistical summaries and conditional filtering.

---

