# MechaCar_Statistical_Analysis
Using statistical analysis to help production issues for AutosRUs

## Deliverable 1: Linear Regression to Predict MPG

### 1.Statistical Significance
Using a 95% confidence level we can determine that three of the variables were statistically significant - having non-random amount of variance to the mpg balues in the dataset.

![R Significance](Resources/RSignificance.png)

Vehicle_length, vehicle_weight, and ground_clearance all show p-values less that .05 and therefore are statistically significant for prediction of mpg. 

### 2.Slope of the Linear Model
When we examine the slope of the linear model we can see that none of the slopes of variables are shown to be zero.

![R Coefficients](Resources/RCoefficients.png)

While vehicle_weight is approaching zero the rest show no doubt of being shown to be non-zero.

### 3.Effectiveness of the Linear Model in Prediction
The multi R-squared for the model is .7149, with the adjusted R-squared being 0.6825. Both of these are very good indicators for the validity of prediction. This model should be effective. There are other consideration that should be made before using this model exclusively and more data should be examined.

![R Squared](Resources/RSquared.png)

## Deliverable 2: Summary Statistics on Suspension Coils

### Total Summary
Here we can see the summary statistics for all the of the manufacturing lots. 

![Total Summary](Resources/total_summary.png)

### Summary by Lot Number
When we split the data into lot numbers we get the following summary statistics.

![Lot Summary](Resources/lot_summary.png)

When we examine the variance of the total manufacturing lot we see that the variance is less than 100. Which means that this manufacturing should pass inspection. However when we split the summary statistics into the three individual lots we can see that Lot 3 has significantly higher variance than Lot 1 and Lot 2, and is above the accepted variance at 170.2. This lot should be taken out of manufacturing and examined to find the source of the variace. Lot 3 should not be put into the manufacturing line.

## Deliverable 3: T-Tests on Suspension Coils

### T-Test on All Lots

![T-Test All](Resources/ttest_all.png)

The T-Test on all manugacturing lots showed a p-value of .6028, with an alpha of .05. With the p-value being above .05 this lot is not statistically significant from the normal distribution. The mean also falls within the 95% confidence interval.

### T-Test Lot 1

![T-Test Lot1](Resources/ttest_lot1.png)

The T-Test for Lot 1 gave a p-value of 1 with an alpha of .05. The p-value is above .05 and is therefore not statistically significant from the normal distribution and the mean falls within the 95% confidence interval. 

### T-Test Lot 2

![T-Test Lot2](Resources/ttest_lot2.png)

The T-Test for Lot 1 gave a p-value of .6072 with an alpha of .05. The p-value is above .05 and is therefore not statistically significant from the normal distribution and the mean falls within the 95% confidence interval.

### T-Test Lot 3

![T-Test Lot3](Resources/ttest_lot3.png)

Lot 3's T-Test returned a p-value of .04168 at the alpha .05. This means that it is statistically significant from the normal distribution, even if the mean falls within the 95% confidence interval.

3 out of the 4 T-tests suggest a normal distribution and therefore there is not sufficient evidence to reject the null hypothesis. which shows the means as statistically similar.


## Study Design

When comparing MechaCar to other car manufacturers further points of analysis that could prove fruitful could be the horsepower, torque, and cargo capacity. The null hypothesis for these points of analysis would be that these different aspects of the cars would have no effect on mpg of MechaCar's vehicles. An alterative hypothesis could be that these aspects have a negative impact on the mpg of MechaCar's vehicles. These three new dimensions of data would work well in a multiple linear regression model to show how these variable impact not only mpg, but also each other and the cars of MechaCar's competitors. Finally, for this study to take place we would need a random sample of data for vehicles of both MechaCar and its competitors vehicles. Ideally, the data set would be greater than 50 data points and contain a data on all three variables for all the vehicles.This way would would be able to use the data with RStudio and be confident with the results we got from the models.
