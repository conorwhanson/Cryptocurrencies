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

There were some interesting results from the K-means clustering and PCA dimensionality reduction. 

- Classes 2 and 0 were most populated, with 286 and and 239 respectively. Class 0 contained many popular or well-known coins such as Bitcoin and Ethereum. Class 2 seemed to have similar Proof Types.

- Class 1 had a single coin in it: BitTorrent. This was a massive outlier when visualized. I'd recommend further research on this to see if there is something special about BitTorrent (or what's causing it to exist in a lone class).

- Running an explained variance shows that the 3 principal components accounted for only **7%** of the variance. This is very low and points to there being not much relationship in the features data. Either more features need to be gathered or more data is needed, or a recognition that this crypto data ust simply does not contain meaningful relationships.