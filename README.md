# Customer-Segmentation-Retention-Analysis-An-Unsupervised-Machine-Learning-Approach

## **Project Overview**
This project aims to segment customers of a UK-based online retail company using unsupervised machine learning techniques. The company, which sells unique all-occasion gifts, lacks a clear understanding of its customer segments. By analyzing transaction data from December 2010 to December 2011, this project seeks to identify distinct customer segments and assess customer retention through cohort and hypothetical analyses, leading to better business strategies and customer satisfaction.

## **Problem Statement**
The UK-based online retail company specializes in selling unique gifts to a diverse customer base, including wholesalers. However, the company struggles to understand its customer segments, making it difficult to tailor marketing efforts, optimize inventory, and engage customers effectively. The goal of this project is to apply unsupervised machine learning techniques to the transaction data to identify distinct customer segments, analyze customer retention rate, and perform hypothesis testing to gain valuable insights.

## **Dataset**
- **Source**: (https://docs.google.com/spreadsheets/d/1Ec4FEZ91HdIt6Cm-onlseTnKxPjN6p9V/edit?usp=sharing&ouid=111472383935335036775&rtpof=true&sd=true)
- **Time Period**: December 2010 - December 2011
- **Size**: 541,909 rows, 8 columns
- **Key Columns**: `InvoiceNo`, `StockCode`, `Description`, `Quantity`, `InvoiceDate`, `UnitPrice`, `CustomerID`, `Country`

## **Project Methodology**

1. **Data Preprocessing**
   - Removed missing values and duplicates.
   - Filtered out cancelled orders and non-product entries.

2. **Exploratory Data Analysis (EDA)**
   - Analyzed key metrics to understand customer behavior.
   - Visualized purchase patterns across various customer groups.

3. **Cohort Analysis for Customer Retention Rate**
   - Analyzed customer retention over time by dividing customers into cohorts based on their first purchase month.
   - Visualized retention rates across different cohorts to identify patterns in customer behaviour.

4. **Hypothetical Analysis**
   - Tested the hypothesis that customer retention decreases as the cohort index increases.
   - Applied linear regression to compare average retention rates between cohorts acquired in the first half (December 2010 - May 2011) and the second half (June 2011 - December 2011).
   - Found statistical evidence supporting the hypothesis, indicating that retention rates decline over time.

5. **RFM Analysis**
   - Calculated Recency, Frequency, and Monetary values for each customer.

4. **Customer Segmentation**
   - Applied clustering algorithms: K-Means with Silhouette Score, K-Means with Elbow Method, Hierarchical Clustering, and DBSCAN.
   - Determined the optimal number of clusters for each method.

## **Key Findings**
The customer segmentation analysis revealed the following distribution among various customer groups:

- **Champions**: 10.4%
- **Loyal Customers**: 7.8%
- **Potential Loyalists**: 2.4%
- **Lost Customers**: 23.1%
- **At-Risk Customers**: 1.3%
- **Other**: 41.8%

### Cluster Analysis Summary:

| SL No. |           Model_Name          | Data | Optimal_Number_of_clusters |
|--------|-------------------------------|------|----------------------------|
|   1    | K-Means with Silhouette Score | RFM  |             2              |
|   2    |   K-Means with Elbow Method   | RFM  |             2              |
|   3    |    Hierarchical Clustering    | RFM  |             2              |
|   4    |            DBSCAN             | RFM  |             4              |


### **Conclusion**
By identifying distinct customer segments and analyzing retention rates, this project provides valuable insights that can help the retail company tailor its marketing strategies, optimize inventory, and enhance customer engagement.

### **Technologies Used**
- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib, Seaborn

