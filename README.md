# Predicting Food Sales

**Author**: Hadassah Port

### Motive:

The purpose of this project was to help retailers determine what factors are important in increasing item sales.

### Data:

The dataset included features such as an item's weight, fat content, maximum retail price, and more (see data dictionary below). 
Data Dictionary:

Item_Identifier:	Unique product ID
Item_Weight:	Weight of product
Item_Fat_Content:	Whether the product is low fat or regular
Item_Visibility:	The percentage of total display area of all products in a store allocated to the particular product
Item_Type:	The category to which the product belongs
Item_MRP:	Maximum Retail Price (list price) of the product
Outlet_Identifier:	Unique store ID
Outlet_Establishment_Year:	The year in which store was established
Outlet_Size:	The size of the store in terms of ground area covered
Outlet_Location_Type:	The type of area in which the store is located
Outlet_Type:	Whether the outlet is a grocery store or some sort of supermarket
Item_Outlet_Sales: Sales of the product in the particular store. This is the target variable to be predicted.

### Results:

1. One important insight from the data was that most of the features did not have a strong correlation with one another. The only features with a moderate correlation were Item MRP and Item Outlet Sales. 

#### Correlations Heat Map
![corr](https://user-images.githubusercontent.com/101424304/165407752-92afa137-fc66-4869-b5e8-ecf724af47ac.png)

2. By examining the average sales per item type and comparing them to their average MRPs, there was a clear trend that indicated higher MRPs led to higher sales. 

#### Average Item MRP and Average Item Sales by Type
![mrp sales](https://user-images.githubusercontent.com/101424304/165407892-276ad148-e17c-4ca3-83fc-be1758e30dc4.png)

Two different models were tested to see which would perform best on this dataset — Linear Regression and Decision Tree. Ultimately, a decision tree with depth 5 performed best.

Decision Tree Metrics:
R^2 for Training: 0.6042066848171654
R^2 for Testing: 0.5960564372160061
MAE for Training: 761.9784955008363
MAE for Testing: 736.8796499354127
MSE for Training: 1171332.784431318
MSE for Testing: 1114471.1152767406
RMSE for Training: 1082.281287111312
RMSE for Testing: 1055.6851402178306

About 60% of the variance in y can be explained by the model. The RMSE 
is about 43% greater than the MAE, which could indicate that the model may be 
making some larger errors. However, the decision tree model beat the baseline model's performance.

Therefore, the decision tree model should be used for predicting item sales. It has better R^2
and RMSE values than the linear regression model. Additionally, the decision tree's
R^2 and RMSE values are relatively similar for the training and testing data, which
likely indicates that the model is not overfit.

### Final Recommendation:
My recommendation would be to increase MRPs for all items and then utilize the decision tree model to predict sales from the new MRPs.
