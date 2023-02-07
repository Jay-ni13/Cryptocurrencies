# Cryptocurrencies
## Project Overview
Utilizing unsupervised machine learning to group cryptocurrencies currently on the trading market and create a new classification system for Accountability Accounting--a prominent investment bank--to offer a cryptocurrency investment portfolio for its customers.

## Resources
 - Data Source: Crypto Compare; crypto_data.csv
 - Article: [Crypto token supplies explained: Cirrculating, maximum and total supply](https://cointelegraph.com/explained/crypto-token-supplies-explained-circulating-maximum-and-total-supply)
 - Software: Python v3.7.13, Jupyter Notebook v6.4.8, Scikit-learn v1.0.2, hvPlot v0.8.2

## Results
After processing the dataset from CryptoCompare to keep only the cryptocurrencies that are currently being traded, the features are standardized in order to apply the Principal Component Analysis (PCA) algorithm and reduce the number of dimensions to avoid overfitting of the machine learning model and extract the principal components. Next, the K-Means algorithm is used to create an elbow curve to find the best value for K and predict the K clusters for the cryptocurrencies’ data--the curve indicates that 4 is the best number of clusters to use for the K-Means analysis.

<img src="https://github.com/Jay-ni13/Cryptocurrencies/blob/main/Images/elbow_curve.png" width=80%>

A 3-D scatter plot is used to visualize the cryptocurrencies according to their three principal components as clustered around 4 centroids:

<img src="https://github.com/Jay-ni13/Cryptocurrencies/blob/main/Images/crypto_3D.png" width=75%>

This table displays the tradable cryptocurrencies on the market--523 in total:

<img src="https://github.com/Jay-ni13/Cryptocurrencies/blob/main/Images/current_trading_coins.png" width=80%>

A 2-D scatter plot shows how the cryptocurrency clusters graph based on their total coin supply versus the total coins mined(i.e. created):

<img src="https://github.com/Jay-ni13/Cryptocurrencies/blob/main/Images/coin_scatter.png" width=75%>

## Summary
The majority of cryptocurrencies on the market cluster around two categories/centroids. However, there are four coin types that form a slightly more separate group--LitecoinCash, Acute Angle Cloud, Poa Network, and BiblePay--and one currency that forms its own cluster entirely--BitTorrent--as shown in both the 2-D and 3-D graphs. The extreme difference between BitTorrent and the rest of the cryptocurrencies has to do with how close its ratio of Total Coins Mined to Total Coin Supply is--i.e. 99% of BitTorrent's coin supply is available for trading (in low demand) at the current price of $0.00000074 USD per token. This indicates that BitTorrent might not be a good cryptocurrency to include in Accountablity Accounting's new investment portfolio, and that more research should be done to determine why these cryptocurrencies were grouped the way they were by the machine learning model and what that implies for their market value overtime.
