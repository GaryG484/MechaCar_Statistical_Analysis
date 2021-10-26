
## Overview
##### Given data from the company MechaCar I was tasked with: creating a linear regression to predict MPG of prototypes, summarize statistics on their suspension coils, create a T-Test on the suspension coils, and design a study comparing the MechaCar products to the competitions models. 
## Linear Regression to Predict MPG
##### After importing the CSV file [MechCar MPG dataset](https://github.com/GaryG484/MechaCar_Statistical_Analysis/blob/main/R_Analysis/MechaCar_mpg.csv) I ran a multiple linear regression using all six column variables from the CSV file. 
##### Linear Results:
![Alttext](https://github.com/GaryG484/MechaCar_Statistical_Analysis/blob/main/Resources/Linear_Regression_Results.JPG)
* Of the six variables vehicle length and vehicle ground clearance are statistically likely to provide non-random amounts of variance to the mpg values in the dataset. 
* The p-Value found in the summary is 5.35e-11 (0.0000000000535). Anything less than 0.05 is enough evidence to reject our null hypothesis. As we have rejected our null hypothesis this leaves us with the alternative that the slope of this linear model is not zero. 
* r = 0.7149.  This indicates that roughly 71 percent of all mpg predictions can be predicted by this model. Since anything over 70 percent for an r value is considered a strong indicator, this linear model can be used to predict mpg of the MechaCar prototypes effectively. 
## Summary Statistics on Suspension Coils
##### After importing the CSV file [Suspension coil dataset]( https://github.com/GaryG484/MechaCar_Statistical_Analysis/blob/main/R_Analysis/Suspension_Coil.csv) I ran a multiple linear regression using the three column variables from the CSV file. Using this data I created two summary statistics tables: one to show the suspension coil’s PSI continuous variable across all manufacturing lots that I titled total_summary, and a second table to show the PSI metrics for each lot that I titled lot_summary.
##### total_summary:
![Alttext](https://github.com/GaryG484/MechaCar_Statistical_Analysis/blob/main/Resources/total_summary.JPG)
##### lot_summary:
![Alttext](https://github.com/GaryG484/MechaCar_Statistical_Analysis/blob/main/Resources/lot_summary.JPG)
##### The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. When looking at the entire production lot there is a variance of the coils equal to 62.69 PSI which is within the variance requirement. 

##### When we look at individual lots, we see a that two of the variables, lot 1 and lot 2, only have a variance of 0.98 PSI and 7.47 PSI respectively. Lot 3 is showing a variance of 170.29, which is outside of the variance requirement. In conclusion, while the manufacturing data shows that most of the production meets design specification, lot three is an outlier and does not.
## T-Tests on Suspension Coils
![Alttext](https://github.com/GaryG484/MechaCar_Statistical_Analysis/blob/main/Resources/t-test.JPG)
##### Using the Suspension coils CSV data set, I performed t-tests to determine if all manufacturing lots and each lot individually are statistically different from the population mean of 1,500 PSI. I performed a t-test on the entire population, as well as individual t-tests on each subset lot. 
##### The t-test for the entire population has a p-Value of 0.6028. This is higher than 0.05 which indicates there is not enough evidence to support rejecting the null hypothesis. This means that the mean of x, 1498.78, is statistically similar the presumed population mean of 1500.
##### Individual lots [1:3]
•	Lot 1 – The sample mean of this lot is 1500. The p-Value of lot one is equal to 1 which is higher than 0.05, meaning that we cannot reject the null hypothesis as there is no statistical difference in this subset and the presumed population mean of 1500. 

![Alttext](https://github.com/GaryG484/MechaCar_Statistical_Analysis/blob/main/Resources/One_Sample_T_Test.JPG)


•	Lot 2 – The sample mean of this lot is 1500.2. The p-Value of lot two is equal to 0.6072 which is higher than 0.05, meaning that we also cannot reject the null hypothesis as there is no statistical difference in this subset and the presumed population mean of 1500.

![Alttext](https://github.com/GaryG484/MechaCar_Statistical_Analysis/blob/main/Resources/One_Sample_T_Test2.JPG)


•	Lot 3 – The sample mean of this lot is 1496.14. the p-Value of lot three is equal to 0.04168 which is lower than 0.05, meaning that we can reject the null hypothesis as this sample indicates a statistical difference in this subset and the presumed population mean of 1500. 

![Alttext](https://github.com/GaryG484/MechaCar_Statistical_Analysis/blob/main/Resources/One_Sample_T_Test3.JPG)

##### In summary lot 3 is an outlier and should be checked for defects in the manufacturing process. It is outside the acceptable tolerance for product variance and there must be an error that needs to be corrected. 
## Study Design: MechaCar vs Competition
##### To compare the performance of the MechaCar vehicles against the performance of vehicles from other manufacturers based on the acceleration ability of the machines and their MPG rating. This will show that for each mile gained per gallon in the MechaCar vehicles, the product loses less performance ability than the competition. 
##### Several variables will be considered to test the metric of acceleration and MPG. 
*	City MPG (Independent variable.)

*	HWY MPG (Independent variable.)

*	Acceleration in 60 seconds (Independent variable.)

*	Towing power (Independent variable.)

*	Vehicle Price (Dependent variable.)

##### Hypothesis: MechaCar has a better value based on a performance and fuel efficiency to cost ratio.
##### Null hypothesis: MechaCar does not have a better value based on a performance and fuel efficiency to cost ratio. 
##### The data that we would use is test this hypothesis would be the abovementioned variables for all currently produced MechaCar vehicles and the top five closest competitors’ current production line.   We would run a multiple regression model to make sure there is more of a correlation for savings when there is a performance drop and a decrease in correlation for cost rising when MPG decreases. 
