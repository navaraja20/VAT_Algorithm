# VAT_Algorithm
This repository contains a Python implementation of the Visual Assessment of Tendency (VAT) algorithm, a powerful tool for visualizing cluster tendency in datasets. The VAT algorithm reorders a dissimilarity matrix to reveal potential cluster structures through visual inspection of the resulting ordered dissimilarity image.

Key features of this implementation:

Complete VAT Pipeline: Handles data preprocessing, dissimilarity matrix computation, optimal reordering, and visualization

Data Type Support: Works with both numerical and categorical data (via automatic preprocessing)

Distance Metrics: Supports both Euclidean and geodesic (manifold) distances for non-linear data

Efficient Computation: Includes subsampling for large datasets

Publication-Quality Visualization: Produces side-by-side comparisons of original and ordered matrices

The implementation matches the format described in the original VAT papers and includes test cases demonstrating its application to various dataset types.

# Visual Assessment of Tendency (VAT) Algorithm

![VAT Example Visualization] ![image](https://github.com/user-attachments/assets/118cd233-306e-4e52-b036-128ba1e10f29)


Python implementation of the Visual Assessment of Tendency (VAT) algorithm for assessing cluster tendency in datasets.

## Features

- Complete VAT pipeline from raw data to visualization
- Handles both numerical and categorical data
- Automatic detection of linear vs non-linear data structures
- Geodesic distance computation for manifold data
- Efficient subsampling for large datasets
- Publication-ready visualizations

## Installation

bash
--pip install numpy pandas matplotlib scipy scikit-learn

The repository includes several test cases demonstrating VAT on different dataset types:

Synthetic Data: Circular and linear patterns

Standard Datasets: IRIS dataset

Mixed Data: Numerical and categorical features

Large Datasets: With automatic subsampling


