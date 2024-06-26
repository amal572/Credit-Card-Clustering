# Credit-Card-Clustering

This project aims to cluster credit cards based on customer-level data containing 18 behavioral variables, to define an effective marketing strategy. Techniques such as PCA, Kmeans, Agglomerative hierarchy, Gaussian Mixture, and Clustering with PyCaret are utilized for credit card clustering.

# Credit Card Clustering

![Header](header_cc.png)

The sample Dataset summarizes the usage behavior of about 9000 active credit card holders during the last 6 months. The file is at a customer level with 18 behavioral variables. You need to develop a customer segmentation to define marketing strategy from the dataset.

# Objective

There are a lot of features in this dataset (18 behavioral features). We will now perform:

* Data preprocessing
* Feature extraction using PCA to reduce the dimensionality to improve clustering
* Experiment with various clustering models: KMeans, Agglomerative Hierarchical, Gaussian Mixture
* Choosing the number of clusters
* EDA to segment the customers

# Data Description
Link to the dataset: [Kaggle link](https://www.kaggle.com/arjunbhasin2013/ccdata)
Following is the Data Dictionary for Credit Card dataset:

* CUST_ID: Identification of Credit Card holder (Categorical)
* BALANCE: Balance amount left in their account to make purchases
* BALANCE_FREQUENCY: How frequently the Balance is updated, score between 0 and 1 (1 = frequently updated, 0 = not frequently updated)
* PURCHASES: Amount of purchases made from account
* ONEOFF_PURCHASES: Maximum purchase amount done in one-go
* INSTALLMENTS_PURCHASES: Amount of purchase done in installment
* CASH_ADVANCE: Cash in advance given by the user
* PURCHASES_FREQUENCY: How frequently the Purchases are being made, score between 0 and 1 (1 = frequently purchased, 0 = not frequently purchased)
* ONEOFFPURCHASESFREQUENCY: How frequently Purchases are happening in one-go (1 = frequently purchased, 0 = not frequently purchased)
* PURCHASESINSTALLMENTSFREQUENCY: How frequently purchases in installments are being done (1 = frequently done, 0 = not frequently done)
* CASHADVANCEFREQUENCY: How frequently the cash in advance being paid
* CASHADVANCETRX: Number of Transactions made with "Cash in Advanced"
* PURCHASES_TRX: Number of purchase transactions made
* CREDIT_LIMIT: Limit of Credit Card for user
* PAYMENTS: Amount of Payment done by user
* MINIMUM_PAYMENTS: Minimum amount of payments made by user
* PRCFULLPAYMENT: Percent of full payment paid by user
* TENURE: Tenure of credit card service for user

# Data Cleaning

One of the most important preprocessing steps in a Data Science project. In this project, I imputed missing values with the median value, dropped the CUST_ID column, then For our application I am looking for a good visualization so I would like to handle the skewness as much as possible as it will help the model to form better clusters.

##  Feature Extraction with PCA
 
Use PCA to reduce the dimensionality of our data. Select an appropriate number of components and analyze total variance explained. Interpret to make sense of the principal components.

## Cluster Kmean with PCA
In this section we will perform K-Means clustering on the data and check the clustering metrics (inertia, silhouette scores).
![Header](cluster1.png)

## Agglomerative Hierarchical Clustering with PCA
![Header](cluster2.png)

## DBSCAN Cluster
![Header](cluster3.png)
