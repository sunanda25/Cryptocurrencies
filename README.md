# Cryptocurrencies
## Overview
Accountability Accounting, a prominent investment bank is interested in offering a new cryptocurrency investment portfolio for their customers. Martha, a senior manager for the advisory services team was asked to create a report about what cryptocurrencies are on the trading market and how they can be grouped to create a classification system for new investment. 

Since there is no known output to look for, unsupervised machine learning is used to discover unknown patterns. A clustering algorithm is used to group the cryptocurrencies and data visualization is used to share the findings.

## Results
### Preprocessing the Data for PCA
The given crypto data was preprocessed by using the Pandas library. Preprocessing is done by removing null values and dropping columns that are not used by the clustering algorithm. To standardize the dataframe, the StandarsScaler() in the sklearn library is used.

![image](https://user-images.githubusercontent.com/76491891/123544308-ad383780-d720-11eb-9b36-21669b0f5b02.png)

### Reducing Data Dimensions Using PCA 
Using Principal Component Analysis (PCA) algorithm, the dimensions of the dataframe are reduced to 3 principal components. To store the 3 principal components, a new dataframe is created with PC 1, PC 2, PC 3 columns and with an index from the original dataframe.

![image](https://user-images.githubusercontent.com/76491891/123544358-e96b9800-d720-11eb-8d52-df5ab701defe.png)

### Clustering Cryptocurrencies Using K-means
The Elbow curve is used to find the best K value from the dataframe.

![image](https://user-images.githubusercontent.com/76491891/123544404-1e77ea80-d721-11eb-99d8-c1a864581891.png)

Upon getting the K value, the K-means algorithm is initialized, fitted, and predicted by the clusters. A new dataframe is created by concatenating the two dataframes and by adding CoinName, Class columns to it.

![image](https://user-images.githubusercontent.com/76491891/123544410-29327f80-d721-11eb-969d-c76f535d96de.png)

### Visualizing Cryptocurrencies Results
The plotly express, scatter_3d () function is used to plot three clusters from the dataframe.

![image](https://user-images.githubusercontent.com/76491891/123544589-fdfc6000-d721-11eb-906f-9fd3bd21b5b8.png)

By using hvplot.table () function, a table is created with tradable cryptocurrencies. 

![image](https://user-images.githubusercontent.com/76491891/123544620-28e6b400-d722-11eb-93fa-aeb5af0ab731.png)

To scale the data, MinMaxScaler.fit_transform() is used and stored in a new dataframe.  A scatter plot is used to visualize the TotalCoinsMined with TotalCoinSupply data.

