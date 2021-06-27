# Cryptocurrencies
## Overview
Accountability Accounting, a prominent investment bank is interested in offering a new cryptocurrency investment portfolio for their customers. Martha, a senior manager for the advisory services team was asked to create a report about what cryptocurrencies are on the trading market and how they can be grouped to create a classification system for new investment. 

Since there is no known output to look for, unsupervised machine learning is used to discover unknown patterns. A clustering algorithm is used to group the cryptocurrencies and data visualization is used to share the findings.

## Results
### Preprocessing the Data for PCA
The given crypto data was preprocessed by using the Pandas library. Preprocessing is done by removing null values and dropping columns that are not used by the clustering algorithm. To standardize the dataframe, the StandarsScaler() in the sklearn library is used.

![image](https://user-images.githubusercontent.com/76491891/123544308-ad383780-d720-11eb-9b36-21669b0f5b02.png)
