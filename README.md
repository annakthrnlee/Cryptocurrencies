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

## Results: 
After removing non-tradable currencies, null values, and the "IsTrading" column, I created a new DataFrame that holds all of the cryptocurrency names. The new DataFrame consisted of 532 rows = 532 tradable cryptocurrencies on the market at that time. 

<img width="751" alt="Screen Shot 2022-09-06 at 6 10 33 PM" src="https://user-images.githubusercontent.com/104043438/188761116-4cbaac9a-705d-42d6-845e-bda4cf50168f.png"

Then I used the K-means algorithm to cluster the cryptocurrencies using the PCA data, where the following steps have been completed:
- An elbow curve was created using hvPlot to find the best value for K.
- Predictions were made on the K clusters of the cryptocurrencies’ data.
- A new DataFrame was created with the same index as the crypto_df DataFrame and had the following columns: Algorithm, ProofType, TotalCoinsMined, TotalCoinSupply, PC 1, PC 2, PC 3, CoinName, and Class.

<img width="1093" alt="Screen Shot 2022-09-06 at 6 15 28 PM" src="https://user-images.githubusercontent.com/104043438/188761608-03b3dd89-00a8-44b8-bb70-e7eec9337a59.png">
 
 #### Elbow Curve:
 <img width="759" alt="Screen Shot 2022-09-06 at 6 16 21 PM" src="https://user-images.githubusercontent.com/104043438/188761686-eb75df3f-c8cf-469a-a534-449334c60bab.png">
 
 #### New DataFrame:
 <img width="1015" alt="Screen Shot 2022-09-06 at 6 16 47 PM" src="https://user-images.githubusercontent.com/104043438/188761722-3109a0e8-512e-4644-b67a-319cb5b69616.png">

Finally, I created a 3-Scatter with the PCA data and the clusters:
<img width="926" alt="Screen Shot 2022-09-06 at 6 17 46 PM" src="https://user-images.githubusercontent.com/104043438/188761821-3bd47a58-9011-4f16-b142-49a9c395bd81.png">

