# Module 1 Project: Microsoft Movie Studio
* **Student name:** Matt Torok

* **Student pace:** Full Time

* **Instructor name:** Amber Yandow

* **Blog post URL:** https://torokmg.wixsite.com/website/post/module-1-final-project-microsoft-studios

## Backround

The goal of this project was to create a model that will identify key features that will best predict housing prices in King County, WA.

## Column Names and descriptions for Kings County Data Set
* **id** - unique identified for a house
* **dateDate** - house was sold
* **pricePrice** -  is prediction target
* **bedroomsNumber** -  of Bedrooms/House
* **bathroomsNumber** -  of bathrooms/bedrooms
* **sqft_livingsquare** -  footage of the home
* **sqft_lotsquare** -  footage of the lot
* **floorsTotal** -  floors (levels) in house
* **waterfront** - House which has a view to a waterfront
* **view** - Has been viewed
* **condition** - How good the condition is ( Overall )
* **grade** - overall grade given to the housing unit, based on King County grading system
* **sqft_above** - square footage of house apart from basement
* **sqft_basement** - square footage of the basement
* **yr_built** - Built Year
* **yr_renovated** - Year when house was renovated
* **zipcode** - zip
* **lat** - Latitude coordinate
* **long** - Longitude coordinate
* **sqft_living15** - The square footage of interior housing living space for the nearest 15 neighbors
* **sqft_lot15** - The square footage of the land lots of the nearest 15 neighbors


## Features to Use in Model
 
 ### Features used as is
   * **view**
   * **floors**
   * **grade**
   * **bedrooms**
   * **bathrooms**
   * **sqft_living**
   * **sqft_lot**
   * **waterfront**
   * **condition**
 
 ### Engineered Features
   * **yr_renovated** - changed to mean simply whether the house was renovated or not
   * **yr_built** - grouped years into 6 equal groups
   * **zipcode_type** - grouped zipcodes into 3 catagories that were determined by the price/sqft of all the homes in each zipcode
   * **sqft_basement** - changed to mean simply whether the house has a basement or not

## Model Results

### Model 1 Data
   Train Mean Squared Error: 0.0036
   Test Mean Squared Error: 0.00361
   R Squared: 0.78787
   Mean Absolute Error: 0.04631
   Root Mean Squared Error: 0.06008
   Average Predicted Price: 0.45261
   Average Actual Price: 0.45456
   Difference: -0.00195
   
### Model 2 Data
   Train Mean Squared Error: 0.00363
   Test Mean Squared Error: 0.00362
   R Squared: 0.78637
   Mean Absolute Error: 0.04639
   Root Mean Squared Error: 0.06014
   Average Predicted Price: 0.45253
   Average Actual Price: 0.45456
   Difference: -0.00203

## Interpretation of Models
* Both of our models are pretty accurate. They both have an R^2 score of .787 which is a measure of how close the data is to the fitted regression line. It means that 79% of the variability can be explained by our model.
* Both the train MSE and test MSE are very close to eachother which means that our model has a proper fit.
* The root mean squared error went up slightly in our second model. RMSE measures the average distance between predicted values and actual values.
* Model 1 was slightly better at predicting the price, but the difference is insignificant.

## Significant Features

The top 6 features that have the biggest effect on price are:

Whether the house has been renovated
Whether the house has a basement
What condition the house is in
What year the house was built in
Whether the house is on the waterfront
Which zipcode type each house is in

**Recommendation** 
Out of the 6 most significant features from our model, half are able to be changed by someone wanting to increase the value of their home: 
* Renovating their home
* Increasing the condition of the home
* Increasing the sqft of the home
