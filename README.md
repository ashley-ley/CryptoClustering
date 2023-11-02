# Cryptocurrency Analysis README
## Introduction
This project is focused on analyzing and visualizing cryptocurrency market data. We use various data science and machine learning techniques to gain insights into the behavior of different cryptocurrencies. The key components of this analysis include data preprocessing, clustering, dimensionality reduction, and visualization.

## Data Source
We utilize cryptocurrency market data from a CSV file named "crypto_market_data.csv." The data includes several columns, such as price change percentages over different time periods, and the cryptocurrency names.

## Analysis Steps
1. Data Preprocessing
+ I start by loading the data into a Pandas DataFrame and perform data preprocessing, including:
  + Handling missing values by using pd.to_numeric() with errors='coerce'.
  + Normalizing the data using the StandardScaler module from scikit-learn.
  
2. K-Means Clustering
+ I apply the K-Means clustering algorithm to group cryptocurrencies into clusters. Key steps include:
  + Determining the optimal number of clusters (k) using the elbow method. The optimal k_value for both datasets was 4.
    
  + ![image](https://github.com/ashley-ley/CryptoClustering/assets/132225987/ef1beb9f-0e5a-4be7-b23a-f8cce6a32dfd)
  + Initializing the K-Means model with the chosen value of k.
  + Adding a new column to the DataFrame with the predicted clusters.
  + Visualizing the clusters using a scatter plot with hvPlot.
 
  + ![image](https://github.com/ashley-ley/CryptoClustering/assets/132225987/d6228718-ca64-4788-9c56-a3ae0d6438d9)


3. Principal Component Analysis (PCA)
+ To reduce the dimensionality of the data and discover underlying patterns, we use PCA:
  + Performing PCA to reduce the data to three principal components.
  + Creating a DataFrame with the PCA results.
  + Visualizing the PCA results to identify relationships between cryptocurrencies and predicting the number of clusters
    
    ![image](https://github.com/ashley-ley/CryptoClustering/assets/132225987/ddeaae71-349e-49c8-a1c4-58a0a2701138)



## Usage
To replicate this analysis, follow these steps:
+ Ensure you have the required libraries installed. You can find the necessary libraries in the code comments.
+ Load your cryptocurrency market data into the "crypto_market_data.csv" file. Ensure that the data includes the required columns.
+ Run the provided code, which will preprocess the data, perform K-Means clustering, and apply PCA.
+ Visualize the results using the provided code for scatter plots and elbow curves.

## Dependencies
Make sure you have the following Python libraries installed:
+Pandas
+hvPlot
+Matplotlib
+Scikit-Learn
You can install these dependencies using pip or conda.

## Conclusion
This cryptocurrency analysis project provides valuable insights into the behavior and clustering of various cryptocurrencies. The results showed the PCA data resulted in clusters less wide=spread than the data in the original data set. 
