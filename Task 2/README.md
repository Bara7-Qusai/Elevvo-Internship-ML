# Customer Segmentation 

## Project Description
This project demonstrates **customer segmentation** using the Mall Customer dataset from Kaggle.  
The goal is to group customers based on **Annual Income** and **Spending Score** to identify distinct customer profiles and better target marketing strategies.

---

## 🔹 Dataset
- **Source:** [Mall Customers Dataset](https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python)
- **Columns:**
  - `CustomerID`: Unique identifier for each customer
  - `Gender`: Male or Female
  - `Age`: Customer age
  - `Annual Income (k$)`: Yearly income in thousand dollars
  - `Spending Score (1-100)`: Score based on spending behavior

---

## 🔹 Tools & Libraries
- Python 3 (Kaggle Python Docker image)
- Pandas
- Numpy
- Matplotlib
- Seaborn
- Scikit-learn (`KMeans`, `DBSCAN`, `StandardScaler`)

---

## 🔹 Steps Performed

### 1️⃣ Data Loading & Exploration
- Load the CSV dataset from Kaggle input directory.
- Inspect the first few rows to understand the data structure.

### 2️⃣ Feature Selection & Scaling
- Selected features: `Annual Income (k$)` and `Spending Score (1-100)`.
- Applied `StandardScaler` to normalize features for clustering.

### 3️⃣ Finding Optimal Clusters (Elbow Method)
- Used **K-Means** with `k` ranging from 1 to 14.
- Plotted **Sum of Squared Distances (SSD)** to find the elbow point.
- Optimal number of clusters identified as `k = 5`.

### 4️⃣ K-Means Clustering
- Applied K-Means with 5 clusters.
- Added cluster labels to the dataset.
- Calculated average spending per cluster:

| Cluster | Average Spending |
|---------|----------------|
| 0       | 49.52          |
| 1       | 82.13          |
| 2       | 79.36          |
| 3       | 17.11          |
| 4       | 20.91          |

- Visualized clusters using a scatter plot.

###  DBSCAN Clustering 
- Applied **DBSCAN** with `eps=0.5` and `min_samples=5`.
- Added DBSCAN cluster labels including noise points (-1).
- Calculated average spending per DBSCAN cluster:

| Cluster | Average Spending |
|---------|----------------|
| -1      | 46.87          |
| 0       | 43.10          |
| 1       | 82.80          |

- Visualized DBSCAN clusters with color-coded points and noise identification.

---

## 🔹 Visualizations
- K-Means clusters clearly show groups such as:
  - High income / high spending
  - Low income / low spending
- DBSCAN identifies dense clusters and outliers.

