Machine learning-based detection of environmental risk zones from illegal dump sites in Khulna, Bangladesh

Methodology
Data Processing

Study Area Loading: 454,558 grid cells with spatial coordinates
Feature Extraction: 12 predictors from raster data sources
Missing Value Imputation: Spatial neighbor-based imputation followed by mean filling
Feature Engineering: Separate transformations for tree-based and linear models

Machine Learning Models
Tree-Based Models:

Random Forest
XGBoost
LightGBM

Linear/Kernel-Based Models:

Logistic Regression
Support Vector Machine (SVM)
Multi-Layer Perceptron (MLP)
K-Nearest Neighbors (KNN)

PU Bagging Strategy

500 iterations per model
Bootstrap sampling of unlabeled data
Reliability filtering based on LL metric (harmonic mean of precision and recall)
Multiple threshold sensitivity analysis (0.55, 0.60, 0.65, 0.70)
Weighted ensemble aggregation

Validation Approach

Spatial Blocking: 5 clusters via K-means on geographic coordinates
GroupKFold CV: Prevents data leakage across spatial boundaries
Holdout Test Set: 30% of positive samples + matched unlabeled samples
95% Confidence Intervals: Empirical CIs from fold-level scores

Predictor Variables
Distance-Based Features

Road network proximity
Railway line proximity
Drainage system proximity
Road intersections
Building density
Waste transfer stations (STS)
Waterbody proximity

Non-Distance Features

Population density
Digital Elevation Model (DEM)
Waste generation rate
Poverty index
Land surface temperature (LST)
