# Customer Segmentation & RFM Analysis using K-Means

## Business Problem
E-commerce businesses frequently struggle with generic marketing campaigns that treat all customers the same. This project applies unsupervised machine learning to segment 4,000+ retail customers into actionable cohorts based on their transactional history.

## Tech Stack
* **Language:** Python
* **Libraries:** Pandas, NumPy, Scikit-Learn, Matplotlib, Seaborn
* **Techniques:** RFM Feature Engineering, Log-Transformation, StandardScaler, K-Means Clustering, Elbow Method

## Methodology
1. **Data Cleaning:** Cleaned 500K+ transaction rows by eliminating missing customer IDs, cancelled orders, and invalid prices/quantities.
2. **RFM Modeling:** Aggregated transactional data into Recency, Frequency, and Monetary metrics per unique customer.
3. **Data Scaling:** Normalized skewed distributions via log transformation and standardized features using `StandardScaler`.
4. **Clustering:** Ran the Elbow Method to evaluate optimal $k$ and clustered customers into 4 distinct behavioral segments using K-Means.

## Business Insights & Strategy
* **Champions:** High frequency, high spend, recent orders. Strategy: Exclusive VIP perks, early product access, loyalty rewards.
* **Loyal Regulars:** Steady order frequency and moderate spend. Strategy: Cross-selling related categories and upselling premium items.
* **At-Risk:** High spend historically, but high recency (have not purchased recently). Strategy: Personalized email win-back campaigns and special incentives.
* **Dormant:** Single low-value orders from long ago. Strategy: Low-cost automated re-engagement surveys.
