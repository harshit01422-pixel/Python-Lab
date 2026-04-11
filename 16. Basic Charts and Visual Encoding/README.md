# 📊 Basic Charts and Visual Encoding in Python

## Name: Harshit
## Branch: EnTC A3
## PRN: 25700123053

---

## 📄 Experiment Title
Data Visualization using Matplotlib and Seaborn

---

## 🎯 Objective
The objective of this experiment is to explore basic charting techniques and visual encoding using **Matplotlib** and **Seaborn**. We aim to represent numerical and categorical data through various plots to identify trends, comparisons, and distributions.

---

## 📌 Overview
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand outliers, patterns, and trends in data.

* **Matplotlib:** A low-level library for creating static, interactive, and animated visualizations.
* **Seaborn:** A high-level interface built on top of Matplotlib for drawing attractive and informative statistical graphics.

---

## 🧠 Key Concepts
* **Visual Encoding:** Translating data into visual properties (color, size, shape, position).
* **Trend Analysis:** Using line charts to see changes over time.
* **Categorical Comparison:** Using bar charts to compare discrete groups.
* **Distribution:** Using histograms to see the frequency of values.
* **Correlation:** Using scatter plots to find relationships between two variables.

---

## 📘 Theory & Visualizations

### 1. Line Charts (Trends)
Used to display information as a series of data points called 'markers' connected by straight line segments.
* **Best for:** Visualizing continuity and trends over a period (e.g., Study hours per day).

### 2. Bar Charts (Comparisons)
Represents categorical data with rectangular bars with heights proportional to the values they represent.
* **Grouped Bar Charts:** Useful for comparing multiple variables across categories (e.g., comparing Marks vs. Study Hours for each day).

### 3. Histograms (Distributions)
An approximate representation of the distribution of numerical data. It groups data into "bins" to show frequency.
* **Alpha:** Controls the transparency of the bars.

### 4. Scatter Plots (Relationships)
Uses dots to represent the values obtained for two different numerical variables. 
* **Conditional Encoding:** Assigning different colors to markers based on a category (e.g., Pass/Fail colors) to add a third dimension to the 2D plot.

---

## ⚙️ Procedure
1.  **Environment Setup:** Import `matplotlib.pyplot`, `seaborn`, `pandas`, and `numpy`.
2.  **Data Creation:** Define a dictionary containing student metrics (Days, Marks, Attendance, etc.) and convert it to a Pandas DataFrame.
3.  **Visualization - Matplotlib:**
    * Create basic and advanced line plots with custom markers (`d`, `*`) and linestyles (`-.`).
    * Implement bar graphs with text annotations for exact values.
    * Create a histogram to analyze the frequency of marks.
    * Plot scatter graphs with conditional coloring.
4.  **Visualization - Seaborn:**
    * Load a secondary dataset (Sales/Profit).
    * Demonstrate the streamlined syntax of Seaborn for line, bar, and scatter plots.

---

## 📘 Implementation Highlights

### Customizing Plots (Matplotlib)
```python
# Adding text labels to bars
bars = plt.bar(df['Days'], df['Marks'], color='cyan')
for bar in bars:
    y = bar.get_height()
    plt.text(bar.get_x() + bar.get_width()/2, y, str(y), ha='center', va='bottom')
```

### Grouped Bar Chart
```python
x = np.arange(len(df['Days']))
width = 0.35
plt.bar(x - width/2, df['Study_Hours'], width, label='Study Hours', color='green')
plt.bar(x + width/2, df['Marks'], width, label='Marks', color='red')
```

### Statistical Plots (Seaborn)
```python
sns.lineplot(x='Day', y='Sales', data=df)
sns.scatterplot(x='Sales', y='Profit', data=df)
```

---

## 📋 Key Functions Used

| Function | Library | Description |
| :--- | :--- | :--- |
| `plt.plot()` | Matplotlib | Creates line charts |
| `plt.bar()` | Matplotlib | Creates bar charts |
| `plt.hist()` | Matplotlib | Creates histograms (Distribution) |
| `plt.scatter()` | Matplotlib | Creates scatter plots (Correlation) |
| `plt.legend()` | Matplotlib | Adds a box identifying plot elements |
| `sns.barplot()` | Seaborn | Creates aesthetic bar charts with less code |
| `plt.xticks()` | Matplotlib | Sets the tick locations and labels on the x-axis |

---

## 📂 Applications
* **Academic Performance Tracking:** Comparing study habits with test results.
* **Business Intelligence:** Monitoring sales and profit trends across different regions.
* **Data Science:** Initial exploratory data analysis (EDA) to understand feature behavior.

---

## 🎯 Outcome
* Mastered the ability to plot multiple variables on a single graph.
* Learned to customize plot aesthetics (colors, markers, grids).
* Understood how to use `numpy` to arrange coordinates for grouped charts.
* Successfully utilized Seaborn for cleaner, more readable statistical visualizations.

---

## 📌 Conclusion
Visualizing data is essential for deriving insights that are otherwise hidden in raw tables. This experiment successfully demonstrated how to use Matplotlib for granular control and Seaborn for rapid, high-quality plotting, ensuring a complete toolkit for any data analysis task.

---

## ✨ Thank You
