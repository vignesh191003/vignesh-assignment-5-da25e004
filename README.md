# DA5401 Assignment 5: Visualizing Data Veracity Challenges in Multi-Label Classification

This repository contains the notebook [`da25e004_Assignment_5.ipynb`](da25e004_Assignment_5.ipynb) by Vignesh Babu JS (Roll: DA25E004), which performs a visual audit of the Yeast dataset—a benchmark for multi-label classification—focusing on data veracity challenges and manifold learning techniques.

## Notebook Overview

### Objective

The goal of the notebook is to uncover and visualize veracity issues (such as class imbalance and label interdependencies) in the Yeast multi-label dataset using advanced dimensionality reduction and visualization techniques.

### Walkthrough

#### 1. Data Ingestion and Initial Profiling

- **Data Loading:** Loads the Yeast dataset (`yeast.arff`) and splits it into feature and label matrices.
- **Shape Summary:** Reports the shape of feature (2417 samples × 103 features) and label (2417 samples × 14 labels) matrices.
- **Label Cardinality Analysis:** Visualizes the frequency of each gene function label using a barplot, highlighting class imbalance.

#### 2. Label Interdependency Analysis

- **Label Interdependency Heatmap:** Computes and displays a heatmap of label co-occurrences, revealing frequent multi-label associations and complex label "networks."

#### 3. Simplified Color-Coding Scheme

- **Category Simplification:** Collapses the 14-label multi-labels into a few interpretable categories:
  - Top two most frequent single-label classes
  - Most common multi-label combination
  - All other combinations
- **Category Distribution Visualization:** Shows the distribution of these simplified categories for further analysis.

#### 4. Feature Normalization

- **Standardization:** Applies zero-mean, unit-variance normalization to the feature matrix for improved modeling and visualization.

#### 5. Visual Investigation with Non-Linear Embeddings

- **t-SNE Embeddings:** Projects the high-dimensional data into 2D using t-SNE with varied perplexity values to explore the effect of local/global structure.
  - Comparative scatterplots and KDE overlays illustrate the separability and overlap of simplified categories.
- **Perplexity Selection:** Justifies the choice of perplexity for optimal visualization of clusters.

#### 6. (Further sections may include) Isomap and PCA Embeddings, Classifier Experiments, or Additional Audits

## How to Run

1. Install required Python packages:
    - `numpy`, `pandas`, `scipy`, `scikit-learn`, `matplotlib`, `seaborn`
2. Place `yeast.arff` in the notebook’s working directory.
3. Open and run all cells in `da25e004_Assignment_5.ipynb`.

## Key Insights

- **Class imbalance** and **label correlation** are major veracity challenges for multi-label genomic datasets.
- **Manifold learning** (t-SNE, Isomap, PCA) provides powerful tools to visually audit dataset structure and reveal underlying data quality issues.

## Author

- **Vignesh Babu JS**
- **Roll:** DA25E004

---

For any issues or questions, please open an issue or discussion in this repository.