🌍 World Happiness Index — Clustering Analysis (2015–2019)

An unsupervised machine learning project that clusters countries by happiness-related factors across five years of World Happiness Report data.


📌 Project Overview

This project uses K-Means clustering to group countries based on six socioeconomic indicators — GDP per capita, social support, life expectancy, freedom, corruption, and generosity — and tracks how cluster composition shifts from 2015 to 2019.

It does not predict happiness scores. Instead, it discovers natural groupings in the data and interprets what those groupings represent.


📁 Repository Structure

Happiness-Index/
│
├── happiness_clustering.ipynb        # Main notebook (all analysis here)
│
├── 2015.csv                          # Raw data — World Happiness Report 2015
├── 2016.csv                          # Raw data — World Happiness Report 2016
├── 2017.csv                          # Raw data — World Happiness Report 2017
├── 2018.csv                          # Raw data — World Happiness Report 2018
├── 2019.csv                          # Raw data — World Happiness Report 2019
│
├── elbow_silhouette.png              # Elbow + Silhouette plot for choosing k
├── silhouette_plot.png               # Per-sample silhouette analysis
├── pca_clusters_all_years.png        # PCA scatter — all years combined
├── pca_clusters_per_year.png         # PCA scatter — broken down by year
├── cluster_heatmap.png               # Heatmap of cluster feature profiles
├── happiness_dist_clusters.png       # KDE distribution of happiness per cluster
└── cluster_composition_over_time.png # Cluster membership counts by year


🧠 Methods Used

StepTechniqueData cleaningColumn harmonisation across 5 different CSV schemas, median imputation for missing valuesFeature scalingStandardScaler (zero mean, unit variance)Optimal k selectionElbow method (inertia) + Silhouette scoreClusteringK-Means (sklearn.cluster.KMeans)Dimensionality reductionPCA to 2 components for visualisationCluster profilingMean feature values per cluster, KDE distributions


📊 Key Visualisations

Choosing the Right Number of Clusters

Show Image

The optimal k is selected where the silhouette score peaks. The elbow in the inertia curve serves as a sanity check.

PCA Cluster Projection — All Years

Show Image

Countries projected onto 2 principal components. Cluster centroids marked with ✕.

Clusters Per Year

Show Image

How cluster membership shifts year-by-year across the 2015–2019 period.

Cluster Feature Heatmap

Show Image

Standardised mean values per feature for each cluster — shows what defines each group (e.g., high-GDP cluster vs. low-freedom cluster).

Happiness Distribution by Cluster

Show Image

Happiness score density per cluster — confirms that the clusters correspond to meaningfully different happiness levels.

Cluster Composition Over Time

Show Image

How many countries fall into each cluster per year — tracks structural shifts in global happiness patterns.


🔧 How to Run


Clone the repository:


bashgit clone https://github.com/unibril/Happiness-Index.git
cd Happiness-Index


Install dependencies:


bashpip install pandas numpy matplotlib seaborn scikit-learn


Open the notebook:


bashjupyter notebook happiness_clustering.ipynb


Run all cells top to bottom. Output plots will be saved as .png files in the same directory.



📦 Dependencies


pandas
numpy
matplotlib
seaborn
scikit-learn



📂 Data Source

World Happiness Report — annual data from 2015 to 2019, publicly available on Kaggle.


👤 Author
 @unibril
