# Customer Segmentation Analysis

## Project Overview

This project was developed as part of my **Data Analytics Internship — Level 1, Task 2**.

The objective is to segment customers based on their purchasing behavior using **RFM (Recency, Frequency, Monetary) Analysis and K-Means Clustering**.

Customer segmentation helps businesses understand customer behavior, identify high-value customers, improve marketing strategies and strengthen customer relationships.

## Dataset

- **Source:** Kaggle
- **Dataset:** E-Commerce Data (Online Retail)
- **Dataset Link:** https://www.kaggle.com/datasets/carrie1/ecommerce-data
- **File Used:** `data.csv`

The dataset contains retail transactions, including invoice numbers, product information, quantities, transaction dates, unit prices, customer identifiers and countries.

## Technologies Used

- Python
- pandas and NumPy
- Matplotlib and Seaborn
- Scikit-learn
- KaggleHub
- Jupyter Notebook / Google Colab

## Project Workflow

### 1. Data Collection and Cleaning

- Loaded the dataset directly from Kaggle.
- Examined missing values and duplicate records.
- Removed records without valid customer identifiers.
- Excluded cancelled transactions and non-positive purchase values.
- Converted invoice dates into datetime format.
- Calculated total transaction values.

### 2. Exploratory Data Analysis

Performed descriptive analysis of:

- Total customers
- Total sales
- Purchase frequency
- Average purchase value
- Customer spending distribution
- Customer purchase recency

### 3. RFM Analysis

Created three customer behavior metrics:

**Recency (R):** Number of days since a customer's most recent purchase.

**Frequency (F):** Number of unique purchase invoices made by a customer.

**Monetary (M):** Total value of a customer's recorded positive purchases.

These features were used to understand differences in customer purchasing behavior.

### 4. Data Preprocessing

- Applied logarithmic transformations to reduce skewness in RFM features.
- Standardized numerical values using StandardScaler.
- Prepared the transformed features for clustering.

### 5. K-Means Clustering

Applied the K-Means algorithm to identify customer segments based on their purchasing behavior.

The **Elbow Method** was used to help determine an appropriate number of clusters.

The Silhouette Score was also calculated as an additional clustering quality metric.

### 6. Cluster Visualization

Visualized customer segments using scatterplots of:

- Recency vs Frequency
- Frequency vs Monetary
- Recency vs Monetary

### 7. Cluster Profiling

Analysed each cluster using:

- Average recency
- Average purchase frequency
- Average monetary value
- Customer count
- Average purchase value
- Revenue contribution

### 8. Marketing Recommendations

Developed marketing recommendations according to customer characteristics.

Potential customer groups include:

| Customer Segment | Recommended Strategy |
|---|---|
| Loyal High-Value Customers | VIP rewards and exclusive offers |
| At-Risk High-Value Customers | Personalized win-back campaigns |
| Recent or Occasional Customers | Repeat-purchase incentives |
| Active Repeat Customers | Loyalty programs and cross-selling |
| Inactive Customers | Targeted reactivation campaigns |

Actual segment labels depend on the clustering results.

## Visualizations

- RFM Distributions
- RFM Correlation Heatmap
- Elbow Method Graph
- Customer Cluster Scatterplots
- Cluster Profile Heatmap
- Customers per Cluster Bar Chart
- Revenue Contribution by Cluster

## Results

The project assigns each customer to a segment based on purchasing behavior and produces customer-level and cluster-level summaries.

**Add the actual results after running the notebook:**

| Metric | Result |
|---|---|
| Total Customers Analysed | TBD |
| Optimal Number of Clusters | TBD |
| Silhouette Score | TBD |
| Highest-Revenue Cluster | TBD |

The analysis uses observed customer spending as a historical Customer Lifetime Value proxy, not a prediction of future lifetime value.

## How to Run

1. Clone or download the repository.
2. Install the required libraries.

```bash
pip install "kagglehub[pandas-datasets]" pandas numpy matplotlib seaborn scikit-learn
```

3. Open the project notebook.
4. Run all cells in sequence.
5. The dataset is downloaded automatically using KaggleHub.

**Note:** The CSV may require `ISO-8859-1` encoding when loaded through pandas.

## Output Files

- `customer_rfm_clusters.csv`
- `customer_segment_summary.csv`
- `cleaned_ecommerce_data.csv`

## Conclusion

This project demonstrates how unsupervised machine learning and RFM analysis can be used to identify customers with similar purchasing patterns.

The generated customer segments provide a foundation for targeted marketing, customer retention initiatives and data-driven business decisions.

## Future Improvements

- Customer Lifetime Value prediction
- Customer churn prediction
- Alternative clustering algorithms
- Interactive Power BI dashboards
- Personalized marketing campaign analysis

## Author

**K Shivaram Goud**  
Data Analytics Intern  
B.Tech — Artificial Intelligence and Machine Learning