# Spring2019_Project1
Develop models which use a broad spectrum of features to predict realty prices
PREDICTING REAL ESTATE PRICES

Authors: Kenneth Richardson, Stacey Smith, Joshua Yi
###################################################################################################
GOAL 1:
Introduction
When customers consider signing a lease or purchasing a building, “Sberbank, Russia’s oldest and largest bank” would to like provide them confidence, as Sberbank understands the significance of this investment. In this report, we set out to build two OLS Models and a Lasso Model. Historical sales data in Russia are used to carry out the construction of these models. We will compare each model using the AIC, SBC, internal and external cross validation in determining the best model of estimating the price of individual properties given the characteristics and features such as bedrooms, location, and so on.

Data Description
There were two datasets used for this study; the “modelingdata” and the “predictionData”, these were provided by the instructor, Dr. Selzer. The “modelingdata” is used to create the actual model and the “predictionData” will be appended to the “modelingData” in order to create the predicted sale price for future dates. Python was used for data cleaning and wrangling for both datasets. A data dictionary describing the various variables has been provided – see Appendix 1. The dataset contains 30,471 observations and 292 variables which included homes and buildings that were sold between years 2011 and 2015. The sales prices ranged from $2,047,255 (prices in millions) to $19,205,462 with a mean sales price of $7,075,593 and median sale price of $6,400,000 – Appendix B. 
Exploratory Data Analysis

OUTLIER HANDLING, ASSUMPTIONS AND MISSING VALUES
In performing an analysis of the data, we discovered that there were at least 40% of missing values within certain variables – see Appendix C. Therefore, we decided to use the median for any missing values or NA’s in both the modeling and prediction dataset to build the models. Since the objective of Goal 1 was to build three models to predict individual property values, price_doc was chosen as the response variable. All data wrangling discussions in this section were only performed on the “modelingData”. The histogram as shown in Figure 1 plots indicate the data is not normally distributed, and could be attributed to the presence of outliers. Therefore, there is a need to apply a logarithmic transformation on the variable price_doc. This transformation has been given a new variable name log_price, which can be seen in Figure 2. The log_price is now close to being normally distributed.

###################################################################################################
GOAL 2:
Introduction
The objective for goal 2 is to forecast the price from July 2015 to June 16. The difference here compared to goal 1 is that we will be using the aggregated mean of the price_doc as the response variable and month number as the explanatory variable. No other explanatory variables will be used to create the model. This is a time series-based modeling and forecasting objective. In this section the following items will be provided; data wrangling explanation, plotting of the time series, modeling of the residual series and forecast.
Data Wrangling
Python was chosen to wrangle the original dataset for goal 2. In Python there is a package called Pandas which is a powerful tool to manipulate datasets. Two datasets were created to be later used by SAS to perform time series analysis. For the first dataset (see Figure 18) the timestamp column was separated into 3 columns, month, day and year. Also, the column monthYear was created.  The dataset was wrangled and saved as an Excel file.
