# Cryptocurrencies
## Overview
This project explores unsupervised machine learning using Sci-Kit learn's varius libraries. Utilizing a crtyptocurrency dataset, we will use unsupervised machine learning to cluster cryptocurrencies using the KMeans algorithm. 

## Resources
Data: Cryptocurrency Data  
Software: Visual Studio Code 1.72.1, Jupyter Notebook 6.4.8, Python 3.7.13  
Libraries: [Pandas](https://pandas.pydata.org/docs/), [Plotly](https://plotly.com/python/), [Sci-Kit Learn](https://scikit-learn.org/stable/)

## Results
### Preprocessing
The below images show the before and after of the cryptocurrency dataset:

![](Images/Original_Dataset.PNG)
> Original Dataset

![](Images/Preprocessed_Dataset.PNG)
> Preprocessed Dataset

In order to prepare the dataset for machine learning, unnecessary columns needed to be removed and any rows with null values were removed from the data set.

![](Images/PCA_dataset.PNG)
> PCA Dataset

Lastly, we used the PCA class in Sci-Kit Learn to reduce the total number of dimensions in the machine learning algorithm to three. This allows the model to only train off of relevant variables.

### Clustering
The KMeans algorithm uses centroids determined ahead of time to group data that are close to each other. In order to determine a good number of clusters for our dataset, we use the elbow curve method. Graphing the number of clusters on the x by the inertia of the model on the y, we focus on when the graph goes sharply from vertical to horizontal, and then choose that particular cluster amount. In the below image, we see four clusters is the appropriate amount.

![](Images/Inertia.PNG)
> Elbow Curve

We can then graph the three dimensions applied to the machine learning algorithm by group on a 3D graph here:

![](Images/3D_Plot.PNG)
> Clustered KMeans Data

And lastly we can see each crypto coin based on total coins in supply, total coins mined, and which group the KMeans algorithm clustered them in.

![](Images/Clustered_Coins.PNG)
> Cryptocurrencies


## Summary
It seems a lot of cryptocurrencies are similar in their mining and supply habits with the exception of BitTorrent and TurtleCoin. BitTorrent has by far the most coins mined and also has a large coin supply. TurtleCoin has a large supply, but very little coins mined. BitTorrent is so different from the other coins that the algorithm classified it in a class by itself. This certainly seems like a good starting point in the cryptocurrency market.