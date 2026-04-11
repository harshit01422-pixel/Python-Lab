# 📈 Statistical and Specialized Data Visualization in Python

## Name: Harshit
## Branch: EnTC A3
## PRN: 25070123053

---

## 📄 Experiment Title
Exploring Statistical and Specialized Data Visualization Techniques

---

## 🎯 Objective
The objective of this experiment is to go beyond basic charts and master specialized plots like **Heatmaps**, **Boxplots**, **Area Plots**, and **Bubble Charts**. These techniques are used to detect outliers, understand correlations, and visualize multi-dimensional data.

---

## 📌 Overview
Statistical visualization allows us to summarize data distributions and relationships. This experiment focuses on:
* **Distribution & Outliers:** Using Boxplots and Histograms.
* **Proportions:** Using Pie and Donut charts.
* **Correlations:** Using Heatmaps to identify how variables move together.
* **Multi-dimensional Data:** Using Bubble plots to represent three or more variables on a 2D plane.

---

## 🧠 Key Concepts

### 1. Area Plot
Similar to a line chart but the area between the axis and the line is filled with color. It is excellent for representing cumulative totals or comparing two magnitudes (e.g., Sales vs. Profit).

### 2. Boxplot (Whisker Plot)
A standardized way of displaying the distribution of data based on a five-number summary: minimum, first quartile (Q1), median, third quartile (Q3), and maximum. It is the primary tool for **outlier detection**.


### 3. Heatmap
A graphical representation of data where individual values contained in a matrix are represented as colors. In data science, it is most commonly used to visualize a **Correlation Matrix**.

### 4. Bubble Plot
An extension of the scatter plot where a third dimension of data is represented through the **size (s)** of the markers. A fourth dimension can be added through **color (c)**.

---

## ⚙️ Procedure
1.  **Library Initialization:** Import `matplotlib`, `seaborn`, `pandas`, and `numpy`.
2.  **Dataset 1 (Categorical):** Create a small dataframe with categories (A-E) to practice proportions and basic specialized plots.
3.  **Advanced Plotting:**
    * Implement **Exploded Pie Charts** to highlight specific categories.
    * Construct a **Donut Chart** by overlaying a circle on a pie chart.
    * Generate a **Heatmap** using the `.corr()` function to see how numerical features relate.
4.  **Dataset 2 (Large Scale):** Generate a synthetic dataset of 100 customers with features like Age, Income, Loan Amount, and Credit Score.
5.  **Statistical Analysis:** Perform outlier detection on loan amounts and visualize credit score frequency using histograms.

---

## 📘 Implementation Highlights

### Correlation Heatmap (Crucial for Feature Selection)
```python
# Calculating correlation and plotting heatmap
corr = df[['Age','Income','Loan_Amount','Credit_Score']].corr()
sns.heatmap(corr, annot=True, cmap='coolwarm')
```


### Donut Chart Logic
```python
plt.pie(df['Values'], labels=df['Category'], autopct='%1.2f%%')
centre_circle = plt.Circle((0,0), 0.4, fc='white') # Create the hole
fig = plt.gcf()
fig.gca().add_artist(centre_circle) # Add hole to the center
```

### Advanced Bubble Plot (Seaborn)
```python
sns.scatterplot(x='Sales', y='Profit', size='Values', hue='Values', data=df, sizes=(50, 300))
```

---

## 📋 Key Functions Used

| Function | Library | Purpose |
| :--- | :--- | :--- |
| `plt.fill_between()` | Matplotlib | Creates Area Plots |
| `plt.pie(explode=...)`| Matplotlib | Highlights specific slices in a Pie chart |
| `sns.boxplot()` | Seaborn | Visualizes quartiles and identifies outliers |
| `.corr()` | Pandas | Generates the correlation matrix for a dataframe |
| `sns.heatmap()` | Seaborn | Visualizes magnitude of correlation through color |
| `plt.Circle()` | Matplotlib | Used to draw the inner circle for Donut charts |

---

## 📊 Dataset Observations
* **Outliers:** The Boxplot allows us to see if any customers have "Loan Amounts" significantly higher than the average.
* **Correlation:** The Heatmap reveals if a high "Credit Score" is positively correlated with "Loan Status" or "Income".
* **Distribution:** The Histogram shows whether "Credit Scores" follow a normal distribution or are skewed.

---

## 🎯 Outcome
* Successfully implemented **multi-dimensional visualization** using Bubble Plots.
* Learned to identify **statistically significant relationships** via Heatmaps.
* Understood how to **clean and validate data** by identifying outliers using Boxplots.
* Mastered aesthetic customizations like `alpha` (transparency) and `palettes` (color schemes).

---

## 📌 Conclusion
Specialized visualizations are vital for professional data storytelling. While basic charts show "what" is happening, statistical plots like Heatmaps and Boxplots explain "why" and "how" variables interact, making them indispensable for exploratory data analysis (EDA) in machine learning.

---

## ✨ Thank You
