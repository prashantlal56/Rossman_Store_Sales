# Rossman Store Sales Prediction

## Project Description 

Rossmann operates over 3,000 drug stores in 7 European countries. Currently, Rossmann store managers are tasked with predicting their daily sales for up to six weeks in advance. Store sales are influenced by many factors, including promotions, competition, school and state holidays, seasonality, and locality. With thousands of individual managers predicting sales based on their unique circumstances, the accuracy of results can be quite varied.

Provided with historical sales data for 1,115 Rossmann stores. The task is to forecast the "Sales" column for the test set. Note that some stores in the dataset were temporarily closed for refurbishment.

## Project Overview 

* Exploratory Data Analysis and Visualisation  
* Feature Engineering  
* Merging train and store dataset to form new train dataset containing all the attributes   
* Building and Implementing Machine Learning Models  
* Model Evaluation  
* Test dataset prediction of sales for up to six weeks   

## Resources Used 

Python Version : 3.8  
Packages : pandas, numpy, sklearn, matplotlib, seaborn, plotly, cufflinks  
Reference and article : Google  
Project Motivation :[Krish Naik](https://www.youtube.com/user/krishnaik06)  
Dataset can be found here: [Kaggle](https://www.kaggle.com/c/rossmann-store-sales/data)   


## Exploratory Data Analysis :
I have done indepth analysis by going through each attributes, finding their relations with the store sales, making pivot tables and plotting graphs  

Some of my findings are :

### Days of Week :  
  
![alt text](https://github.com/prashantlal56/Rossman_Store_Sales/blob/master/pic/dayOfWeek1.png)

#### Takeaway 
* The 7th day of week has very less variability as compare to other days of week  
* The count of 7th days is very less as compare to other days but the average sales and average number of customers are pretty much high.  
* One possible reason could be on sunday customers comes for a specific commodity as an essential need for survival  

### running Promo :  

![alt text](https://github.com/prashantlal56/Rossman_Store_Sales/blob/master/pic/running%20promo.png)

#### Takeaway 
* There is much difference in sale before and after running Promo. It indicates that promo have done a great job in increasing the sale  
* Not much noticable difference is seen in number of customers visit to store. Promo idea was not capable to attract new customers but the buying quantity of existing old customers have increased, therefore overall the running of promo worked  

### State Holidays :

![alt text](https://github.com/prashantlal56/Rossman_Store_Sales/blob/master/pic/state%20holiday2.png)

#### Takeaway  
* People are more often to buy more on Christmas and Easter festival, therefore sales and count of customers visit are more on this seasons  
* But it is clearly seen the variation in public choice is less in these festival as people tend to buy particular range and type of product,where as the opposite behavior is been observed when there is no holiday  

![alt_text](https://github.com/prashantlal56/Rossman_Store_Sales/blob/master/pic/average%20sales%20per%20customers1.png)  

#### Takeaway  
* As early said Christman and Easter festival season shows high rate of sales 

![alt_text](https://github.com/prashantlal56/Rossman_Store_Sales/blob/master/pic/avg%20cust%20vas%20avg%20sales.png)
![alt_text](https://github.com/prashantlal56/Rossman_Store_Sales/blob/master/pic/avg%20sale%20vs%20compet.png)

## Feature Engineering

* Converted into datetime format containing date information
* Made column of sales per customers 
* Made columns which captures all the information of customers based on different categories of stores
* Made columns to show Date information separately
* Made column contains date information in months since the competition was opened
* Made column contains date information in weeks since the promo is running
* Get the dummy varaible of categorical columns
* Log transformation to get the variables distribution as close as Gaussian distribution

## Building and Implementing Machine Learning Models  
First I split the dataset into train and test, then i performed ML model building and trained the model using engineered dataset.  
With engineered dataset I tried to build **Random Forest** model beacause the model's performance is not affected by an outliers  

## Model Evaluation   
* **oob score** : 0.9228561536464273
* **Root Mean Square Error** : 854.7540464572053
##### 5 Important features  
![alt text](https://github.com/prashantlal56/Rossman_Store_Sales/blob/master/pic/imp%20feat.png)

### Predictions from Model 

![alt text](https://github.com/prashantlal56/Rossman_Store_Sales/blob/master/pic/pred.png)
