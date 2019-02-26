Description of the dataset:

This dataset is downloaded from the ongoing Hackathon on Analytics Vidhya here https://datahack.analyticsvidhya.com/contest/build-a-recommendation-engine-powered-by-ibm-cloud/.

The dataset contains 330575 rows of transactions. Each transaction has the features-
1. CustomerID
2. InvoiceNo
3. Quantity
4. InvoiceDate
5. UnitPrice
6. Country
7. StockCode

Among these features, the only features that we need are CustomerID(to identify distinct customers) and the StockCode(the item that the customer has bought).
Hence, all other features are dropped. 

Data Preparation:

The dataset is converted into three different sets-
1. Data with user, item, and target field
2. Dummy set (removing quantities and making the value 1 if the item is bought)
3. Normalized data that normalizes purchase frequency (Quantity) with formula:
(x=min(x))/max(x)-min(x)


Next, we split the data into train and test sets.

Models to be used:
1. Popularity (baseline)
2. Cosine Similarity
3. Pearson Similarity

These 3 models are applied to the 3 subsets of data(as given above).

Results:

Performance Criteria:
1. RMSE (Root Mean Squared Error)
2. Recall (buys/actually recommended)
3. Precision (Liked/recommended)

The results are summarized below:
1. Pearson Similarity has the best performance with overall RMSE 0.16167100749943727.
2. Cosine Similarity comes next with overall RMSE  0.28784213504255296.
3. Population similarity has an overall RMSE of 0.50173815309945103.
