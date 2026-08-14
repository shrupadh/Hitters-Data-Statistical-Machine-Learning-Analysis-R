# Hitters-Data-Statistical-Machine-Learning-Analysis-R
Statistical learning analysis of the Hitters dataset using PCA, hierarchical and K-means clustering, and regression methods including linear regression, PCR, PLS, and ridge regression.


This project applies statistical and machine learning methods to the **Hitters dataset** using R. The analysis explores dimensionality reduction, clustering, and regression modeling of Major League Baseball player statistics.

## Analyses

### 1. Principal Component Analysis (PCA)
- Standardized the predictor variables
- Examined variance explained by principal components
- Interpreted PC1 and PC2 using correlations and loadings
- Visualized the results using a scree plot and PCA biplot

### 2. Clustering
- Complete-linkage hierarchical clustering using Euclidean distance
- K-means clustering with K = 2
- Compared player characteristics and mean salaries across clusters
- Compared hierarchical and K-means cluster assignments

### 3. Regression Modeling
Player salary was modeled using:
- Multiple Linear Regression
- Principal Components Regression (PCR)
- Partial Least Squares (PLS)
- Ridge Regression

Model performance was compared using Leave-One-Out Cross-Validation (LOOCV).

## Model Comparison

| Model | Selected Parameter | LOOCV MSE |
|---|---|---:|
| Multiple Linear Regression | All predictors | 118,039.7 |
| PCR | 16 PCs | 115,298.0 |
| PLS | 12 components | **114,847.0** |
| Ridge Regression | λ = 25.53 | 115,547.4 |

PLS achieved the lowest LOOCV prediction error among the four regression approaches.

## Tools

- R
- R Markdown
- ISLR
- pls
- glmnet

## Dataset

The analysis uses the `Hitters` dataset from the ISLR package. After removing observations with missing salary values, 263 players were included in the analysis.
