Analysis of Algorithms for Movie Recommendation System
---------------------------
Group 201712-72
Lillian Chik, Mun Shin (mc3549)

How to use this project:
The source code contains the four algorithms for predicting movie ratings: baseline predictor, nearest neighbors collaborative filtering, latent factor collaborative filtering and content-based linear predictor. Here are the steps to use this project.

1.  Set up the environment with the following libraries and computing framework: 
Python, Numpy, SciPy, Pandas, Scikit-Learn, and Apache Spark

2.  Download the 100k and 20M MovieLens datasets from GroupLens Research:
https://grouplens.org/datasets/movielens/. After unzipping the downloaded dataset, only ratings.csv file will be used. 

3.  Use data_partition.py to split the datasets into training (80%), validation(10%) and test(10%) by random sampling. 

4.  Use Baseline_Predictor.ipynb to evaluate the performance made by the movie recommendation system using global average, user average, item average and adjusted average. 

5.  Use Collaborative_Filtering_100k.ipynb to analyze the performance of nearest neighbors and latent factor collaborative filtering on the 100k MovieLens datasets. 

6.  Collaborative_Filtering_20M.ipynb is revised from Collaborative_Filtering_100k.py using sparse matrix representations to handle the 20M (bigger) MovieLens dataset more efficiently. 

7.  Use Content-based_Recommendation.ipynb to implement content-based linear predictor to predict movie ratings using user and movie features. 

_____________________________________________________________________

## Running the script files

1) User-basedCF_20M.py: Nearest Neighbors Collaborative Filtering

Input K = number of top similar users to use for making predictions
Input FILENAME = path to input file

-----------------------------------------------------------------------

2) Latent_Factor_20M.py: Latent Factor Collaborative Filtering 

Input K = number of latent factors
Input LR = learning rate for Stochastic Gradient Descent
Input LAMBDA = regularization 
Input EPOCHS = number of epochs for Stochastic Gradient

------------------------------------------------------------------------

## You will need Apache Spark in order to run the following scripts

Use Apache Spark command $SPARK_HOME/bin/spark-submit --master "url of spark master node" to run the following scripts. 

3) User-basedCF_Spark.py: Nearest Neighbors Collaborative Filtering Using Spark

Input K = number of top similar users to use for making predictions
Input FILENAME = path to input file
Input MASTER = url of spark master node 

---------------------------------------------------------------------------
4) Latent_Factor_Spark.py: Latent Factor Collaborative Filtering Using Spark

Input K = number of latent factors
Input LR = learning rate for Stochastic Gradient Descent
Input LAMBDA = regularization
Input EPOCH = number of epochs for Stochastic Gradient Descent
Input FILENAME = path to input file
Input MASTER = url of spark master node

