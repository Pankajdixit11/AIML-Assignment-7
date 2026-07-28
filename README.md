# Customer Segmentation using K-Means Clustering and PCA
## 📋 Objective
The primary objective of this project is to segment shopping mall customers into distinct groups based on their annual income and spending behavior using unsupervised machine learning techniques. The project aims to:

- Identify meaningful customer segments for targeted marketing campaigns
- Apply K-Means clustering algorithm to group similar customers
- Use Principal Component Analysis (PCA) for dimensionality reduction and visualization
- Provide actionable insights for business decision-making

## 📊 Dataset
** Dataset Name: ** Mall Customer Segmentation Dataset
** Dataset Link: ** Kaggle - Mall Customer Segmentation

** Dataset Description: **
** Total Records: ** 200 customers
** Features: **
- Customer ID: Unique identifier for each customer
- Gender: Male/Female
- Age: Customer age in years
- Annual Income (k$): Annual income in thousands of dollars
- Spending Score (1-100): Score assigned based on customer spending behavior

### 📚 Libraries Used
** Data manipulation and analysis **
- import pandas as pd
- import numpy as np

** Data visualization **
import matplotlib.pyplot as plt
import seaborn as sns

** Machine Learning **
from sklearn.preprocessing import StandardScaler, LabelEncoder
from sklearn.cluster import KMeans
from sklearn.decomposition import PCA
from sklearn.metrics import silhouette_score

** Utilities **
import warnings
warnings.filterwarnings('ignore')

### 🔧 Methodology:
1. Data Understanding
Loaded the dataset and performed exploratory data analysis

Identified numerical and categorical features

Generated summary statistics to understand data distribution

2. Data Preprocessing
Missing Values: Checked and confirmed no missing values

Feature Removal: Dropped CustomerID as it's not relevant for clustering

Encoding: Encoded Gender using LabelEncoder (0=Female, 1=Male)

Standardization: Applied StandardScaler to normalize features for K-Means

3. Model Development
K-Means Clustering
Used Elbow Method to determine optimal number of clusters (K=5)

Trained K-Means model with K=5 clusters

Assigned cluster labels to each customer

Principal Component Analysis (PCA)
Applied PCA to reduce 4-dimensional data to 2 principal components

Preserved 68.22% of total variance

Used for visualization and interpretation

4. Evaluation
Internal Validation: Silhouette Score (peaked at K=5)

Visual Validation: Scatter plots showing cluster separation

Business Validation: Interpretable clusters with distinct characteristics

### PCA Results
** Explained Variance: **
- PC1: 35.73% of variance (spending behavior dominant)
- PC2: 32.49% of variance (income and gender patterns)
- Total Variance Explained: 68.22%

  ![Customer Cluster](https://github.com/Pankajdixit11/AIML-Assignment-7/blob/b781ccd8312bffc01bdfbbd49bcdad2bcb9c415f/Customer%20cluster.png)

### Visualizations
- Elbow Curve: Shows optimal K at 5 with clear elbow point
- Original Feature Scatter: Displays clusters in Income vs. Spending space
- PCA Visualization: Shows cluster separation in 2D reduced space
- Cluster Characteristics Table: Provides statistical summaries per cluster

## 🏁 Conclusion
This project successfully demonstrated the application of K-Means clustering and PCA for customer segmentation in a retail context. Five distinct customer segments were identified, each with unique characteristics that enable targeted marketing strategies. PCA proved valuable for visualizing high-dimensional data while preserving meaningful patterns. The insights gained can help the shopping mall optimize marketing spend, personalize customer experiences, and increase customer lifetime value. While K-Means has certain limitations, the results provide a solid foundation for data-driven business decisions and can be further enhanced with additional data and advanced techniques.
