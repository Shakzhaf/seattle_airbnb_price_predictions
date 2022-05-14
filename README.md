# Seattle Airbnb Price Predictions
Since 2008, guests and hosts have used Airbnb to travel in a more unique, personalized way. As part of the Airbnb Inside initiative, this dataset describes the listing activity of homestays in Seattle, WA. 

## Problem Statement 
For all prospective Airbnb hosts in Seattle, I will answer these questions in this project:
- when to rent to maximise revenue?
- when is the off-peak season for maintenance?
- common group size of Seattle travellers, is it 2 or family or 4 or larger?
- bedroom configurations to maximise booking rates?
- how to achieve a good rating?
- do hosts with higher rating have higher revenue?
- which areas in have high price an loow price


## Business Objectives:
You as a Data scientist are required to apply some data science techniques for the price of houses with the available independent variables. That should help the management to understand how exactly the prices vary with the independent variables. They can accordingly manipulate the prices of the houses, the business strategy etc. to meet certain price levels.

## Algorithm
- Decison Trees
- Linear Regression
- Lasso Regression
- Ridge Regression
- ElasticNet Regression

## The solution is divided into the following sections:
- Data understanding and exploration
- Data cleaning
- Data preparation
- Model building and evaluation

### Data Understanding and Explorations
- there are 1734 listings in this test dataset and 3466 listing in train dataset.
- values in the price column contain the dollar symbol ($)
- there are no missing values in columns bathrooms, bedrooms, and beds
- there is a particular listing where no of bedrooms is 0. (which is then dropped in teh later stage)

### Data cleaning
![](https://github.com/Shakzhaf/seattle_airbnb_price_predictions/blob/main/Content/cleaning.JPG)

### Data Visualizations
- Correlations with the help of Heatmaps 
![](https://github.com/Shakzhaf/seattle_airbnb_price_predictions/blob/main/Content/Heatmap.JPG)/
With the help of this heatmap we can conclude that room_type, host_listings_count, cleaning_fee, bedrooms, accommodates, bathrooms, guests_included, cancellation_policy are highly correlated.

- Room Type Distribition
![](https://github.com/Shakzhaf/seattle_airbnb_price_predictions/blob/main/Content/piechart.JPG)    
Conclusion from the Pie Chart     
Shared Room: 2.25%      
Private Room: 21.35%   
Entire home/apt: 76.40%  

- Property Type Distribution
![](https://github.com/Shakzhaf/seattle_airbnb_price_predictions/blob/main/Content/no_vs_property_type.JPG)
Owners are more inclines to listing their property as a whole and not just a part of their house.  
The data is filled with Apartment and House although there are other peoperty type listed here and there.  

- Price vs Room Types
![](https://github.com/Shakzhaf/seattle_airbnb_price_predictions/blob/main/Content/price_vs_room_type.JPG)  
Conclusion from the above Scatter Plot:  
Owners who are offerring their Entire home/apt are going from low to high price range.   
Owner who are offerring Private Room are going from low to medium price range.   
Owners who are offering Shared Rooms are going for low rates.  

- Neighboorhoood vs Bedroom 
![](https://github.com/Shakzhaf/seattle_airbnb_price_predictions/blob/main/Content/neighbourhood_vs_bedrooms.JPG)

Conclusion from the above heatmap  
It can be analyzed that with the increase in the number of bedrooms price of listing increases. Although, it depends upon the neighbourhood as well(Although there are lot of ouliers in neighbouhood as well).  

### Model Evaluation 

---------------DecisionTree-------------------  
MAE: 0.7606538641621097  
MSE: 0.9561492143230277  
RMSE: 0.9778288266987365  
R2 0.339032  
Accuracy -0.9328513487582233  
---------------Linear ---------------------  
--Phase-1--   
MAE: 0.938703  
RMSE: 1.087538  
R2 0.182396  
--Phase-2--  
MAE: 0.938703  
RMSE: 1.087538  
R2 0.182396   
---------------Ridge ---------------------   
--Phase-1--   
MAE: 0.939518  
RMSE: 1.087467  
R2 0.182502   
--Phase-2--   
MAE: 0.939518
RMSE: 1.087467   
R2 0.182502  
---------------Lasso-----------------------   
--Phase-1--  
MAE: 0.938836  
RMSE: 1.087608   
R2 0.182291  
--Phase-2--   
MAE: 0.938836   
RMSE: 1.087608  
R2 0.182291   
---------------ElasticNet-------------------   
--Phase-1 --  
MAE: 0.939612  
RMSE: 1.088210  
R2 0.181384  
--Phase-2--  
MAE: 0.939612  
RMSE: 1.088210   
R2 0.181384  

From the above result we can Choose Decision Trees
