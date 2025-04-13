# Best Neighborhood in Pittsburgh - Final Project

## Team Name  
**Squirrel Squad**

## Team Member  
**Elena Tamba** (elt160@pitt.edu)

---

## 🧠 Project Summary  
This project investigates **Stanton Heights** to determine if it is Pittsburgh’s safest and therefore “best” neighborhood, using a data-driven approach. By analyzing real datasets from the [Western Pennsylvania Regional Data Center (WPRDC)](https://data.wprdc.org/), we define and measure “bestness” through public safety indicators: housing stability, arrest records, and police incident reports.

Each dataset was cleaned, normalized, and merged to calculate a composite **Safety Score** for every neighborhood. The project was conducted entirely in Python using Jupyter notebooks and includes data visualizations, reflections, and conclusions based solely on open public data.

---

## 📊 Datasets Used

| Metric             | Dataset Title                | Source |
|--------------------|------------------------------|--------|
| 🏡 Home Value       | Property Value Estimates      | [WPRDC](https://data.wprdc.org/dataset/property-assessments) |
| 🚓 Arrest Records   | Police Arrest Data            | [WPRDC](https://data.wprdc.org/dataset/arrest-data) |
| 🛑 Fire Incidents | Fire Reports        | [WPRDC](https://data.wprdc.org/dataset/police-blotter) |

Each dataset was analyzed individually and then aggregated using a simple, equal-weighted average to create a final **Safety Score** for each neighborhood.

---

## ⚙️ Methodology

To ensure fairness across datasets with different scales, we used the following normalization and scoring method:

```python
Safety_Score = (Norm_Homes + Norm_Arrests + Norm_Incidents) / 3
