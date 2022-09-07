# Cryptocurrencies
## Overview: 
Accountability Accounting, a prominent investment bank, is interested in offering a new cryptocurrency investment portfolio for its customers. The company, however, is lost in the vast universe of cryptocurrencies. My job is to create a report that includes what cryptocurrencies are on the trading market and how they could be grouped to create a classification system for this new investment. The data I was given is not in an ideal format for my algorithms, so it will need to be processed to fit the machine learning models. Since there is no known output for what the company is looking for, I will use unsupervised learning. 

- Using my knowledge of Pandas, I preprocessed the dataset to perform PCA.
- Using my knowledge of PCA (Principal Component Analysis) algorithm, I reduced the dimensions of the X DataFrame to three principal components and placed these dimensions into a new DataFrame.
- Next, I clustered the cryptocurrencies using the K-Means algorithm. 
- Finally, using my knowledge of creating scatter plots with Plotly Express and hvplot, I visualized the distinct groups that corresponded to the three principal components. 

## Resources:
- Software: Python 3.9.7 and Jupyter Notebook
- Data: crpto_data.csv

## Definitions:
- K-Means: The K-means algorithm groups the data into K clusters, where belonging to a cluster is based on some similarity or distance measure to a centroid.
- PCA: PCA is a statistical technique to speed up machine learning algorithms when the number of input features (or dimensions) is too high. The technique 
reduces the number of dimensions by transforming a large set of variables into a smaller one that contains most of the information in the original large set.

## Results: 
After removing non-tradable currencies, null values, and the "IsTrading" column, I created a new DataFrame that holds all of the cryptocurrency names. The new DataFrame consisted of 532 rows = 532 tradable cryptocurrencies on the market at that time. 

<img width="599" alt="Screen Shot 2022-09-06 at 6 33 25 PM" src="https://user-images.githubusercontent.com/104043438/188763263-d1085dc7-e9b5-41ab-acfd-a6abce595684.png">

Then I used the K-means algorithm to cluster the cryptocurrencies using the PCA data, where the following steps have been completed:
- An elbow curve was created using hvPlot to find the best value for K.
- Predictions were made on the K clusters of the cryptocurrencies’ data.
- A new DataFrame was created with the same index as the crypto_df DataFrame and had the following columns: Algorithm, ProofType, TotalCoinsMined, TotalCoinSupply, PC 1, PC 2, PC 3, CoinName, and Class.
  
<img width="1093" alt="Screen Shot 2022-09-06 at 6 15 28 PM" src="https://user-images.githubusercontent.com/104043438/188761608-03b3dd89-00a8-44b8-bb70-e7eec9337a59.png">
 
 #### Elbow Curve:
 <img width="759" alt="Screen Shot 2022-09-06 at 6 16 21 PM" src="https://user-images.githubusercontent.com/104043438/188761686-eb75df3f-c8cf-469a-a534-449334c60bab.png">
 
 #### New DataFrame:
 <img width="1015" alt="Screen Shot 2022-09-06 at 6 16 47 PM" src="https://user-images.githubusercontent.com/104043438/188761722-3109a0e8-512e-4644-b67a-319cb5b69616.png">

### 3D-Scatter plot with the PCA data and the clusters:
<img width="926" alt="Screen Shot 2022-09-06 at 6 17 46 PM" src="https://user-images.githubusercontent.com/104043438/188761821-3bd47a58-9011-4f16-b142-49a9c395bd81.png">

#### Finally, I created a new table with the tradable cryptocurrencies. The total number of tradable cryptocurrencies = 532 

<img width="748" alt="Screen Shot 2022-09-06 at 6 20 25 PM" src="https://user-images.githubusercontent.com/104043438/188762027-42364cfb-e3f4-4f13-9840-541ddd2380be.png">

<img width="777" alt="Screen Shot 2022-09-06 at 6 21 00 PM" src="https://user-images.githubusercontent.com/104043438/188762082-e4603327-bd8f-4257-9101-faf24ceb2da6.png">

## Summary: 
As you can see from the final 2D-Scatter plot, most of the clusters are overlapping and not quite forming the distincts groups as we had hoped. That's why I also created a 3D graph to help better visualize each group, providing three distinct groups that correspond to the three clusters that we expect the model to break the data into. 

<img width="926" alt="Screen Shot 2022-09-06 at 6 27 58 PM" src="https://user-images.githubusercontent.com/104043438/188762767-711ff7d5-7d6f-4f71-9575-70cc2a0f4d4c.png">
- The 3D scatter plot can be rotated using the mouse to click and drag using the scroll wheel. Try hovering over a unique point to receive information such as each principal component. 
