# Unsupervised Anomaly Detection in Mixed-Type Data

## Overview
This repository contains the implementation of an anomaly detection project focusing on mixed-type data (binary and continuous variables). The project evaluates and compares four approaches for identifying anomalies in datasets with significant challenges, such as imbalanced binary attributes, skewed continuous distributions, and high dimensionality.

## Project Goals
- Develop and test models to identify anomalies in datasets with mixed data types.
- Analyze anomaly score distributions and evaluate model performance.
- Create and use an artificial dataset with labeled outliers to validate results.

## Dataset
The project uses a dataset with:
- **7200 data points** and **21 attributes** (6 continuous, 15 binary).
- Continuous data normalized to the [0, 1] range.
- A generated dataset for validation, containing 5% labeled outliers.

## Approaches
The following methods were implemented and evaluated:

1. **K-Prototypes Clustering**:
   - Combines K-Means (for continuous data) and K-Modes (for binary data).
   - Detects anomalies based on the distance to cluster centroids.

2. **Information Gain Approach**:
   - Uses entropy changes to identify anomalies.
   - Calculates entropy separately for binary and continuous attributes.

3. **Hybrid Method**:
   - Combines K-Means for continuous attributes and entropy-based detection for binary attributes.
   - Aggregates scores using a weighted average.

4. **Autoencoder**:
   - A neural network model trained to minimize reconstruction error.
   - High reconstruction error indicates anomalies.
