# Insiders Clustering
![image](https://user-images.githubusercontent.com/77629603/161514587-9609878a-ebbd-4609-8123-071fb170e0ef.png)

# 1. Context
This project is based in a Kaggle Challenge wich simulates a business problem. An Ecommerce called All in One wants to release the "Insiders Program". This program consists in segment customers based on their features. The main features we are looking into are:
* Gross Revenue (Unit price * Quantity)
* Recency (days since the last purchase)
* Frequency (times the customer purchase in a period)
The most valuable clients will get some benefits, for that, clustering is a good call.

# 2. Challenge

## 2.1. Problem

The business team wants to retain good customers giving gifts and benefits.

## 2.2. Causes

* There are no method of customer segmentation running.
* Marketing is not data driven.
* The ecommerce don't know their best customers.

## 2.3. Solution

* Using Machine Learning model to do clustering
* Use clusters to do specific marketing to each group of customers

# 3. Solution Development

## 3.1. Data Description 

Checking the shape of the datase, nulls and filling the nulls values.

## 3.2. Data Filtering

Investigating the data and cleaning based on the business assumptions. 

## 3.3. Feature Engineering

Calculating new features based on the original data.

## 3.4. Data Preparation

Using normalization, rescaling and encoding to prepare the data to the Machine Learning model.

## 3.5.  Exploratory Data Analysis 

Investigating variancy, outliers and distribution of the features.

## 3.6. Feature Selection

Selecting the most important features to train the model.

## 3.7. Machine Learning Model

Training different Machine Learning models and comparing based on the Silhouette Scores. The choosen method was the K-Means because of the good speed and accuracy of the model. 

## 3.8. Data Visualization on Metabase

Loading the data into a Sqlite file and making visualization in a Dashboard in Metabase.

[imagem]

# 4. Results and Conclusion

# 4.1 Clusters Id and Names

* Cluster 7 : Insiders
* Cluster 2 : More frequency
* Cluster 0 : Lazy
* Cluster 5 : Hibernating (High recency)
* Cluster 4 : More products
* Cluster 6 : Forgotten
* Cluster 3 : Lost
* Cluster 1 : One-time customer

## 4.2. Main Concluions of Data Visualization

The main conclusios found in the EDA was:

### C1. Cluster Briefing

![image](https://user-images.githubusercontent.com/77629603/161519755-3aa98725-4f5c-4a6e-9f4a-a1e2c0c08dde.png)

There are 12 customers in Insiders group. They have great number of products, gross revenue, frequency and small recency. But also have a large average of returns. They are very few comparing to the total amount, for that reason the averages are very high as we will see in the next conclusions.

### C2. Products

![image](https://user-images.githubusercontent.com/77629603/161524157-cf59ed75-6d91-4afb-be38-744a42201349.png)
Cluster 2 represents the biggest part of the population, for that reason it has the biggests result of quantity of products. But when we look into average of products, Insiders are champions.
The Insiders correspond to 6% of total products bought.

### C3. Gross Revenue

![image](https://user-images.githubusercontent.com/77629603/161524123-c6048e3e-bde6-4098-a42b-ff1ba1b0a646.png)
Cluster 2 represents the biggest part of the population, for that reason it has the biggests result of absolute gross revenue. But when we look into gross revenue average, Insiders are champions.
The Insiders correspond to 14% of total GMV.

### C4. Returns

![image](https://user-images.githubusercontent.com/77629603/161521891-4b902794-b885-4af6-8966-9b15a3e9b59e.png)

Cluster 5 is champion of total returns, they are probably problematic customers. It called attention to analyse it separately. The Insiders have a big average of returns, but in absolute number is not so relevant. 

## 4.2. Model Performances

Nº of clusters: 8

Model Used: Gaussian Mixture Model

Silhouette Score: 0,53

Insiders are few but great customers. They have a good participation of the company revenue. Now, marketing can make custom actions to each cluster and work on their retention.

# 5. Next Steps

* Collecting feedback of the users and improve the usability if necessary
* Improve the performance in the next CRISP cycle

# 6. References

The data is avaliable in this repository.
