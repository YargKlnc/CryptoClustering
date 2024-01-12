# Crypto Clustering
This is Crypto Clustering Project by YK, UofT, Canada.

***Crypto Clustering using Python and unsupervised learning to predict if cryptocurrencies are affected by 24-hour or 7-day price changes.***

![image](https://github.com/YargKlnc/CryptoClustering/assets/142269763/75db4c2a-1f0d-47f9-8d77-a6465b2f9287)

# Description

#### Analysis Description:

This comprehensive analysis employs various techniques to cluster and analyze cryptocurrency data, aiming to enhance accuracy and visibility. The process begins with the normalization of data using the MinMaxScaler() module from scikit-learn, followed by the creation of a DataFrame with scaled data.

The Elbow Curve Analysis, applied both to the original scaled DataFrame and Principal Component Analysis (PCA) data, guides the determination of the optimal value for k in K-Means clustering. The results reveal insights into the inertia values and their impact on the clustering process.

Further exploration involves clustering cryptocurrencies using K-Means on both the original scaled data and PCA data. Visualization techniques, such as scatter plots, provide a visual representation of the clusters, emphasizing the impact of employing fewer features on cluster separation and identification of outliers.

Despite a deliberate data loss of approximately 10.5%, the analysis consistently yields accurate results, showcasing the robustness of the chosen methodology. The readme encourages exploring alternative models to further refine accuracy and enhance data visibility.

This analysis, detailed in the readme, serves as a valuable resource for understanding the intricacies of clustering cryptocurrency data and offers insights into optimizing the clustering process for improved accuracy and interpretability.

***Checking the DataFrame with Plot***

![image](https://github.com/YargKlnc/CryptoClustering/assets/142269763/dfd9b22a-8d78-4c8a-9b21-41698fcd4c8e)

***Preparing the Data***

• Using the MinMaxScaler() module from scikit-learn to normalize the data from the CSV file.
• Creating a DataFrame with the scaled data and setting the "coin_id" index from the original DataFrame as the index for the new DataFrame.

***Finding the Best Value for k Using the Original Scaled DataFrame***

Using the elbow method to find the best value for k using the following steps:

• Creating a list with the number of k values from 1 to 11.
• Initializing an empty list to store the inertia values.
• Implementing a for loop to compute the inertia with each possible value of k.
• Creating a dictionary with the data to plot the elbow curve.
• Plotting a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.
• Answering the following question in your notebook: What is the best value for k?

***Clustering Cryptocurrencies with K-means Using the Original Scaled Data***

Using the following steps to cluster the cryptocurrencies for the best value for k on the original scaled data:

• Initializing the K-means model with the best value for k.
• Fitting the K-means model using the original scaled DataFrame.
• Predicting the clusters to group the cryptocurrencies using the original scaled DataFrame.
• Creating a copy of the original data and adding a new column with the predicted clusters.
• Creating a scatter plot using hvPlot as follows:
  o Setting the x-axis as "PC1" and the y-axis as "PC2."
  o Coloring the graph points with the labels found using K-means.
  o Adding the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.

***Optimizing Clusters with Principal Component Analysis***

• Using the original scaled DataFrame, performing a PCA and reducing the features to three principal components.
• Retrieving the explained variance to determine how much information can be attributed to each principal component and then answering the following question in your notebook:
  o What is the total explained variance of the three principal components?
• Creating a new DataFrame with the PCA data and setting the "coin_id" index from the original DataFrame as the index for the new DataFrame.

***Finding the Best Value for k Using the PCA Data***

Using the elbow method on the PCA data to find the best value for k using the following steps:

• Creating a list with the number of k-values from 1 to 11.
• Initializing an empty list to store the inertia values.
• Implementing a for loop to compute the inertia with each possible value of k.
• Creating a dictionary with the data to plot the elbow curve.
• Plotting a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.
• Answering the following questions in your notebook:
  o What is the best value for k when using the PCA data?
  o Does it differ from the best k value found using the original data?

***Clustering Cryptocurrencies with K-means Using the PCA Data***

Using the following steps to cluster the cryptocurrencies for the best value for k on the PCA data:

• Initializing the K-means model with the best value for k.
• Fitting the K-means model using the PCA data.
• Predicting the clusters to group the cryptocurrencies using the PCA data.
• Creating a copy of the DataFrame with the PCA data and adding a new column to store the predicted clusters.
• Creating a scatter plot using hvPlot as follows:
  o Setting the x-axis as "price_change_percentage_24h" and the y-axis as "price_change_percentage_7d."
  o Coloring the graph points with the labels found using K-means.
  o Adding the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.
• Answering the following question:
  o What is the impact of using fewer features to cluster the data using K-Means?

  # Summary

  ![image](https://github.com/YargKlnc/CryptoClustering/assets/142269763/16b2ceec-ec8e-4b53-9286-a85da5199398)

  ![image](https://github.com/YargKlnc/CryptoClustering/assets/142269763/b19d8ac4-7014-46fa-b656-b0aa5718a6bc)

#### Summary: 

After visually analyzing the cluster analysis results, the use of K-Means for data clustering demonstrated a significant improvement, effectively reducing ambiguity and enhancing clarity in the analysis.

The Elbow Curve Analysis indicated that, although the k value remained at 4, the inertia decreased post-Principal Component Analysis (PCA). This suggests that employing fewer features resulted in more compact cluster formations.

In the Scatter Plots Analysis, Principal Component Analysis successfully eliminated overlaps, particularly isolating outliers such as `ethlend` and `celsius-degree-token`. Upon closer inspection, it became evident that the use of PCA contributed to clearer cluster distinctions, highlighting the effectiveness of utilizing fewer features for more effectively separated clusters.

Despite a data loss of approximately 10.5%, the analysis still produced accurate results, underscoring the effectiveness of the chosen approach.

Additionally, exploring alternative models could further enhance accuracy and visibility in data analysis.

  # References
  
  Head photo rights belongs to https://decrypt.co/ 

