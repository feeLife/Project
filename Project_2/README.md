# Problem Statement

The company received a project from customers to develop website that will evaluate the price of the asset from the information that the customer entered.By wanting to use AI to analyze And predict the price.

Therefore, the team is drawn to help design the model that will be able to predict the price of the asset. In the source, the team will rely on the information that the customer has. To be used in the model design.

# Data List

1.Data of Facility from customers

|    Feature    | Type    | Description                      |
|:-------------:|---------|----------------------------------|
|   Row Number  | INT     | Row number of record             |
|     ID        | Number  | ID of resident from customer     |
|   facilities  | list    | list of facility of resident     |

# EDA

Because the team has a lot of outstanding projects, the model design will be a sprint. In the first sprint, the information that the customer will be provided. In the part that is Numeric is used in the model design, there will be a step consisting of

1. total_units
2. bedrooms
3. total_units
4. bedrooms
5. baths
6. floor_area
7. floor_level
8. nearby_supermarkets
9. nearby_shops

And will add two more Feature that come from the calculation.

1. num_facility : It is a count of the number of facilities that the asset has.
2. closest_station_distance : Calculate from the information of the bus station whether it is near or not.

# Modeling

1. Linear regression
2. Linear regression with GridSearch
3. Ridge
4. Cross Validation with scaler (Use Pipeline)
5. Ridge with scaling
6. Ridge Regression with Grid-Search and Cross-Validation
7. Lasso

# Conclusion and Recommendations

From all 6 models, it will be found that the R-Square value of every type will not be more than 0.162. There will be a Linear Regression OLS model that can reach 0.163 and the model at the lowest score. Linear with scaling, which from the score may be enough to conclude that The information that may not be suitable for the prediction. Should find information that is catagory.
