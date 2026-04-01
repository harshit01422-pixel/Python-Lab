
# 📊 Data Normalization and Data Type Conversion in Python

## Name: Harshit

## Branch: EnTC A3

## PRN: 25070123053

---

## 📄 Experiment Title

Data Normalization and Data Type Conversion using Python

---

## 🎯 Objective

The objective of this experiment is to understand and apply data normalization techniques, encoding methods, and data type conversion in Python to prepare datasets for efficient analysis and machine learning.

---

## 📌 Overview

Real-world datasets often contain values in different ranges, inconsistent formats, and categorical data that cannot be directly used for analysis.

* **Normalization** scales numerical data
* **Standardization** centers and normalizes distribution
* **Encoding** converts categorical data into numerical form
* **Type Conversion** ensures proper data formats

These steps are essential for accurate and efficient data processing.

---

## 🧠 Key Concepts

* Data Normalization
* Standardization
* Feature Scaling
* Encoding Techniques
* Data Type Conversion
* Data Cleaning

---

## 📘 Theory

### 🔹 Data Normalization

Normalization scales data into a fixed range, usually **0 to 1**, to ensure fair contribution of all features.

---

### 🔸 Types of Normalization

#### 1. Min-Max Normalization

Scales data between 0 and 1

```
(x - min) / (max - min)
```

**Use Case:**
When data has known bounds

---

#### 2. Z-Score Normalization (Standardization)

Transforms data to have mean = 0 and standard deviation = 1

```
(x - mean) / standard deviation
```

**Use Case:**
When data has outliers or unknown distribution

---

#### 3. Decimal Scaling

Moves decimal point based on maximum value

```
x / 10^n
```

Where *n* is chosen such that values fall between -1 and 1

**Use Case:**
Simple scaling when magnitude is large

---

#### 4. Log Transformation

Applies logarithm to reduce skewness

```
log(x)
```

**Use Case:**
Highly skewed data

---

#### 5. Max Absolute Scaling

Scales values between -1 and 1

```
x / max(|x|)
```

**Use Case:**
Data centered around zero

---

### 🔹 Standardization vs Normalization

| Feature       | Normalization         | Standardization |
| ------------- | --------------------- | --------------- |
| Range         | 0 to 1                | No fixed range  |
| Mean          | Not centered          | Mean = 0        |
| Std Deviation | Not fixed             | Std = 1         |
| Sensitivity   | Sensitive to outliers | Less sensitive  |

---

### 🔹 Encoding Techniques

Encoding is used to convert categorical data into numerical form.

---

#### 1. Label Encoding

Assigns a unique number to each category

Example:
Male → 0, Female → 1

**Use Case:**
Ordinal data

---

#### 2. One-Hot Encoding

Creates separate binary columns for each category

Example:
Red → [1,0,0], Blue → [0,1,0]

**Use Case:**
Nominal data

---

#### 3. Ordinal Encoding

Encodes categories based on rank/order

Example:
Low → 1, Medium → 2, High → 3

---

#### 4. Binary Encoding

Converts categories into binary numbers

**Use Case:**
High cardinality data

---

#### 5. Frequency Encoding

Replaces categories with their frequency

---

#### 6. Target Encoding

Replaces category with mean of target variable

**Use Case:**
Supervised learning

---

### 🔹 Data Type Conversion

Ensures that data is stored in correct formats such as:

* Integer
* Float
* String

Helps avoid errors and improves computation efficiency.

---

## ⚙️ Procedure

1. Import required libraries (Pandas, NumPy)
2. Load dataset into DataFrame
3. Identify numerical and categorical columns
4. Apply normalization techniques
5. Apply encoding methods
6. Convert data types
7. Validate processed data

---

## 📘 Implementation

### Min-Max Normalization

```python
df['Normalized'] = (df['Column'] - df['Column'].min()) / (df['Column'].max() - df['Column'].min())
```

### Standardization

```python
df['Zscore'] = (df['Column'] - df['Column'].mean()) / df['Column'].std()
```

### Decimal Scaling

```python
df['Scaled'] = df['Column'] / 10**n
```

### One-Hot Encoding

```python
pd.get_dummies(df['Category'])
```

### Label Encoding

```python
from sklearn.preprocessing import LabelEncoder
le = LabelEncoder()
df['Category'] = le.fit_transform(df['Category'])
```

### Data Type Conversion

```python
df['Column'] = df['Column'].astype(float)
```

---

## 📊 Dataset Description

The dataset includes:

* Numerical values with different ranges
* Categorical data requiring encoding
* Columns needing formatting and conversion

---

## 🛠 Tools Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Jupyter Notebook / Google Colab / VS Code

---

## 📂 Applications

* Machine learning preprocessing
* Data visualization
* Predictive modeling
* Business analytics

---

## 🔄 Workflow

Load Data → Analyze Data → Normalize Values → Encode Categories →
Convert Data Types → Clean Data → Validate Output

---

## 📋 Key Functions

| Operation       | Function       | Example                 |
| --------------- | -------------- | ----------------------- |
| Normalization   | min(), max()   | (x - min) / (max - min) |
| Standardization | mean(), std()  | (x - mean) / std        |
| Encoding        | get_dummies()  | One-hot encoding        |
| Label Encoding  | LabelEncoder() | Numeric labels          |
| Conversion      | astype()       | df['x'].astype(int)     |

---

## 🎯 Outcome

* Applied multiple normalization techniques
* Converted categorical data using encoding
* Standardized dataset for analysis
* Ensured correct data types

---

## 📝 Key Takeaways

* Different normalization techniques suit different data
* Encoding is essential for categorical data
* Clean and consistent data improves model accuracy
* Always validate transformed data

---

## 📌 Conclusion

Data normalization, encoding, and type conversion are fundamental preprocessing steps in data analysis.
They ensure that datasets are structured, consistent, and ready for machine learning and statistical applications.

---

## ✨ Thank You

---

If you want next, I can also make a **very short 1-page exam revision sheet from this** 📄👍
