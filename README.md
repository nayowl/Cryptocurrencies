# Cryptocurrencies
## 1 Overview of the Project
Accountability Accounting, a prominent investment bank, is interested in offering a new cryptocurrency investment portfolio for its customers. In this project the company asked  to create a report that includes what cryptocurrencies are on the trading market and how they could be grouped to create a classification system for this new investment.
The following tasks will be performed in this analysis:
* Preprocessing the Data for PCA
* Reducing Data Dimensions Using PCA
* Clustering Cryptocurrencies Using K-means
* Visualizing Cryptocurrencies Results

## 2 Resources
Software: Python 3.7.6 , Jupyter notebook, Pandas library,sklearn,hvplot,plotly express

Data source: crypto_data.csv

## 3 Result
### Preprocessing the Data for PCA
Before the data processed for PCA the data from csv will be cleaned.The processes are:
* Keep the cryptocurrencies that are being traded & algorithm worked
* Drop the IsTrading column
* Remove rows that have at least one null value
* Keep cryptocurrencies that TotalCoinsMined>0
* Drop column CoinName
* Use get_dummies() to create variables for text features

The result is X dataframe with 532 rows and 98 columns, like we can see on figure 1 . Next, the data will be standardize with StandardScaler() , as shown on Figure 2.


<p align="center">
    <img src="https://user-images.githubusercontent.com/88597187/147422384-476d9b47-66f5-4858-9da6-eca8797727b9.png" width="400" height="200"/>
</p>

<p align="center">
  <sub> Figure 1 DataFrame After Cleaned  </sub>
</p>




<p align="center">
    <img src="https://user-images.githubusercontent.com/88597187/147422397-345b837a-7d89-4597-b660-0222d9f18947.png" width="400" height="200"/>
</p>

<p align="center">
  <sub> Figure 2 Data After Standardized  </sub>
</p>


### Reducing Data Dimensions Using PCA
The  dimensions of the X DataFrame will be reduced to three principal components using PCA Algorithm and will be placed in a new DataFrame as shown in Figure 3.

<p align="center">
    <img src="https://user-images.githubusercontent.com/88597187/147422474-c20ff760-0ed1-4cd4-89c7-cb43e97c256b.png" width="350" height="400"/>
</p>

<p align="center">
  <sub> Figure 3 DataFrame with the three principal components </sub>
</p>



### Clustering Cryptocurrencies Using K-means

Clusters of Cryptocurrencies data were predicted by plotting the elbow curve to find the best value for K using KMeans algorithm. The best value for the clusters is 4 as shown in Figure 4. 

<p align="center">
    <img src="https://user-images.githubusercontent.com/88597187/147422531-b7a8e957-80a1-4700-bdea-b36ea0aaa7fb.png" width="400" height="200"/>
</p>

<p align="center">
  <sub> Figure 4 Elbow Curve  </sub>
</p>

A New Dataframe will be created to show the data with the  predicted clusters and cryptocurrencies features as shown in Figure 5.

<p align="center">
    <img src="https://user-images.githubusercontent.com/88597187/147422597-e2ff0da3-4c15-4712-9c5b-257cea119972.png" width="400" height="200"/>
</p>

<p align="center">
  <sub> Figure 5 Dataframe with predicted clusters and cryptocurrencies features.  </sub>
</p>



### Visualizing Cryptocurrencies Results

The visualizations of the cryptocurrencies results will be shown in Figure 6 and Figure 7.



