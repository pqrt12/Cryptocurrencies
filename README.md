# Cryptocurrencies
# Challenge
This Challenge uses unsupervised learning to analyze cryptocurrencies. A Jupyter Notebook, [Crypto.ipynb](https://github.com/pqrt12/Cryptocurrencies/blob/master/Notebooks/Crypto.ipynb), has all work. 

The crypto data is loaded from [crypto_data.csv](https://github.com/pqrt12/Cryptocurrencies/blob/master/Resources/crypto_data.csv), totaling 1252 rows. After filtering out crypto not trading, with null value, or not mined yet, there are 532 rows remaining. They all have defined algorithms. The 'TotalCoinSupply' column is converted to integer, where rows with decimal dot are dropped as the unit is not clear. Finally, 'TotalCoinSupply' should be no less than 'TotalCoinsMined'. The final DataFrame crypto_df has 448 crypto coins.

The DataFrame coins_name is created per challenge requirement. DataFrame X is created for machine learning. After label encoding, data scaling, the numpy array X_scaled is obtained.

PCA analysis helps reduce X_scaled to three dimensions, the resulting DataFrame is pcs_df.

The K-means Elbow curve helps pick k value 6. The K-means clustering result is the DataFrame clustered_df.

The results are visualized in a 3D scatter, an hvplot table and an hvplot scatter. 

Overall, 448 crypto coins are picked, divided into six clusters. It leaves a lot to be desired what the classification means, and how to evaluate the effectiveness. 
