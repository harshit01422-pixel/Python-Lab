# 🌐 Real-World and Interactive Visualizations

## Name: Harshit
## Branch: EnTC A3
## PRN: 25070123053

---

## 📄 Experiment Title
Advanced Visualizations: Hierarchical, Interactive, and Multi-dimensional Charts

---

## 🎯 Objective
The objective of this experiment is to implement advanced and interactive data visualization techniques using **Plotly**, **SciPy**, and **Matplotlib-Venn**. We aim to represent complex data structures such as hierarchical relationships, flow processes, and multi-dimensional skill sets.

---

## 📌 Overview
Standard 2D charts are often insufficient for modern data storytelling. This experiment explores:
* **Interactive Plots:** Using **Plotly** to allow users to hover, zoom, and rotate data.
* **Hierarchical Data:** Visualizing nested structures and clusters.
* **Process Flow:** Tracking how data moves from one stage to another.
* **Set Theory:** Visualizing intersections between different groups.

---

## 🧠 Key Concepts

### 1. Treemap
Uses nested rectangles to display hierarchical data. The size of each rectangle is proportional to its value.
* **Use Case:** Company budget distribution or disk space usage.

### 2. Dendrogram
A tree-like diagram that records the sequences of merges or splits in **Hierarchical Clustering**. It helps determine the optimal number of clusters in a dataset.


### 3. Sankey Diagram
A flow diagram in which the width of the arrows is proportional to the flow rate.
* **Use Case:** Student progression (Admission → Year 1 → Placement) or energy consumption flows.


### 4. Radar (Spider) Chart
A graphical method of displaying multivariate data in the form of a two-dimensional chart of three or more quantitative variables represented on axes starting from the same point.
* **Use Case:** Employee skill assessment or athlete performance profiles.

### 5. 3D Scatter Plot
Adds a third spatial dimension ($Z$-axis) to a standard scatter plot, allowing for the analysis of three numerical variables simultaneously.

---

## ⚙️ Procedure
1.  **Library Installation:** Import specialized libraries: `plotly.express`, `scipy.cluster.hierarchy`, and `matplotlib_venn`.
2.  **Hierarchical Analysis:** Use `linkage` and `dendrogram` to perform and visualize clustering on a coordinate-based array.
3.  **Interactive 3D Modeling:** Create a 3D Scatter plot to analyze the relationship between Study Hours, Marks, and Attendance.
4.  **Flow Visualization:** Construct a Sankey diagram using `graph_objects` to map the student journey through college.
5.  **Skill Profiling:** Map a student's proficiency across various technical domains using a Radar chart.

---

## 📘 Implementation Highlights

### 3D Scatter Plot with Plotly
```python
fig = px.scatter_3d(df, x='Study_Hours', y='Marks', z='Attendance')
fig.show()
```

### Hierarchical Clustering (Dendrogram)
```python
from scipy.cluster.hierarchy import dendrogram, linkage
linked = linkage(data, method='ward') # 'Ward' minimizes variance within clusters
dendrogram(linked)
```

### Flow Mapping (Sankey)
```python
fig = go.Figure(data=[go.Sankey(
    node=dict(label=["Admission", "First Year", "Second Year", "Placed"]),
    link=dict(source=[0, 1, 2], target=[1, 2, 3], value=[100, 80, 60])
)])
```

---

## 📋 Key Functions Used

| Function | Library | Purpose |
| :--- | :--- | :--- |
| `px.treemap()` | Plotly Express | Visualizes hierarchical proportions |
| `linkage()` | SciPy | Performs hierarchical/agglomerative clustering |
| `venn2()` | Matplotlib-Venn | Shows intersections between two sets |
| `go.Sankey()` | Plotly Graph Objects | Visualizes flow and quantity between nodes |
| `go.Scatterpolar()`| Plotly Graph Objects | Creates Radar/Spider charts |
| `px.scatter_3d()` | Plotly Express | Interactive 3D point visualization |

---

## 📂 Applications
* **Education Tech:** Tracking student retention and progression through Sankey diagrams.
* **HR Analytics:** Radar charts for "Spider-web" skill gap analysis during hiring.
* **Finance:** Treemaps for visualizing portfolio allocation across different sectors.
* **Biology:** Dendrograms for species classification and genetic similarities.

---

## 🎯 Outcome
* Successfully transitioned from static plots to **dynamic, interactive dashboards**.
* Gained the ability to visualize **non-linear data** (flows, sets, and hierarchies).
* Learned to represent **higher-dimensional data** (3D and Polar coordinates).
* Improved data storytelling capabilities for real-world business and engineering scenarios.

---

## 📌 Conclusion
Interactive and specialized visualizations like Sankey diagrams and 3D plots provide a much deeper level of insight than standard bar or line charts. By utilizing libraries like Plotly and SciPy, we can create sophisticated models that are both scientifically rigorous and visually engaging for end-users.

---

## ✨ Thank You
