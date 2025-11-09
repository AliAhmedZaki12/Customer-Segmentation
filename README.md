#  Customer Segmentation System
# App : (https://cusromer-segmentation-l7jwahrko8zxcj8bur5beu.streamlit.app/)

An advanced, research-grade **unsupervised learning pipeline** built to perform intelligent segmentation, automated model selection, and meta-clustering analysis — developed with full **modularity**, **scalability**, and **interpretability** in mind.

---

##  (Project Overview)

This project introduces a comprehensive **Machine Learning framework** designed for **Customer Segmentation** using unsupervised learning techniques.

It automatically:

-  Loads and explores real-world customer datasets (CSV).  
-  Cleans, encodes, and scales mixed data (numerical & categorical).  
-  Reduces dimensionality using PCA for visualization and analysis.  
-  Performs clustering with **KMeans** and **HDBSCAN**.  
-  Evaluates cluster quality using **Silhouette Score**.  
-  Combines multiple clustering outputs into a **Meta-Clustering layer** for deeper, consensus-driven insights.  
-  Generates clear, publication-ready visualizations and exports all processed results to CSV.  

Unlike traditional one-pass clustering scripts, this pipeline emphasizes:

- **Automation** — from preprocessing to evaluation.  
- **Interpretability** — structured workflow and transparent metrics.  
- **Scalability** — supports large and diverse datasets.  
- **Flexibility** — works with both numerical and categorical data automatically.

---

##  (Key Features)

| **Stage** | **Description** |
|------------|----------------|
| **Data Loading** | Reads any CSV dataset and allows column selection for focused analysis. |
| **Exploratory Data Analysis (EDA)** | Generates descriptive statistics, histograms, KDE plots, boxplots, countplots, and correlation heatmaps. |
| **Preprocessing** | Uses `ColumnTransformer` with `SimpleImputer`, `StandardScaler`, and `OneHotEncoder`. Saves the fitted transformer via `joblib`. |
| **Dimensionality Reduction** | Applies PCA (2D) for visualization and variance exploration. |
| **Model Selection** | Tests KMeans (k=2–10) and HDBSCAN configurations; selects the one with the best Silhouette Score. |
| **Meta-Clustering** | Aggregates results from all clustering models using a KMeans meta-model for more stable customer groups. |
| **Visualization** | Displays 2D scatterplots of both best model and meta-clusters. |
| **Output** | Exports results with `BestCluster` and `MetaCluster` columns to `clustered_customers_output.csv`. |

---

##  (Technologies Used)

**Python Version:** 3.10+

**Core Libraries:**
- `pandas`, `numpy`, `seaborn`, `matplotlib`
- `scikit-learn`
- `hdbscan`
- `joblib`

---

##  (How It Works)

1. **Load your customer dataset** (e.g., demographics, purchases, activity, etc.).  
2. The system performs **automated EDA** to reveal patterns and correlations.  
3. **Preprocessing:** missing values handled, categorical encoded, and features scaled.  
4. **Dimensionality Reduction** via PCA (2D) for visualization.  
5. Multiple clustering algorithms (**KMeans**, **HDBSCAN**) are trained and evaluated.  
6. The **best-performing model** is selected using **Silhouette Score**.  
7. **Meta-Clustering** combines clustering outcomes for a unified segmentation view.  
8. Results are **visualized and saved** for business insights or further analytics.

---

##  (Output Files)

| **File** | **Description** |
|-----------|----------------|
| `preprocessor.joblib` | Saved preprocessing pipeline for reuse. |
| `clustered_customers_output.csv` | Final dataset with assigned clusters. |

---

##  (Example Use Cases)

This pipeline can be applied to various business and analytical domains, such as:

-  **Customer Segmentation** for personalized marketing strategies.  
-  **Fraud Detection** or anomaly discovery in financial transactions.  
-  **Product Recommendation** and behavioral grouping.  
-  **Pattern Discovery** in large-scale consumer datasets.

---

## ( Insights )

The system’s core innovation lies in its **meta-clustering strategy**, which blends insights from multiple clustering algorithms to build more consistent and reliable customer segments — revealing deeper behavioral or demographic structures that single models may overlook.

---

##  (Future Improvements)

- Add additional cluster validation metrics (**Davies-Bouldin**, **Calinski-Harabasz**).  
- Extend Meta-Clustering with **Spectral** and **Agglomerative Clustering**.  
- Enable **auto-generation of analytical reports** (PDF/HTML).  
- Optimize processing for **big data** via `MiniBatchKMeans` or **Dask**.

---
