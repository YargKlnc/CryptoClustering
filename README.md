# Crypto Clustering
This is Crypto Clustering Project by YK, UofT, Canada.

***Crypto Clustering using Python and unsupervised learning to predict if cryptocurrencies are affected by 24-hour or 7-day price changes.***

![image](https://github.com/YargKlnc/CryptoClustering/assets/142269763/75db4c2a-1f0d-47f9-8d77-a6465b2f9287)

# Description

***Checking the DataFrame with Plot***

![image](https://github.com/YargKlnc/CryptoClustering/assets/142269763/dfd9b22a-8d78-4c8a-9b21-41698fcd4c8e)

***Preparing the Data***

•	Using the StandardScaler() module from scikit-learn to normalize the data from the CSV file
•	Creating a DataFrame with the scaled data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame

*** Finding the Best Value for k Using the Original Scaled DataFrame ***

Using the elbow method to find the best value for k using the following steps:

•	Create a list with the number of k values from 1 to 11.
•	Create an empty list to store the inertia values.
•	Create a for loop to compute the inertia with each possible value of k.
•	Create a dictionary with the data to plot the elbow curve.
•	Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.
•	Answer the following question in your notebook: What is the best value for k?

***Clustering Cryptocurrencies with K-means Using the Original Scaled Data***

Using the following steps to cluster the cryptocurrencies for the best value for k on the original scaled data:

•	Initialize the K-means model with the best value for k
•	Fit the K-means model using the original scaled DataFrame
•	Predict the clusters to group the cryptocurrencies using the original scaled DataFrame
•	Create a copy of the original data and add a new column with the predicted clusters
•	Create a scatter plot using hvPlot as follows:
  o	Set the x-axis as "PC1" and the y-axis as "PC2"
  o	Color the graph points with the labels found using K-means
  o	Add the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point
Optimize Clusters with Principal Component Analysis
•	Using the original scaled DataFrame, perform a PCA and reduce the features to three principal components
•	Retrieve the explained variance to determine how much information can be attributed to each principal component and then answer the following question in your notebook:
  o	What is the total explained variance of the three principal components?
•	Create a new DataFrame with the PCA data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame

***Finding the Best Value for k Using the PCA Data***

Using the elbow method on the PCA data to find the best value for k using the following steps:

•	Create a list with the number of k-values from 1 to 11
•	Create an empty list to store the inertia values
•	Create a for loop to compute the inertia with each possible value of k
•	Create a dictionary with the data to plot the Elbow curve
•	Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k
•	Answer the following question in your notebook:
  o	What is the best value for k when using the PCA data?
  o	Does it differ from the best k value found using the original data?

***Clustering Cryptocurrencies with K-means Using the PCA Data***

Using the following steps to cluster the cryptocurrencies for the best value for k on the PCA data:

•	Initialize the K-means model with the best value for k
•	Fit the K-means model using the PCA data
•	Predict the clusters to group the cryptocurrencies using the PCA data
•	Create a copy of the DataFrame with the PCA data and add a new column to store the predicted clusters
•	Create a scatter plot using hvPlot as follows:
  o	Set the x-axis as "price_change_percentage_24h" and the y-axis as "price_change_percentage_7d"
  o	Color the graph points with the labels found using K-means
  o	Add the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point
•	Answer the following question:
  o	What is the impact of using fewer features to cluster the data using K-Means?

  # References
  Head photo rights belongs to https://decrypt.co/ 

