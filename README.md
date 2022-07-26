# Cryptocurrencies and Unsupervised Machine Learning

<p align="center">
  <img src="https://github.com/conorwhanson/Cryptocurrencies/blob/main/resources/coin1.png">
</p>

## Purpose & Overview
The purpose of this analysis was to gather crypto currency data from CryptoCompare and build an unsupervised machine learning model to cluster the data and visualize it for possible relationships. 

The crypto dataset was loaded in as a csv file, preprocessed and cleaned, and filtered for coins which are actively trading and currently mined. Next, the dataframe was filtered so as to include only columns: Algorithm(split into columns based on algorithm used), Proof Type, Total Coins Mined, and Total Coin Supply. This dataframe was then scaled and the dimensions reduced to **3** components using PCA. The scaled principal components were saved off as a dataframe and fed into an elbow curve graph to find the optimal K-means value, which was 4. The K-means model with 4 clusters was fitted and the clusters predicted. A final dataframe was created which consisted of the PCA features created previously, their classes, and the cleaned coin data.

Once this work was done a 3D visualization and scatter plot of the PCA model and clusters were created.

![3D_clusters](https://github.com/conorwhanson/Cryptocurrencies/blob/main/resources/PCA_cluster_3d.png)

## Findings & Recommendations

