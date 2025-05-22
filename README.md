
# 🛍️ Mall Customer Segmentation using K-Means Clustering

This project uses unsupervised learning (K-Means clustering) to segment mall customers based on their **Annual Income** and **Spending Score**, helping businesses understand customer behavior and target marketing strategies effectively.

## 📁 Dataset

- **File**: `Mall_Customers.csv`
- **Attributes**:
  - `CustomerID`: Unique ID
  - `Gender`: Male/Female
  - `Age`: Age of the customer
  - `Annual Income (k$)`: Customer income in thousands
  - `Spending Score (1-100)`: Customer's spending score assigned by the mall

## 🧪 Exploratory Data Analysis

- Checked for missing values and duplicates.
- Used only **Annual Income** and **Spending Score** for clustering (2D for visualization).
- Determined the optimal number of clusters using the **Elbow Method**.

## 📊 Clustering Process

1. **Libraries Used**:
   - `pandas`, `numpy` for data handling
   - `matplotlib`, `seaborn` for visualization
   - `sklearn.cluster.KMeans` for modeling
2. **Steps**:
   - Loaded dataset
   - Cleaned the data (checked `null` and `duplicates`)
   - Selected features: `Annual Income`, `Spending Score`
   - Used **K-Means** with `k=5` based on the Elbow plot
   - Visualized clusters and centroids

## 📌 Key Outputs

- **WCSS (Within Cluster Sum of Squares)** plot to identify optimal `k`
- **Scatter plot** showing 5 clusters with different colors
- **Centroids** marked for each cluster

## 📁 Model Export

Model saved using `joblib`:
```python
joblib.dump(model, 'kmeans_model.pkl')
```

> (Note: If a `scaler` was used, make sure to define it. Your code mentions saving `scaler.pkl`, but no scaler is declared.)

## 🔧 Requirements

```
pandas
numpy
matplotlib
seaborn
scikit-learn
joblib
```

Install dependencies:
```bash
pip install -r requirements.txt
```

## ▶️ Run the Project

```bash
python kmeans_clustering.py
```

Make sure the CSV file is in the correct path, or update the path in the script accordingly.
