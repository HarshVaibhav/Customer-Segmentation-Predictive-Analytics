# Customer Segmentation & RFM Analysis using K-Means

This project applies RFM (Recency, Frequency, Monetary) analysis and K-Means clustering to group customers by purchasing behavior and translate the segments into potential marketing actions.

## Business Problem

Broad, one-size-fits-all campaigns can miss differences in customer value and activity. This analysis explores whether transaction history can help identify customer groups for retention, re-engagement, and growth strategies.

## Dataset and Cleaning

- **Dataset:** Online Retail transaction data
- **Raw rows loaded:** 541,909
- **Rows remaining after the notebook's cleaning steps:** 397,884
- **Customers remaining for RFM analysis:** 4,338

The notebook removes rows with missing customer IDs, cancelled invoices, non-positive quantities, and non-positive unit prices. These choices define the analyzed population and should be considered when interpreting the results.

## Tech Stack

- Python
- Pandas and NumPy
- Scikit-learn
- Matplotlib and Seaborn
- Jupyter Notebook

## Methodology

1. **Load and clean transactions** by applying the filters described above.
2. **Calculate line-item value** as quantity multiplied by unit price.
3. **Build customer-level RFM features:**
   - **Recency:** days since the customer's latest purchase
   - **Frequency:** number of distinct invoices
   - **Monetary:** total line-item value
4. **Transform and scale features** to reduce skew and standardize the inputs.
5. **Inspect the Elbow Method** to assess candidate cluster counts.
6. **Fit K-Means with four clusters** using a fixed random seed.
7. **Compare cluster profiles** using recency, frequency, and monetary summaries and visualizations.

## Customer Segments

The analysis uses four clusters. The business labels below are interpretations of the cluster profiles rather than guaranteed meanings of the numeric cluster IDs.

| Interpreted segment | General profile | Potential action |
|---|---|---|
| **Champions** | Recent, frequent, high-value customers | Loyalty rewards and early access |
| **Loyal Regulars** | Consistent purchase behavior | Relevant cross-sell and upsell |
| **At-Risk** | Previously valuable but less recently active | Targeted win-back campaigns |
| **Dormant** | Lower activity or long time since last purchase | Low-cost re-engagement tests |

Validate these labels against the final cluster summary before using them in a business decision; K-Means cluster numbers themselves have no inherent ranking.

## How to Run

1. Download the Online Retail dataset and place the Excel file at `data/Online Retail.xlsx` relative to the notebook.
2. Install the notebook dependencies: `pandas`, `numpy`, `openpyxl`, `scikit-learn`, `matplotlib`, and `seaborn`.
3. Open `Customer Segmentation and Predictive Analytics-checkpoint.ipynb` in Jupyter Notebook or JupyterLab.
4. Run the cells in order.

The notebook expects the dataset to be supplied locally; the raw Excel file is not embedded in the notebook repository. If you use a different location, update the `file_path` variable in the first data-loading cell.

## Limitations

- RFM values reflect the dataset's transaction period and the notebook's chosen snapshot date, not a live customer state.
- K-Means is sensitive to feature choices, scaling, and the selected number of clusters.
- Segment names are business interpretations and should be validated against cluster-level statistics.
- The analysis does not establish that a marketing action will cause improved retention or revenue.

## Workflow

**Transactions → cleaning → RFM feature engineering → log transformation and scaling → K-Means → cluster profiling → potential marketing actions**
