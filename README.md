# MechaCar_Statistical_Analysis

# Deliverable 1:

## Linear Regression to Predict MPG

Test results for 50 prototype MechaCars in the MechaCar_mpg.csv dataset. The prototypes for MechaCar were produced using multiple design specifications to identify ideal vehicle performance. The metrics that were collected for each vehicle included vehicle length, vehicle weight, spoiler angle, drivetrain, and ground clearance. A linear model was designed in R Studio to predict the mpg of MechCar prototypes using multiple cariables from the MechaCar_mpg.csv file.

### Requirements:

The below requirements have been completed:
     -	The MechaCar_mpg.csv file was imported and was read in a dataframe
     -	An RScript was written for a linear regression model on all six variables (vehicle length, vehicle weight, spoiler angle, drivetrain, and ground clearance)
     -	An RScript was written to create the statistical summary of the linear regression model with the intended p-values
     -	A summary addresses the three following questions:
          1.	Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?
          2.	Is the slope of the linear model considered to be zero? Why or why not?
          3.	Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?

### Results:

![Deliverable1_results]( https://github.com/fletchrk/MechaCar_Statistical_Analysis/blob/main/Resources/Deliverable1_results.PNG)

### Summary:

1.	Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?
     -	The variables/coefficients that appears to have a non-random amount of variance to the mpg values is the vehicle length and vehicle ground clearance, though they have a significant impact on miles per gallon. The p-Values for the vehicle weight, spoiler angle and All Wheel Drive (AWD) indicate a random amount of variance in the dataset.
2.	Is the slope of the linear model considered to be zero? Why or why not?
     -	The slope of the linear model is not considered to be zero. The reason why is that the p-Value (5.35e-11) is much smaller than the significance level of 0.05%, which indicates that the slope of the linear model is not zero.
3.	Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?
     -	The linear model does predict mpg of MechaCar prototypes effectively. The reason why is that the linear model has an r-squared value of 0.7149, which is approximately 71% of all mpg predictions.

# Deliverable 2:

## Summary Statistics on Suspension Coils

The results from multiple production lots is in the Suspension_Coil.csv dataset. The dataset contains the weight capacities of multiple suspension coils that were tested to determine if the manufacturing process is consistent across production lots. Using RStudio a summary statistics table was created to show: 
1.	The suspension coil’s PSI continuous variable across all manufacturing lots
2.	The following PSI metrics for each lot: mean, median, variance, and standard deviation.

### Requirements:

The below requirements have been completed:
-	The Suspension_Coil.csv file was imported and read into a dataframe
-	An RScript was written to create a total summary dataframe that shows the mean, median, variance, and standard deviation of the PSI for all manufacturing lots
-	An RScript was written to create a lot summary dataframe that shows the mean, median, variance, and standard deviation of the PSI for each manufacturing lot (3)
-	A summary addressed the design specification requirement for all the manufacturing lots and each lot individually.

### Results

#### total_summary dataframe of all manufacturing lots:
![total_summary]( https://github.com/fletchrk/MechaCar_Statistical_Analysis/blob/main/Resources/total_summary.png)

#### lot_summary dataframe of 3 manufacturing lots:
![lot_summary]( https://github.com/fletchrk/MechaCar_Statistical_Analysis/blob/main/Resources/lot_summary.png)

### Summary

The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?
-	The total_summary dataframe shows that at all the manufacturing lots the PSI is 62.29 which is way within the 100 PSI variance requirement.
-	The lot_summary dataframe shows that at Lot1 and Lot2 are within the 100 PSI variance requirement. Lot1 is at 0.98 while Lot2 is at 7.47. Unfortunately, Lot3 is way above the 100 PSI variance requirement at it is at 170.29. 

# Deliverable 3:

## T-Tests on Suspension Coils

T-Tests were performed to determine if all the manufacturing lots and each individual log are statistically different for the population mean of 1,500 poinds per square inch.

### Requirements:

The below requirements have been completed:
     -	An R-Script was written on a t-test that was performed that compared all the manufacturing lots against the mean PSI of the population.
     -	An R-Script was written for three t-tests that compared each manufacturing lot against mean PSI of the population.
     -	A summary was written for the results of the t.tests for all manufacturing lots and for each of the 3 lots.

### Summary:

The first t.test for all lots shows that the mean of the sample is 1498.78 with a p-Value of 0.06. With the p-Value being slightly higher that the common significance level of 0.05, I feel that there is not enough evidence to support rejecting the null hypothesis because the mean of all manufacturing lots is like the presumed population mean of 1500.

![ttest_alllots]( https://github.com/fletchrk/MechaCar_Statistical_Analysis/blob/main/Resources/ttest_alllots.png)

Lot 1 t.test has a sample mean of 1500 with a p-Value of 1. Due to the observed sample mean and the presumed population mean the same, I think that we cannot reject the null hypothesis.

![ttest_lot1](https://github.com/fletchrk/MechaCar_Statistical_Analysis/blob/main/Resources/ttest_lot1.png)

Lot 2 t.test has a sample mean of 1500.02 with a p-Value of 0.61. The null hypothesis should not be rejected as the sample mean is 1500 which is the same as the presumed population of 1500.

![ttest_lot2](https://github.com/fletchrk/MechaCar_Statistical_Analysis/blob/main/Resources/ttest_lot2.png)

Lot 3 is a slightly different case. The sample mean is 1496.14 with the p-Value at 0.04 which means that it is slightly lower than both the presumed population of 1500 and the common significance level of 0.05. With the results being slightly lower, I fell that the null hypothesis should be rejected for lot 3.

![ttest_lot3]( https://github.com/fletchrk/MechaCar_Statistical_Analysis/blob/main/Resources/ttest_lot3.png)

# Deliverable 4:

## Study Design: MechaCar vs Competition

A statistical study was performed to compare performance of the MechaCar vehicles against performance of vehicles from other manufacturers.

### Requirements:

The below requirements have been completed:
     -	A metric to be tested was mentioned
     -	A null hypothesis or an alternate hypothesis is described
     -	A statistical test is described to test the hypothesis
     -	The data for the statistical test is described.

### Summary:

AutoRUs wants to guarantee to their customers that are getting the best value for their vehicles over their competitors. The rate of depreciation is going to get measured for MechaCars versus other manufacturers.

#### Metric

The metric that is going to be tested is the rate of depreciation, which is the value of a vehicle over time).

#### Hypothesis

Null hypothesis: The rate of depreciation at AutoRUS on MechaCars is the same as competitors.
Alternative hypothesis: The rate of depreciation at AutoRUs on MechCars is not the same as competitors.

#### Statistical Test

The statistical test I recommend would be a multiple linear regression test to help predict the rate of depreciation on MechaCars.

#### Data needed

The analysts will need the following data to be able to perform multiple linear regression to predict rate of depreciation: vehicle make/model, vehicle mileage, vehicle condition, and the current fair market value of the vehicle.
