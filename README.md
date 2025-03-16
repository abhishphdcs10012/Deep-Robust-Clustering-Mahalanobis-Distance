# Deep Robust Clustering with Mahalanobis Distance (DRCMD)

This repository contains the implementation of robust clustering using Mahalanobis Distance. The project includes experiments on several benchmark datasets.

## Datasets Used

### 1. Pima Indians Diabetes Dataset
- **Source**: UCI Machine Learning Repository
- **URL**: [https://archive.ics.uci.edu/dataset/34/diabetes](https://archive.ics.uci.edu/dataset/34/diabetes)
- **Description**: Dataset of female patients of Pima Indian heritage, containing medical predictor variables and a target variable indicating diabetes diagnosis.
- **Features**: 8 numeric features + 1 binary target
- **Instances**: 768

### 2. Parkinson's Disease Dataset
- **Source**: UCI Machine Learning Repository
- **URL**: [https://archive.ics.uci.edu/ml/datasets/parkinsons](https://archive.ics.uci.edu/ml/datasets/parkinsons)
- **Description**: Biomedical voice measurements from 31 people, 23 with Parkinson's disease (PD).
- **Features**: 22 features (various voice measure attributes)
- **Instances**: 197
- **Citation**: Max A. Little, Patrick E. McSharry, Eric J. Hunter, Lorraine O. Ramig (2008), 'Suitability of dysphonia measurements for telemonitoring of Parkinson's disease'

### 3. Heart Disease Dataset
- **Source**: UCI Machine Learning Repository
- **Description**: Database containing 76 attributes, but all published experiments refer to using a subset of 14 of them.
- **Features**: 14 attributes (13 features + 1 target)
- **Instances**: 303

### 4. Hepatitis Dataset
- **Source**: UCI Machine Learning Repository
- **Description**: Dataset containing information about hepatitis patients
- **Features**: Contains information about symptoms, test results, and patient demographics
- **Instances**: 155

### 5. Ionosphere Dataset
- **Source**: UCI Machine Learning Repository
- **Description**: Radar data collected by a system in Goose Bay, Labrador
- **Features**: 34 continuous attributes + 1 binary class
- **Instances**: 351

### 6. Anemia Dataset
- **Description**: Medical dataset for anemia diagnosis
- **Features**: Contains various blood test parameters and patient information
- **Note**: This appears to be a custom or proprietary dataset. Please ensure proper citation and usage rights.

## Project Structure

```
.
├── T6 ROMD.ipynb          # Main implementation notebook
├── dataset/               # Directory containing all datasets
└── README.md             # This file
```

## Implementation Details

The implementation is based on the paper:
V. Roizman, M. Jonckheere and F. Pascal, "Robust clustering and outlier rejection using the Mahalanobis distance distribution," 2020 28th European Signal Processing Conference, Amsterdam, Netherlands, 2021, pp. 2448-2452, doi: 10.23919/Eusipco47968.2020.9287356.

## Proposed Solution: Deep Robust Clustering with Mahalanobis Distance (DRCMD)

Our proposed solution introduces several key innovations in robust clustering:

### Key Components

1. **Deep Feature Learning**
   - Utilizes deep neural networks to learn robust feature representations
   - Incorporates autoencoder architecture for dimensionality reduction
   - Preserves essential data structure while reducing noise

2. **Robust Mahalanobis Distance**
   - Implements Tyler's robust estimator for covariance computation
   - Accounts for data scale and correlation in distance calculations
   - Provides better handling of high-dimensional data

3. **Adaptive Clustering Mechanism**
   - Dynamic cluster assignment based on robust distance metrics
   - Automatic outlier detection using statistical thresholds
   - Handles varying cluster shapes and densities

### Novel Contributions

1. **Enhanced Robustness**
   - Improved handling of outliers and noise in high-dimensional spaces
   - Better cluster separation in the presence of overlapping distributions
   - Reduced sensitivity to initialization parameters

2. **Automatic Parameter Selection**
   - Data-driven approach to determine optimal number of clusters
   - Adaptive threshold selection for outlier detection
   - Reduced need for manual parameter tuning

3. **Scalability and Efficiency**
   - Efficient implementation for large-scale datasets
   - Parallel processing capabilities for high-dimensional data
   - Reduced computational complexity compared to traditional methods

### Performance Metrics

The algorithm's performance is evaluated using multiple metrics:
- Silhouette Score
- Davies-Bouldin Index
- Adjusted Rand Index (ARI)
- F1 Score
- Hubness Score
- ROC-AUC for outlier detection

### Advantages Over Existing Methods

1. **Robustness**
   - Better handling of noise and outliers
   - More stable cluster assignments
   - Improved performance on real-world datasets

2. **Adaptability**
   - Automatic parameter adjustment
   - Handles varying data distributions
   - Suitable for different application domains

3. **Interpretability**
   - Clear cluster boundaries
   - Meaningful outlier detection
   - Explainable results

## Requirements

- Python 3.x
- NumPy
- Pandas
- Scikit-learn
- Matplotlib
- SciPy

## Usage

The main implementation and experiments can be found in `T6 ROMD.ipynb`. This notebook contains:
- Data loading and preprocessing
- Implementation of robust clustering algorithm
- Outlier detection using Mahalanobis distance
- Visualization and evaluation metrics

## License

Please ensure to cite the appropriate sources when using these datasets and respect their individual licenses.

## Citation

If you use this implementation in your research, please cite:

```
@INPROCEEDINGS{9287356,
  author={Roizman, V. and Jonckheere, M. and Pascal, F.},
  booktitle={2020 28th European Signal Processing Conference (EUSIPCO)}, 
  title={Robust Clustering and Outlier Rejection Using the Mahalanobis Distance Distribution}, 
  year={2021},
  pages={2448-2452},
  doi={10.23919/Eusipco47968.2020.9287356}}
``` 