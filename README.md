# Clustering Countries Based on Economic Indicators

This repository demonstrates an unsupervised learning project that groups countries by key economic metrics (inflation, GDP growth, unemployment, interest rates, stock index values) to uncover patterns in global economic performance.

---

## 📂 Repository Structure

```
clustering-countries-economic-indicators/
├── Countries.ipynb        # Main Jupyter notebook with full analysis
├── Data.csv               # Quarterly economic indicators (2010–2023)
├── requirements.txt       # Python dependencies
├── LICENSE                # MIT License
└── README.md              # Project overview and instructions
```

---

## 🚀 Quick Start

1. **Clone this repo**

   ```bash
   git clone https://github.com/muhammederbay10/clustering-countries-economic-indicators.git
   cd clustering-countries-economic-indicators
   ```

2. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

3. **Launch the notebook**

   ```bash
   jupyter lab      # or jupyter notebook
   ```

   Open `Countries.ipynb` and run all cells in order.

---

## 📊 Methodology

1. **Data Loading & EDA**

   * Loaded quarterly data (2010–2023) for 10 countries.
   * Performed summary statistics, missing/duplicate checks, and visualized correlations.

2. **Data Preprocessing**

   * Aggregated each country’s metrics (mean, median, std).
   * Standardized numeric features to zero mean & unit variance.

3. **Dimensionality Reduction (PCA)**

   * Applied PCA to retain 90% of variance (\~3 components).
   * Visualized first two principal components for exploratory insights.

4. **Clustering**

   * **K-Means**: used Elbow & Silhouette methods to evaluate k = 2…10; silhouette peaked at **k = 3** (≈0.44), elbow suggested **k = 4**.
   * **Hierarchical (Ward)**: built dendrogram to choose **k = 4**, achieved silhouette ≈0.48 and balanced cluster sizes.

5. **Cluster Interpretation**

   * Computed per-cluster means of all five indicators.
   * Identified four policy-relevant groups:

     * Cluster 0: Brazil & France (moderate growth, low rates)
     * Cluster 1: Japan & UK (high growth & inflation)
     * Cluster 2: Canada, China, Germany & India (low growth, tight policy)
     * Cluster 3: Australia & USA (mid-growth, higher unemployment)

6. **Choropleth Map**

   * Rendered an interactive world map showing each country’s cluster assignment.

7. **Conclusions & Next Steps**

   * Summarized key takeaways and suggested extensions (additional indicators, time‑series clustering, dashboard).

---

## 🔍 Key Findings

* **Advanced economies** (Japan & UK) are driving recovery with high growth but face structural labor challenges.
* **Emerging markets** (Canada, China, India) maintain lower growth under tighter monetary policy.
* **Middle performers** (Brazil, France) balance moderate expansion with looser rates—ideal candidates for targeted fiscal stimulus.
* **Cyclical markets** (Australia, USA) exhibit headwinds in unemployment and valuations—fiscal and re-skilling measures recommended.

---

## 📑 License

This project is licensed under the **MIT License**. See [LICENSE](License) for details.

---

*Created by Muhammed (2025)*
