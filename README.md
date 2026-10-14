# Customer Segmentation & RFM Analysis using K-Means

> Unsupervised customer segmentation using RFM analysis and K-Means clustering to identify actionable behavioral cohorts.

## Business Problem

E-commerce businesses often treat customers too broadly in marketing campaigns. This project segments customers using transactional behavior so that different cohorts can be approached with different retention and growth strategies.

## Tech Stack

- **Python**
- **Pandas**
- **NumPy**
- **Scikit-Learn**
- **Matplotlib**
- **Seaborn**

## Methodology

### 1. Data Cleaning
Cleaned 500K+ transaction rows by handling missing customer IDs, cancelled orders, and invalid price/quantity records.

### 2. RFM Feature Engineering
Built customer-level:

- **Recency** — how recently a customer purchased
- **Frequency** — how often a customer purchased
- **Monetary** — how much a customer spent

### 3. Feature Transformation
Applied log transformation to reduce skew and standardized features using StandardScaler.

### 4. Customer Clustering
Used the Elbow Method to evaluate the clustering structure and applied K-Means to produce **four behavioral segments**.

## Customer Segments

| Segment | Behavioral profile | Example strategy |
|---|---|---|
| **Champions** | Recent, frequent, high-value customers | Loyalty rewards, VIP benefits, early access |
| **Loyal Regulars** | Consistent purchase behavior and moderate spend | Cross-sell and upsell relevant products |
| **At-Risk** | Historically valuable but inactive recently | Personalized win-back campaigns |
| **Dormant** | Low-value or long-inactive customers | Low-cost re-engagement campaigns |

## Analytical Workflow

**Raw transactions → cleaning → RFM features → transformation → scaling → K-Means → customer segments → business strategy**

## Business Value

The project demonstrates how an analytical segmentation model can move beyond clustering output and translate customer behavior into practical marketing actions.
