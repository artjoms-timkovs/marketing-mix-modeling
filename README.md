# Marketing Mix Modeling for The SED Architecture

This repository demonstrates a framework for **Marketing Mix Modeling (MMM)** using Python.
It serves as a proof-of-concept for moving beyond deterministic (pixel-based) attribution toward probabilistic measurement.

### 📉 The Problem
Traditional attribution (GA4, Facebook Ads) relies on cookies and clicks. This introduces **Selection Bias**—overvaluing bottom-of-funnel channels (like Search) and undervaluing demand generation (like TV or Social).

### 📐 The Solution (Methodology)
We use **Ordinary Least Squares (OLS) Regression** to mathematically estimate the contribution of each media channel to total revenue, controlling for external factors like Seasonality.

The formula:
$$Revenue = \alpha + \beta_1(TV) + \beta_2(Social) + \beta_3(Search) + \beta_4(Seasonality) + \epsilon$$

### 🛠 Tech Stack
* **Python**: Core logic
* **Pandas**: Data manipulation
* **Seaborn/Matplotlib**: Visualization (Correlation Heatmaps)
* **Scikit-Learn**: Linear Regression modeling

### 🚀 How to use
1. Open `mmm_analysis.ipynb` to view the logic and outputs.
2. The `data.csv` contains dummy data for demonstration purposes.

---
**Note:** In a production environment (The SED Architecture), this model runs on BigQuery ML with live data ingestion and utilizes Adstock/Diminishing Returns transformations.
