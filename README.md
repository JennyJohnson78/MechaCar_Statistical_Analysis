# MechaCar Statistical Analysis

AutosRUs' MechaCar is "suffering from production troubles" and upper management has called on the data analytics team to review the production data for insights that may help the manufacturing team. Below is a statisitical analysis of automobile performance with R.

## Linear Regression to Predict MPG

Linear Regression Model:

![image](https://user-images.githubusercontent.com/67409852/147899396-369f415b-1f38-4ed1-b29a-49fd6bb16b81.png)

Summary:

![image](https://user-images.githubusercontent.com/67409852/147899484-5152ec15-d271-454a-ba21-1041aceadb21.png)

- Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset? Vehicle length and ground clearance are the most significant variables in our dataset which show a non-random effect on the MPG of the MechaCar. Vehicle length and ground clearance resulted in p-values of 2.6x10-12 and 5.21x10-8, respectively.

- Because the p-value of 5.35x10-11, The slope of the linear model can not be considered to be zero. Therefore, the null hypothesis must be rejected, meaning the relationship between our variables and the miles per gallon is subject to more than random chance.

- The r-squared value of 0.7149, meaning the model is 71% accurate, so the model does predict the mpg of the MechaCar prototype somewhat effectively. 

## Summary Statistics on Suspension Coils

Total Summary:

![image](https://user-images.githubusercontent.com/67409852/147899669-935e65fe-e65e-4341-bb0f-9cd917b674b4.png)

Lot Summary:

![image](https://user-images.githubusercontent.com/67409852/147899935-5325199c-e3de-401c-83dc-f86b4925baf1.png)

- Overall variance is under 100 PSI meeting specifications, however the variance for Lot 3 is well over 100 PSI, at 170.28. Therefore lot 3 does not meet design specifications.

## T-Tests on Suspension Coils

PSI across all manufacturing lots:

![image](https://user-images.githubusercontent.com/67409852/147900212-54233d1f-c235-44e1-990a-35ecb5b9ccd5.png)

- The results of the t-test for the suspension coils spanning all manufacturing lots shows that they aren't statistically different from the population mean. Because the p-value is 0.0603, we cannot reject the null hypothesis.

PSI for manufacturing lot 1:

![image](https://user-images.githubusercontent.com/67409852/147900348-63e25512-caf7-44c7-8067-39552ed7e1a0.png)

- The t-test for the suspension coils for Lot 1 shows that they aren't statistically different from the population mean. The p-value is 1.00, thus not low enough to reject the null hypothesis.

PSI for manufacturing lot 2:

![image](https://user-images.githubusercontent.com/67409852/147900389-88ec6455-db1c-4c4e-b5d8-0f15874e7b25.png)

- As with Lot 1, the t-test for Lot 2 shows that they are not statistically different from the population mean. The p-value is 0.6072 and is not low enough to reject the null hypothesis.

PSI for manufacturing lot 3:

![image](https://user-images.githubusercontent.com/67409852/147900496-478f9247-2f50-426c-bdf9-78410f1de8cd.png)

- The t-test for the suspension coils for Lot 3 shows that they are slightly statistically different from the population mean. The p-value is 0.0417, which is just low enough to reject the null hypothesis. 

## Study Design: MechaCar vs Competition

A good statistical study to perform would be to predict values for maintenance cost using a linear model and values from cost. When buying a new car, maintenance costs can be a big determining factor to consumers. AutosRUs could use this study against competitors and increase sales for the company, as well as informing customers.

- Metric(s) to test: the r-squared value to determine if future data points would fit the model

- Null hypothesis: the slope of the linear model is zero

- Alternative hypothesis: the slope of the linear model is not zero

- Statistical test to use: a simple linear regression t-test

- Data needed to run test: the cost and maintenance cost of MechaCar prototypes
