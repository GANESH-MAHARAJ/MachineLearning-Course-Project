# Machine Learning Course Project — Customer Segmentation using RFM + Clustering

This repository contains my final Machine Learning course project:  
**"Customer Segmentation using K-means, Gaussian Mixture Models (GMM), and DBSCAN"**  
built on the **UCI Online Retail dataset (2010–2011)**.

The project demonstrates how unsupervised learning can uncover actionable customer insights,
combining data preprocessing, feature engineering, model comparison, validation, and business interpretation.

---

## 📘 Project Overview

Customer segmentation helps businesses understand behavioral diversity among their customers and design
personalized campaigns.  
This project constructs an end-to-end segmentation workflow starting from raw transactional data and ending
with interpretable, validated clusters ready for marketing activation.

### Objectives
- Implement and compare **K-means**, **Gaussian Mixture Models**, and **DBSCAN**.
- Evaluate clusters using internal metrics (**Silhouette**, **Jaccard stability**, **ARI/NMI**).
- Translate results into business terms (KPIs, Revenue-Lift curve).
- Add an **Explainable AI** layer using a Decision-Tree surrogate.
- Make the entire analysis reproducible and ready for extension.

---

## 🧭 Workflow

```text
UCI Online Retail Dataset
        │
        ▼
 Data Cleaning & Preprocessing
 (remove cancellations, missing IDs, negative quantities)
        │
        ▼
 Feature Engineering
 (Recency, Frequency, MonetaryNet, Return Ratio)
        │
        ▼
 Standardization & Scaling
        │
        ▼
 ┌──────────────────────────────────────────────┐
 │   Clustering Algorithms                     │
 │   - K-means                                 │
 │   - Gaussian Mixture Model (GMM)            │
 │   - DBSCAN (ε, minPts tuning)               │
 └──────────────────────────────────────────────┘
        │
        ▼
 Validation & Analysis
 (Silhouette, ARI/NMI, Bootstrap Jaccard)
        │
        ▼
 Business Insights
 (KPIs, Revenue-Lift Curve)
        │
        ▼
 Interpretability
 (Decision-Tree surrogate rules)
        │
        ▼
 Deployment Readiness & Drift Monitoring
```

## 🧭 Key Results

| Method      | Silhouette | #Clusters | Stability (Jaccard) | Business Insight                 |
| ----------- | ---------- | --------- | ------------------- | -------------------------------- |
| **K-means** | 0.589      | 4         | 0.745               | Balanced, interpretable baseline |
| **GMM**     | 0.419      | 4–5       | 0.547               | Captures overlapping boundaries  |
| **DBSCAN**  | 0.896      | 2 + noise | —                   | Detects dense cores & outliers   |

- Top 10 % customers contribute > 60 % of total revenue.
- Decision-Tree surrogate reproduces K-means labels with 0.989 accuracy, offering clear “if-then” segmentation rules.
- ARI/NMI ≈ 0 between algorithms → each reveals a unique structural view of the data.

## 🏁 Future Scope
- Add basket2vec/item2vec embeddings to represent product-level affinities.
- Implement Consensus Clustering for ensemble stability.
- Integrate Population Stability Index (PSI) for drift detection.
- Build a Streamlit dashboard for business visualization and CRM export.

## ✍️ Author
Ganesh Maharaj Kamatham

B.Tech – Computer Science Engineering spl in Data Science, VIT Vellore

📧 [ganeshmaharaj.kamatham@gmail.com](ganeshmaharaj.kamatham@gmail.com)

📄 [[LinkedIn Profile](https://www.linkedin.com/in/ganesh-maharaj-kamatham-4b38a6310/)]


