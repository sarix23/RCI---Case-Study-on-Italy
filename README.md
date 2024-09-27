# Regional Competitiveness Analysis: RCI 2.0 2022 in Italy🇮🇹

## Overview

This project aims to analyze the competitiveness of Italian regions by clustering them based on various socio-economic indicators. The analysis highlights regional disparities and identifies key factors contributing to these differences, focusing on a persistent North-South divide.

## Key Points

- **Data Sources**: The analysis utilizes a set of socio-economic indicators relevant to regional competitiveness, distilled down to 31 significant indices after preprocessing from an initial set of 68.
- **Clustering Method**: Mean Shift clustering was employed to categorize regions based on their attributes, with an emphasis on silhouette scores to evaluate the clustering quality.
- **Visualization**: Choropleth maps illustrate the clustering results, where regions are colored according to their cluster affiliation and silhouette values, showcasing areas of strength and weakness.
- **Insights**: The analysis reveals that Northern regions generally outperform Southern regions in various competitiveness dimensions such as technological readiness, infrastructure quality, and labor market efficiency.

## Project Structure

```
/regional-competitiveness-analysis
│
├── data/                 # Contains datasets used in the analysis
├── notebooks/            # Jupyter notebooks with exploratory analysis
├── scripts/              # Python scripts for data processing and analysis
└── results/              # Output results including figures and maps
```

## Key Libraries Used

- `pandas`: For data manipulation and analysis.
- `numpy`: For numerical computations.
- `scikit-learn`: For clustering and machine learning algorithms.
- `geopandas`: For geographical data manipulation and visualization.
- `matplotlib`: For plotting and visualizations.

## Methodology

### 1. Data Preprocessing
- **Missing Values**: Imputed using `KNNImputer`.
- **Standardization**: Data was standardized to prepare it for clustering.

### 2. Clustering
- **Mean Shift Clustering**: Applied to the preprocessed dataset.
- **Silhouette Score Calculation**: Assessed the appropriateness of the cluster assignments.

### 3. Aggregating Scores
- Developed a custom score for each cluster based on the mean of the indicators, weighted by their significance.

### 4. Visualization
- **Choropleth Maps**: Created to visualize regional clusters, colored by silhouette scores using the `viridis` color scale.
- **Bar Plots**: Displayed silhouette scores for each region, colored according to cluster affiliation.

## Conclusion

The analysis confirms significant territorial disparities affecting regional competitiveness in Italy, with key differences between Northern and Southern regions. Future work may focus on deeper regional analyses to guide targeted policy interventions.

## Authors
Giulia Saresini, Sara Nava
