Customer Segmentation Analysis

Oasis Infobyte — Data Analytics Level 1 | Task 2

Project Overview

This project performs customer segmentation analysis on an Online Retail dataset using RFM (Recency, Frequency, Monetary) analysis and K-Means clustering.

The objective is to identify distinct customer groups based on purchasing behaviour and provide targeted marketing recommendations for each segment.

Objective

- Analyse customer purchasing behaviour.
- Clean and prepare the retail transaction data.
- Calculate customer-level RFM features.
- Standardise the selected features using "StandardScaler".
- Apply K-Means clustering.
- Use the Elbow Method to determine the number of clusters.
- Visualise and profile the customer segments.
- Develop marketing strategies for each segment.

Dataset

The project uses the Online Retail dataset, containing transaction-level information such as:

- Invoice Number
- Stock Code
- Product Description
- Quantity
- Invoice Date
- Unit Price
- Customer ID
- Country

After data cleaning, 397,884 valid transactions and 4,338 unique customers were analysed.

Data Cleaning

The following steps were performed:

- Removed transactions with missing Customer IDs.
- Removed transactions with negative quantities.
- Removed transactions with zero or negative unit prices.
- Created a "TotalAmount" feature using:

"TotalAmount = Quantity × UnitPrice"

RFM Analysis

Three customer behaviour features were created:

- Recency: Number of days since the customer's most recent purchase.
- Frequency: Number of unique invoices/purchases.
- Monetary: Total amount spent by the customer.

The RFM features were standardised using StandardScaler before clustering.

Clustering

The K-Means clustering algorithm was used for customer segmentation.

The Elbow Method was used to determine the number of clusters, and 4 clusters were selected for the final analysis.

Customer Segments

Cluster| Segment| Customers
0| Regular Customers| 3,054
1| Low-Value / Inactive Customers| 1,067
2| VIP / Extremely High-Value Customers| 13
3| Loyal High-Value Customers| 204

Marketing Insights

Regular Customers

These customers make moderately frequent purchases and have moderate spending.

Recommended strategy: Personalised promotions, product recommendations, seasonal discounts, and loyalty rewards.

Low-Value / Inactive Customers

These customers have not purchased recently and have relatively low purchase frequency and monetary value.

Recommended strategy: Re-engagement campaigns, personalised discounts, reminder emails, and limited-time offers.

VIP / Extremely High-Value Customers

This small group purchases very frequently and has exceptionally high monetary value.

Recommended strategy: VIP loyalty programs, exclusive offers, early access to products, personalised services, and premium rewards.

Loyal High-Value Customers

These customers purchase frequently, have purchased recently, and generate substantially higher spending than regular customers.

Recommended strategy: Loyalty benefits, personalised recommendations, cross-selling, upselling, and targeted offers.

Visualisations

The project includes:

- Elbow Method plot
- Recency vs Monetary scatter plot
- Frequency vs Monetary scatter plot
- Customer count by cluster bar chart

Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook

Conclusion

The analysis identified four distinct customer segments based on purchasing behaviour. These segments provide useful information for developing targeted marketing strategies, improving customer retention, and focusing business resources on high-value customers.

Project Files

- "Customer_Segmentation_Analysis.ipynb" — Complete analysis notebook
- "Online Retail.xlsx" — Dataset used for the analysis
- "README.md" — Project documentation
