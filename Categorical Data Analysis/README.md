

# 📊 CATEGORICAL DATA ANALYSIS USING PYTHON

**Name:** Harshit  
**PRN:** 25070123053  
**Batch:** A-3  

---

## 📄 Title Page

- **Experiment Name:** Categorical Data Analysis using Python  
- **Purpose:** Study and analysis of categorical data using Python and Pandas  
- **Language:** Python  

---

## 🎯 Aim of the Experiment

The aim of this experiment is to analyze categorical data using Python by applying different data analysis techniques such as:

- Frequency count  
- Unique values analysis  
- Cross tabulation  
- Percentage distribution  
- Filtering  
- Grouping  
- Sorting  

using the **Pandas library**.

---

## 📌 Introduction

Categorical data refers to data that can be divided into specific groups or categories.

Examples include:
- Product category  
- Payment method  
- Customer type  
- Gender  
- Department  
- Grade  

Python provides powerful tools for analyzing categorical data using the **Pandas library**, which allows easy manipulation, summarization, and exploration of datasets.

---

## 📖 Study of Categorical Data Analysis (Instructions)

1. Create a dataset containing categorical variables  
2. Import the Pandas library  
3. Load data into a DataFrame  
4. Perform frequency analysis  
5. Identify unique values in categorical columns  
6. Perform cross-tabulation between variables  
7. Analyze percentage distribution  
8. Apply filtering, grouping, and sorting operations  

---

## 🔑 Key Concepts

| Function | Description |
|----------|------------|
| `DataFrame()` | Creates a 2D labeled data structure |
| `value_counts()` | Returns count of unique values |
| `nunique()` | Returns number of unique values |
| `crosstab()` | Computes cross-tabulation |
| `groupby()` | Groups data |
| `sort_values()` | Sorts data |
| `read_csv()` | Reads CSV file |

---

## 📘 Theory (Categorical Data Analysis)

### 1. Frequency Count
Determines how many times each category appears.

```python
df['Category'].value_counts()
````

### 2. Unique Values

Displays all distinct values in a column.

```python
df['Category'].unique()
```

### 3. Number of Unique Values

Calculates total unique categories.

```python
df['Category'].nunique()
```

### 4. Cross Tabulation

Compares two categorical variables.

```python
pd.crosstab(df['Category'], df['Payment_Method'])
```

### 5. Percentage Distribution

Shows percentage share of each category.

```python
df['Category'].value_counts(normalize=True)*100
```

### 6. Filtering Data

Extracts rows based on conditions.

```python
df[df['Category'] == 'Electronics']
```

### 7. Grouping Data

Analyzes relationships between variables.

```python
df.groupby('Category')['Payment_Method'].value_counts()
```

### 8. Sorting Data

Sorts dataset based on a column.

```python
df.sort_values(by='Order_ID')
```

---

## 📊 Dataset Used

### 📁 Dataset 1: Order Dataset

Contains:

* Order ID
* Category
* Payment Method
* Delivery Type
* Customer Type

Used for:

* Sales analysis
* Payment behavior
* Delivery preferences

---

### 📁 Dataset 2: Student Dataset

Contains:

* Student
* Gender
* Department
* Grade

Used for:

* Academic analysis
* Gender distribution
* Department-wise performance

---

## 📊 Key Observations

### 🔹 Dataset 1 Insights

* Electronics is the most frequent category (40%)
* UPI is the most used payment method
* Equal distribution of new and returning customers
* Equal distribution of express and standard delivery

### 🔹 Dataset 2 Insights

* Grade B is the most common
* Equal gender distribution (Male = Female)
* CSE has the highest number of students
* Grade distribution varies across departments

---

## 🛠 Tools Used

* Python
* Pandas Library
* Jupyter Notebook / Google Colab / VS Code

---

## 📂 Applications of Categorical Data Analysis

* Business sales analysis
* Customer behavior analysis
* Market research
* Academic performance analysis
* Data-driven decision making

---

## 🎯 Conclusion

Categorical data analysis is an important technique in data science.

Using Python and Pandas, we can:

* Analyze categorical variables efficiently
* Identify patterns
* Generate meaningful insights

This experiment demonstrated key techniques such as:

* Frequency analysis
* Cross tabulation
* Grouping
* Filtering

which are essential for real-world data analysis.

---

## 📎 Extra Notes

* Pandas provides powerful tools for categorical analysis
* Cross-tabulation helps compare variables
* Grouping gives deeper insights
* Data analysis supports better decision making

---

## 🙌 THANK YOU

```
```

