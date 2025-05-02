## CryptoClustering

#Purpose 

In this solo challenge, I used unsupervised learning techniques to analyze and cluster cryptocurrencies based on their 24-hour and 7-day price changes. The objective was to identify groupings and structure in the data using:

K-Means Clustering

PCA (Principal Component Analysis)

hvPlot for interactive visualizations

The project was implemented in Python within a Jupyter Notebook, using data from crypto_market_data.csv.

# How I did it

1. Data Preparation
Loaded and explored the crypto_market_data.csv dataset

Normalized numerical features using StandardScaler

Set "coin_id" as the index of the DataFrame

2. K-Means on Scaled Data
Applied the elbow method to determine the optimal number of clusters (k)

Clustered cryptocurrencies based on:

price_change_percentage_24h

price_change_percentage_7d

Created an interactive hvPlot scatter plot to visualize clusters

3. Dimensionality Reduction with PCA
Applied Principal Component Analysis (PCA) to reduce the data to 3 components

Analyzed the explained variance of the components

Created a new PCA DataFrame containing PC1, PC2, and PC3

4. K-Means on PCA-Reduced Data
Re-applied the elbow method to the PCA-reduced data

Re-clustered the data using K-Means and visualized the results

Compared PCA clustering results with the original scaled clustering

5. Comparison & Discussion
Built composite plots to compare:

Elbow curves (original vs. PCA)

Cluster visualizations (original vs. PCA)

Reflected on the impact of using fewer features with PCA in K-Means clustering

# Findings

- PCA clusters were similarly structured to the original clustering, suggesting that dimensionality reduction preserved the core patterns in the data without major distortion.


# Repository structure

CryptoClustering/
├── Crypto_Clustering.ipynb     => (Main Jupyter notebook with all analysis)
├── Resources/
│   └── crypto_market_data.csv   => (Dataset is placed here)
└── README.md                    => (This file)

# References
- edX Bootcamp Starter Code and Data

- Scikit-learn Documentation

- hvPlot Documentation
