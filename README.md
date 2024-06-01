# CryptoClustering
The purpose of this project was to use Python and unsupervised learning to predict if cryptocurrencies are affected by 24-hour or 7-day price changes.

The following libraries and dependencies were used: 
- pandas
- hvplot
- sklearn; KMeans, PCA, StandardScaler

To completed the analysis, the following steps were executed:
1) Import the csv file and save the data as a dataframe
2) Plot the dataframe to visualize the price changes for each bitcoin
3) Use StandardScaler to normalize the data and save it as a dataframe
4) Find the best value of K to use for the model using a range of 1 to 12
5) Create a KMeans model that iterates through the range and save the resulting inertia to a list
6) Plot the inertia list vs k value to generate the elbow curve and identify where the bend occurs - this would be the best value for k, which was determined to be 4. 
7) Initialize a new KMeans model after founding the best value for k. 
8) Add a column in the standardized dataframe to hold the predicted clusters from the model. 
9) Plot the clusters.
10) Optimize clusters using PCA and retrieve the explained variance .
11) Repeat steps 4 to 8 while using the PCA data. 
12) Plot the elbow curves and cluster plots side by side to compare the outcomes with and without using the PCA technique.

After the comparison, it was noted that using the PCA technique results in tigther clusters with more entries within 0 and 1 when comapred to the original analysis. 