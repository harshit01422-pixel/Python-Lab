
---

# 🦠 COVID-19 Intelligence & Global Trends Analysis
### *Exploratory Data Analysis | Experiment 19 & 20*

| 👤 Developer | 🆔 PRN | 🏛️ Batch |
| :--- | :--- | :--- |
| **Harshit** | **25070123053** | **EnTC A3** |

---

## 📄 Abstract
This research project focuses on the computational analysis of the COVID-19 pandemic using the Python scientific ecosystem. By leveraging a multi-dimensional time-series dataset spanning from **January 2020 to May 2021**, the study implements rigorous data cleaning, complex feature engineering, and high-fidelity visualization. The project aims to decode global infection trajectories, identify reporting anomalies, and evaluate healthcare outcomes through localized and global lenses.

---

## 🎯 Project Goals
* **Data Sanitization & Optimization:** Executed a comprehensive cleaning pipeline by removing redundant indices (`SNo`) and administrative timestamps (`Last Update`). Observation dates were cast into `datetime64` objects to unlock time-series indexing and frequency conversion.
* **Epidemiological Feature Engineering:** Beyond raw counts, the project engineers the `Active` case metric and derives normalized ratios, specifically **Mortality Rate %** and **Recovery Rate %**, to enable fair comparisons between nations with vastly different population scales.
* **Interactive Geospatial Mapping:** Leveraged `Plotly Express` to construct dynamic Choropleth maps. These visualizations utilize ISO-alpha country codes and continuous color scales to represent the shifting epicenter of the pandemic across various continents.
* **Temporal Signal Smoothing:** Implemented advanced smoothing techniques using `diff()` and `rolling(7).mean()` to generate 7-day averages. This was critical for filtering out "weekend effects" and reporting lags, providing a true representation of epidemic velocity in India, Brazil, and the US.
* **Regional Hotspot Identification:** Conducted a specialized deep-dive into the province-level distribution within Spain (Experiment 20), utilizing `groupby` and `idxmax()` functions to isolate and visualize sub-national regions with the highest clinical burden.

---

## 🛠️ Technical Toolkit

| Category | Libraries & Tools | Key Functionalities Used |
| :--- | :--- | :--- |
| **Data Science Core** | `Pandas`, `NumPy` | `pivot_table`, `rank`, `reset_index`, Vectorized Math |
| **Static Visualization** | `Matplotlib`, `Seaborn` | Subplots, Heatmaps, Formatting Tickers |
| **Interactive Maps** | `Plotly Express` | `choropleth`, Color-scaling, Location Modes |
| **Workflow** | `Jupyter / Google Colab` | Cell-based execution and inline rendering |

---

## 📊 Methodology & Analytical Highlights

### 1. The Preprocessing Pipeline
The dataset was initially inspected using `.info()` and `.head()` to identify schema inconsistencies. The sanitization phase involved stripping 2nd-order noise and handling null values in the `Province/State` column. Case counts were explicitly cast from floats to 64-bit integers to ensure precision in downstream arithmetic.

### 2. Global Distribution Dynamics (Experiment 19)
By filtering for the absolute latest observation date (May 29, 2021), the project creates a high-resolution snapshot of the pandemic's status. Aggregation via `groupby("Country/Region")` was essential to consolidate sub-national data for accurate national-level reporting.



### 3. Advanced Epidemiological Insights
* **Identification of Reporting Anomalies:** The analysis reveals a significant data artifact where the US exhibits a 0% recovery rate. Research confirms this is due to a shift in national reporting protocols rather than an actual absence of patient recoveries.
* **Epidemic Wave Analysis:** Through the 7-day rolling average technique, the project identifies the precise timing and peak intensity of India’s second wave (April 2021), allowing for a comparative study of wave trajectories against the US and Brazil.
* **Multivariate Correlation:** Using a Seaborn heatmap, a Pearson correlation matrix was generated. It established a near-linear relationship (~0.95) between Confirmed cases and Deaths, while identifying that a country's **Mortality Rate** is more closely tied to local healthcare capacity than absolute case volume.



### 4. Spanish Province Deep-Dive (Experiment 20)
This specialized module focused on Spain, analyzing the internal distribution of cases. By using `.unique()` and `.nunique()`, the study quantified the reporting granularity and produced a targeted choropleth map using the `Magma` color scale to highlight localized infection hotspots.

---

## 🏁 Summary & Future Scope
The experiment demonstrates the power of Python in transforming chaotic public health data into structured, actionable intelligence. By moving beyond raw numbers into **normalized rates** and **smoothed trends**, we gain a clearer understanding of global health crises.

**Future Roadmap:**
* **Vaccination Correlation:** Integrate global vaccination datasets to evaluate the efficacy of rollouts on mortality reduction.
* **Predictive Modeling:** Implement ARIMA or Facebook Prophet models to forecast potential future peaks.
* **Web Dashboard:** Deploy the interactive modules using `Streamlit` or `Dash` for public accessibility.

---

## 📚 References
1. **JHU CSSE** - COVID-19 Public Data Repository.
2. **Pandas & Scikit-Learn** - Technical Documentation.
3. **WHO** - Pandemic Situation Reports and Guidelines.

---

**Submitted by:** Harshit | **PRN:** 25070123053
