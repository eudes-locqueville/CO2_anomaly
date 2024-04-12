Predicting Deviations in CO2 Consumption for Alarm Generation 

This project aimed to address the challenge of predicting whether the CO2 consumption on a given day is significantly divergent from the expected value, with the purpose of implementing alarms to notify clients.

I first conducted the basic statistical analysis to understand the behaviour of the data, track missing values and outliers.

The first approach to detect anomalies is a naive approach using quantiles : an anomaly is an observation greater than 1,5 times the third quantile (that is a basic approach to detect outliers that I decided to test for anomalies). 

I noticed a trend in the data and decided to implemet a K-means algorithm to study tow different types of data : the low-consumption days (approximately two days every week) and the normal consumption days. I mixed this approach with a density-based algorithm to track anomalies. This gave me good results. 

Finally, I implemented a density-based algorithm with a predicitve tool (LocalOutlierFactor(novelty=True) from scikit-learn). 
I created a test sample from my original data to test my algorithm which gave me very consistant results.
