# Predicting Food Sales

**Author**: Hadassah Port

### Motive:

The purpose of this project was to help retailers determine what factors are important in increasing item sales.

### Results:

1. One important insight from the data was that most of the features did not have a strong correlation with one another. The only features with a moderate correlation were Item MRP and Item Outlet Sales. 

#### Correlations Heat Map
![corr](https://user-images.githubusercontent.com/101424304/165407752-92afa137-fc66-4869-b5e8-ecf724af47ac.png)

2. By examining the average sales per item type and comparing them to their average MRPs, there was a clear trend that indicated higher MRPs led to higher sales. 

#### Average Item MRP and Average Item Sales by Type
![mrp sales](https://user-images.githubusercontent.com/101424304/165407892-276ad148-e17c-4ca3-83fc-be1758e30dc4.png)

Two different models were tested to see which would perform best on this dataset — Linear Regression and Decision Tree. Ultimately, a decision tree with depth 5 performed best; it had R^2s of about 60% for the training and testing data. 

### Final Recommendation:
My recommendation would be to increase MRPs for all items and then utilize the decision tree model to predict sales from the new MRPs.
