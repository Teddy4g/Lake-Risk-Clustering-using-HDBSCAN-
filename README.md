# 🌊 Lake Risk Clustering using HDBSCAN

This project performs **unsupervised clustering on U.S. lake ecosystem data** using **HDBSCAN (Hierarchical Density-Based Spatial Clustering of Applications with Noise)** to identify **high-risk clusters** influenced by agricultural and urban pressures.  
The analysis aims to provide **data-driven insights** into **regional environmental vulnerability**, helping stakeholders understand how human activity impacts water quality and ecological resilience.

---

## 📘 Overview

Lakes are crucial ecosystems that regulate biodiversity and provide resources for agriculture, recreation, and human consumption.  
However, **anthropogenic pressures** — such as **urban expansion** and **intensive agriculture** — can significantly alter their ecological balance.

This project leverages **machine learning clustering (HDBSCAN)** to uncover **patterns of ecological risk** among lakes, classifying them based on multidimensional indicators like:
- Water quality,
- Agricultural activity,
- Urban development,
- And environmental pressure metrics.

---

## 🎯 Objectives

- Identify **natural groupings** among lakes using unsupervised learning.
- Detect **high-risk clusters** with degraded environmental quality.
- Provide **data insights** that can inform sustainable ecosystem management.
- Compare clustering results with **geographical or anthropogenic patterns**.

---

## 🧠 Methodology

### 1️⃣ Data Collection & Preprocessing
- Raw dataset: `data.csv`
- Variables include: lake clarity, agricultural index, urban pressure, connectivity, etc.
- Conducted data cleaning, scaling, and normalization using **pandas** and **scikit-learn**.

### 2️⃣ Clustering Algorithm
- Applied **HDBSCAN** due to its ability to:
  - Detect clusters of varying density,
  - Handle noise/outliers,
  - Avoid manual `k` selection (unlike K-Means).
- Parameter tuning with `min_cluster_size` and `min_samples`.

### 3️⃣ Evaluation
- Compared with **K-Means** and **DBSCAN** to assess robustness.
- Evaluated results using:
  - **Silhouette Score**
  - **Cluster Stability**
  - **Visualization (PCA / t-SNE projections)**

### 4️⃣ Visualization
- Cluster mapping using **Matplotlib** and **Seaborn**.
- Heatmaps, scatter plots, and cluster profiles to interpret ecosystem differences.

---

## 📊 Files Description

| File | Description |
|------|--------------|
| `Lake Clustering.ipynb` | Main notebook with full analysis pipeline |
| `data.csv` | Processed dataset of U.S. lakes with environmental indicators |
| `DSC_Data_Entering_compressed.pdf` | Presentation slides summarizing project background, methodology, and results. |
| `README.md` | Project documentation |

---

## 🧰 Tech Stack

| Category | Tools |
|-----------|-------|
| **Language** | Python |
| **Libraries** | pandas, numpy, matplotlib, seaborn, scikit-learn, hdbscan |
| **Environment** | Jupyter Notebook |
| **Visualization** | PCA & t-SNE dimensionality reduction |
| **Version Control** | Git + GitHub |

---

## 🧩 Key Results

- HDBSCAN successfully identified **10 clusters** with varying ecological risk.
- **Cluster 2** showed the **highest vulnerability**, characterized by:
  - Low water clarity,
  - High agricultural intensity,
  - Dense urban surroundings.
- Visualization confirmed a clear **gradient between natural and disturbed ecosystems**.

> 🧭 These insights highlight the link between land use and lake ecosystem health, providing a foundation for sustainable management strategies.

---

## 🧪 How to Run

```bash
# 1️⃣ Clone the repository
git clone https://github.com/Teddy4g/Lake-Risk-Clustering-using-HDBSCAN-.git
cd Lake-Risk-Clustering-using-HDBSCAN-

# 2️⃣ (Optional) Create virtual environment
python -m venv env
source env/bin/activate  # or env\Scripts\activate on Windows

# 3️⃣ Install dependencies
pip install -r requirements.txt

# 4️⃣ Open Jupyter Notebook
jupyter notebook "Lake Clustering.ipynb"
