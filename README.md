# Seattle Airbnb Price Predictions
Since 2008, guests and hosts have used Airbnb to travel in a more unique, personalized way. As part of the Airbnb Inside initiative, this dataset describes the listing activity of homestays in Seattle, WA. 

## Problem Statement 
For all prospective Airbnb hosts in Seattle, I will answer these questions in this article:
- when to rent to maximise revenue?
- when is the off-peak season for maintenance?
- common group size of Seattle travellers, is it 2 or family or 4 or larger?
- bedroom configurations to maximise booking rates?
- how to achieve a good rating?
- do hosts with higher rating have higher revenue?


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
![](https://github.com/Shakzhaf/seattle_airbnb_price_predictions/blob/main/Content/Heatmap.JPG)<b />
With the help of this heatmap we can conclude that room_type, host_listings_count, cleaning_fee, bedrooms, accommodates, bathrooms, guests_included, cancellation_policy are highly correlated.

- Room Type Distribition
![](https://github.com/Shakzhaf/seattle_airbnb_price_predictions/blob/main/Content/piechart.JPG)<b />
onclusion from the above Pie Chart<b />
Shared Room: 2.25%
Private Room: 21.35%
Entire home/apt: 76.40%

- Property Type Distribution
![](https://github.com/Shakzhaf/seattle_airbnb_price_predictions/blob/main/Content/no_vs_property_type.JPG)
Owners are more inclines to listing their property as a whole and not just a partt of their house.<b />
The data is filled with Apartment and House although there are other peoperty type listed here and there.<b />

