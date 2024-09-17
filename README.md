# Text Clustering with Sentence-Transformers

## Project Overview

This repository demonstrates a complete pipeline for text clustering using Sentence-Transformers (SBERT). The project includes text preprocessing, generation of sentence embeddings, and clustering with K-Means and DBSCAN algorithms. It also features visualization techniques for interpreting clustering results and analyzing example texts from each cluster.

## Features

- **Text Preprocessing**:
  - Removal of punctuation and numbers
  - Conversion of text to lowercase
  - Removal of stop words
  - Normalization using stemming or lemmatization

- **Embedding Generation**:
  - Utilizes the `paraphrase-MiniLM-L6-v2` model from Sentence-Transformers for creating embeddings

- **Clustering**:
  - **K-Means**:
    - Fixed number of clusters or determination of the optimal number of clusters
  - **DBSCAN**:
    - Automatic tuning of `eps` and `min_samples` parameters

- **Visualization**:
  - PCA for dimensionality reduction
  - Scatter plots for cluster visualization

- **Cluster Analysis**:
  - Display of sample texts from each cluster

## Getting Started

### Prerequisites

Make sure you have the following Python packages installed:

```bash
pip install sentence-transformers pandas scikit-learn matplotlib seaborn nltk
```

### Data Preparation

1. **Load Data**: Place your dataset files in the `data/` directory.
2. **Preprocess Data**: Apply text cleaning and normalization to prepare data for embedding generation.

### Embedding Generation

1. **Generate Embeddings**: Convert the preprocessed text into embeddings using the SBERT model.
2. **Save Embeddings**: Store the generated embeddings for use in clustering.

### Clustering

1. **K-Means Clustering**:
   - Perform clustering with a specified number of clusters.
   - Optionally, find the optimal number of clusters based on silhouette scores.

2. **DBSCAN Clustering**:
   - Perform clustering with automatically tuned `eps` and `min_samples` parameters.

### Visualization

1. **Visualize Clusters**:
   - Use PCA to reduce dimensionality and plot the clusters.

2. **Review Results**:
   - Analyze clustering results and review example texts from each cluster.

## Folder Structure

- `data/`: Contains input datasets (`train.parquet`, `test.parquet`).
- `results/`: Directory for output files and visualizations.
- `scripts/`: Contains Python scripts for preprocessing, embedding generation, clustering, and visualization.
- `README.md`: Project documentation.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
