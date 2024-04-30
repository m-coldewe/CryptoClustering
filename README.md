# CryptoClustering - Unsupervised Predictions

## Overview
This project seeks to use unsupervised learning to predict if cryptocurrencies are affected by 24-hour or 7-day price changes. 

Utilizes Python, with hvplot and sklearn libraries.

## Purpose
To complete this project, the program uses the following steps:
- get and read the data from the csv
- visualize the data, using summary statistics and a simple line graph
- scale the data in order to visualize the data using similar numbers
- use a KMeans model to test values 1-10 for the optimal k-value
- visualize the results to best see the optimal value

With the optimal k-value:
- create the model with the chosen k-value
- fit the model
- predict using the scaled dataset
- add the predictions to the dataset to allow visualization
- visualize the result

To test for better results with principal component analysis:
- select the number of components to comprise the new dataset version
- fit and transform the data to get the new dataset version
- check how much of the data is preserved in the new dataset
- prepare the transformed dataset
- repeat the previous steps using the new dataset to find the optimal k-value
- repeat the previous steps using the optimal k-value to predict on the new dataset
- visualize the result
- compare the results

## Result

#### The Data
![original_data](https://github.com/m-coldewe/CryptoClustering/assets/152045367/295467a4-1bb9-41cc-a201-5b95997c5673)

#### Elbow Curve using the Dataset (scaled only)
![original_elbow_curve](https://github.com/m-coldewe/CryptoClustering/assets/152045367/4e08d8a4-7e5d-4d68-8590-fa0a7d39a4d7)

The optimal k-value according the chart appeears to be 4.

#### The Resulting Prediction
![original_prediction_scatter](https://github.com/m-coldewe/CryptoClustering/assets/152045367/34fff998-26ba-4eee-8149-b885c3280116)

While the blue (0) cluster clearly exhibt some sort of grouping, the other clusters don't.

#### Elbow Curve using the PCA Dataset
![pca_elbow_curve](https://github.com/m-coldewe/CryptoClustering/assets/152045367/1d5d4cfd-008d-466f-8b39-51b72d251b47)

While more pronounced, the optimal k-value still appears to be 4.

#### The Resulting Prediction using PCA Dataset
![pca_prediction_scatter](https://github.com/m-coldewe/CryptoClustering/assets/152045367/4f4e2947-89db-4f26-b36b-0c82760cb005)

Here, there are two primary clusters.

To better visualize the differences:
#### Composit Elbow Curve
![composition_elbow_curve](https://github.com/m-coldewe/CryptoClustering/assets/152045367/56ac48f8-072a-4776-b729-081928fcaf84)

#### Side-by-side Prediction plots
![comparison_scatter_plots](https://github.com/m-coldewe/CryptoClustering/assets/152045367/3504d74b-c397-4d0c-83f5-c6048a6ff7da)

## Summary
Whereas the original scatter, using all of the features didn't provide a clear answer, reducing the data with principal component analysis allowed a clearer grouping to emerge with one cluster mostly above 0 for PCA2 values and mostly below 0 for the other cluster. This suggests that while cryptocurrencies might be affected by 24-hour or 7-day price changes, there are likely other factors which also affect them. 
