# HousingPrediction
Flatiron Online DataScience Mod 2 Project
By: Steven Kyle

## Introduction/Abstract

The purpose of this project is to try and create a linear model for Housing Prices in King County. With this linear model we will be able to predict future housing prices. The features that are going to be used in this linear model will be discovered through EDA of an existing housing data set from King County.

### Main Questions

The main Questions that we are asking are:
1. Can we actually use a linear model to predict housing prices?
2. What features are important for evaluating a house?
3. How accurate can we get the model to be?

## Resources
### Files
- Jupyter Notebook
- Main Notebook: Main_Notebook.pynb
- King County Housing Dataset

### Packages
- statsmodels
- sklearn
- matplotlib
- numpy
- pandas
- scipy

## Final model including all the features
![alt text](https://github.com/stevenkyle2013/HousingPrediction/blob/main/Pictures/FinalModelSummary1.png)
![alt text](https://github.com/stevenkyle2013/HousingPrediction/blob/main/Pictures/FinalModelSummary2.png)
![alt text](https://github.com/stevenkyle2013/HousingPrediction/blob/main/Pictures/FinalModelSummary3.png)
![alt text](https://github.com/stevenkyle2013/HousingPrediction/blob/main/Pictures/FinalModelSummary4.png)
![alt text](https://github.com/stevenkyle2013/HousingPrediction/blob/main/Pictures/FinalModelSummary5.png)
![alt text](https://github.com/stevenkyle2013/HousingPrediction/blob/main/Pictures/FinalModelSummary6.png)
![alt text](https://github.com/stevenkyle2013/HousingPrediction/blob/main/Pictures/FinalModelQQPlot.png)
![alt text](https://github.com/stevenkyle2013/HousingPrediction/blob/main/Pictures/FinalModelHomoscedasticity.png)
![alt text](https://github.com/stevenkyle2013/HousingPrediction/blob/main/Pictures/FinalModelError.png)
![alt text](https://github.com/stevenkyle2013/HousingPrediction/blob/main/Pictures/FinalModelFull.png)


## Conclusion

*The numbers in the conclusion will slightly change every time the model is ran but they should all be generally the same*

In conclusion Linear Regression may not be the best modeling technique to use on predicting housing prices but it did a fairly decent job. In the end the final model used a logged form of the price (dependent variable) meaning that the trend is more likely exponential than linear. The final model has an Adj. R-squared value of 0.856. This means that 85.6% of the variation in price (dependent value) can be accounted by the model. The average error for the model is ~$100,000 which is 20% of the average price.

By looking at the Homoscedacisity Plot we can see that the model tends to overpredict values on the lower end of the market and under predict values on the higher end of the market. The QQ-plot shows that the residuals are not quite normally distributed and that it has light tails.

The features that were used in the final model are:

1. "zipcode" (categorical, varies greatly -.05 to 1.04)
2. "sqft_living" (0.46 increase in logged price for every 1 log increase in sqft)
3. "DistanceFromCenterOfSeattle" (-0.1757 increase in logged price for every 1 log increase in miles)
4. "view" (0.0648 increase in logged price for every view)
5. "grade" (0.1126 increase in logged price for 1 increase in grade)
6. "Condition" (0.0477 increase in logged price for 1 increase in condition)
7. "waterfront" (0.42	increase in logged price if it is on the waterfront)
8. "renovated" (0.0798 increase in logged price if if was renovated)
9. "floors" (-0.0188 increase in logged price for every floor)
10. "bathrooms" (0.0104 increase in logged price for every bathroom)

This model is also consistent when working with new data, the difference in Mean Error is only ~$2,000 from the training set and the testing set.

## Future Work
The future steps I want to take with this model is to look at school districts. I know school districts are important when buying houses and replacing zipcode with these districts might create a more accurate model.
