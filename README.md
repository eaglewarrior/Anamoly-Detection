# Anomaly-Detection
This repo depicts the techniques I have tried to detect anamolies in a dataset .

## Data description :

## Predict Financial crisis 

Given certain parameters related to financial performance of companies. I wanted to detect the companies suffering financial distress by using unsupervised method and then will later compare the labels to check performance of the algorithm.

## Data Dictionary:

First column: Company represents sample companies.

Second column: Time shows different time periods that data belongs to. Time series length varies between 1 to 14 for each company.

Third column: The target variable is denoted by "Financial crisis" where 0 is healthy (0). and 1 is financially unstable (1). 

Fourth column to the last column: The features denoted by x1 to x83, are some financial and non-financial characteristics of the sampled companies. These features belong to the previous time period, which should be used to predict whether the company will be financially distressed or not (classification). Feature x80 is a categorical variable.

For example, company 1 is financially distressed at time 4 but company 2 is still healthy at time 14.

## Approach for detecting Anomalies in dataset

Detecting anomalies is quite important as it can affect your analysis .

## Approach -I 

I started with trying many different algorithm like :

Angle-based Outlier Detector (ABOD)

Cluster-based Local Outlier Factor (CBLOF)

Feature Bagging

Histogram-base Outlier Detection (HBOS)

Isolation Forest

K Nearest Neighbors (KNN)

Average KNN

Out of which **Isolation Forest** gave better results so I thought to use Isolation Forest and further do hyperparameter tuning to it .

## Approach -II

I had approx 3.7% of anomalies in my dataset , I tried using Isolation forest and by tuning it parameter I got about 45 % of recall score .Remember as we have only 3.7% of data which is anomaly so accuracy is not at all a good metric to judge our algorithm so we need to measure performance using confusion metric , recall score or F1 score.

## Approach -III

Autoencoder in deeplearning is mostly used to get rid of redundant data but one more of it's use case is to detect anomaly
I choose Autoencoders, which is a deep learning, unsupervised ML algorithm. "Autoencoding" is a data compression algorithm, which takes the input and going through a compressed representation and gives the reconstructed output.

I have used H2O library to make the autoencoder and I got about 83% of recall score.









