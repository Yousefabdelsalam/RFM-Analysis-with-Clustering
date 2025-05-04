# 🧠 RFM Analysis & Customer Segmentation Clustering

This project focuses on **Customer Segmentation** using **RFM (Recency, Frequency, Monetary) analysis**, a proven technique in marketing analytics that helps identify and understand customer behavior. I used RFM values to segment customers and applied clustering algorithms to discover distinct customer groups based on their purchasing patterns.

---

## 🔍 Project Overview

The goal of this project is to:

- Analyze customer purchase behavior using transactional data.
- Compute **Recency**, **Frequency**, and **Monetary** metrics.
- Score and segment customers based on RFM values.
- Apply clustering algorithms to group customers into meaningful segments.
- Visualize and interpret the clusters for actionable business insights.

---

## 🧮 RFM Feature Engineering

After preparing the dataset, I calculated:

- **Recency (R)**: Days since the customer's last purchase.
- **Frequency (F)**: Total number of purchases.
- **Monetary (M)**: Total amount spent by the customer.

Next, I segmented each RFM value using `pandas.cut()` to assign scores:

- `r_score`, `f_score`, and `m_score` values range typically from 1 to 4 or 5.
- The scoring reflects customer behavior:  
  - **Lower recency = higher r_score** (more recent)  
  - **Higher frequency = higher f_score**  
  - **Higher monetary = higher m_score**

Then, I combined the scores into a single RFM score and assigned customer segments based on that.



## 🤖 Clustering Models Used

I applied and compared three unsupervised clustering algorithms to group customers:

- **K-Means Clustering**  
  - Used Elbow Method and Silhouette Score to determine the best number of clusters.

- **Agglomerative Hierarchical Clustering**  
  - Used dendrograms to visualize cluster merges and identify optimal clusters.

- **DBSCAN (Density-Based Spatial Clustering of Applications with Noise)**  
  - Tuned `eps` and `min_samples` to identify core customer clusters and outliers.

---

## 📈 Results & Insights

- Discovered meaningful customer groups such as:
  - **bronze Customers**
  - **silver Spenders**
  - **gold Customers**
  - **platinum Customers**

- Helped understand which customers deserve retention efforts and which groups to target with promotions.

---

## 🧰 Tools & Technologies

- **Python**
  - `pandas`, `numpy` for data manipulation
  - `matplotlib`, `seaborn` , `potly` for visualization
  - `scikit-learn` for clustering models

- **Jupyter Notebook** for development and experimentation

---

## 🚀 Future Improvements

- Integrate results into a dashboard using **Streamlit** or **Power BI**
- Automate segmentation for real-time analysis
- Explore additional features like customer tenure or product categories
- Export segmentation results into a CRM-ready format

---

⭐ *If you found this project useful or insightful, feel free to star the repo and share feedback!*

