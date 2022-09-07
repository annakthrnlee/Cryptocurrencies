# Cryptocurrencies
## Overview: 
Accountability Accounting, a prominent investment bank, is interested in offering a new cryptocurrency investment portfolio for its customers. The company, however, is lost in the vast universe of cryptocurrencies. My job is to create a report that includes what cryptocurrencies are on the trading market and how they could be grouped to create a classification system for this new investment. The data I was given is not in an ideal format for my algorithms, so it will need to be processed to fit the machine learning models. Since there is no known output for what the company is looking for, I will use unsupervised learning. 

- Using my knowledge of Pandas, I preprocessed the dataset to perform PCA.
- Using my knowledge of PCA (Principal Component Analysis) algorithm, I reduced the dimensions of the X DataFrame to three principal components and placed these dimensions into a new DataFrame.
- Next, I clustered the cryptocurrencies using the K-Means algorithm. 
- Finally, using my knowledge of creating scatter plots with Plotly Express and hvplot, I visualized the distinct groups that corresponded to the three principal components. 
