# Predict diamond's price competition
The goal of this project is the prediction of the price of diamonds based on their characteristics (weight, color, quality of cut, etc.).

![alt text](https://sep.yimg.com/ay/jbead/diamonds-the-4-c-s-11.gif)

## Table of Contents
1. [General Info](#general-info)
2. [Data](#data)
3. [Technologies](#technologies)
4. [Summary](#summary)
5. [Competition](#collaboration)
6. [Rules](#rules)


### General Info
This is an academic competition created for the students of Iron Hack Data Analytics Bootcamp Part Time Edition April 2020.

Part of this project is based on the previous project where we made an exploratory data analysis of a dataset with another 40k different diamonds with the similar characteristics and price. 
The aim of this part is to use the ML algorithms to predict the market price of 16k diamonds based on their characteristics.


### Data
In this section you will find data needed to train your model and a detailed description of it.

#### Files
- diamonds_train.csv: training set
- diamonds_predict.csv: test set
- sample_submission.csv: sample submission

#### Features
- *id*: only for test & sample submission files, id for prediction sample identification
- *price*: price in USD
- *carat*: weight of the diamond
- *cut*: quality of the cut (Fair, Good, Very Good, Premium, Ideal)
- *color*: diamond colour, from J (worst) to D (best)
- *clarity*: a measurement of how clear the diamond is (I1 (worst), SI2, SI1, VS2, VS1, VVS2, VVS1, IF (best))
- *x*: length in mm
- *y*: width in mm
- *z*: depth in mm
- *depth*: total depth percentage = z / mean(x, y) = 2 * z / (x + y) (43--79)
- *table*: width of top of diamond relative to widest point (43--95)


### Technologies
Core technical concepts and inspirations:
- Python 3.7.3
- Numpy 1.18.1
- Pandas 0.24.2
- Plotly 4.8.2
- Matplotlib 3.2.1
- Seaborn 0.10.1
- Scikit-learn 0.23.2
- xgboost 1.2.0
- lightgbm 2.3.0
- catboost 0.24


### Summary
The useful information is defined in EDA made on previos project.
![alt text](https://qualitynoc.es/wp-content/uploads/2020/06/network-operation-center-noc-as-an-efficient-and-comprehensive-network-operations-center-png-520_427.png)

the main conclusions drawn are:
- Correlation > 0.96 between the variables X, Y, Z, Carat, Price.
- X, Y, Z form the size and I calculate the volume of the diamond.
- Carat is the weight, therefore there exist correlation between volume and weight.
- In correlations one to one variable, the only one that correlates with Price is Carat.
- I see in the relationship between Depth and Cut that the worst qualities of Cut are in the extremes and the best in the middle, showing a relationship between Depth and Cut.
- I see that the worst qualities of the combinations Cut-Color-Clarity needs less carat for achieve more prices, showing a relationship between Cut-Color-Clarity with Price.
- I see a clear ladder in the barplot of the Average Price per the combinations of Cut-Color-Clarity, better Cut-Color-Clarity the average of price is lower, showing that is difficult to obtain a diamond with a high quality (Cut-Color-Clarity) and high weight (Carat).

The best result is obtained combine different models based on GBR-RF-XGB-LGB and the most important thing is to do the train & test to validate well with a 80%, 20% of the datasheet to verify that the RMSE result in train is not too far from the test throught validation.

The most important thing is to obtain the lowest RMSE value to predict the price better.

Another important thing is to seek inside the datasheet and create your own variables as volume of the diamond, shape, the logarithm of carat, etc.


### Competition
It is possible to see the Kaggle competicion in this [link](https://www.kaggle.com/c/dataptmad0420/overview)

The evaluation metric chosen for this competition is the [RMSE](https://en.wikipedia.org/wiki/Root-mean-square_deviation) (Root Mean Squared Error)

#### Result
My score in public leaderboard was *518.15125* with 28 entries
My score in private leaderboard was *547.85363* being within the top 5 of my promotion (with a total of 31 participants)


### Rules
- Submissions are limited to 5 times a day.
- The test set is divided into a public part (with which the public leaderboard is calculated, accessible during the competition) and another private part, with which the final positions are calculated, after the end of the competition.
- Predictions will be sent in the format indicated in the sample_submission.csv file in the data section.
- Don't cheat!
- Apply yourself!
- Have fun!

