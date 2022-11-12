 # MechaCar_Statistical_Analysis
 # Overview of the Project 
    The purpose of this project is to review the production data for insights that might help the manufacturing team to overcome production troubles 
    blocking their progress.
   
    The Analysis include the following:
    * Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes
    * Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots
    * Run t-tests to determine if the manufacturing lots are statistically different from the mean population
    * Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers.  

## Linear Regression to Predict MPG
  ![image](https://user-images.githubusercontent.com/64270455/201454707-f9405cc9-108c-480b-bcde-2ae6fa8843a2.png)
 
  ![image](https://user-images.githubusercontent.com/64270455/201454675-df1af9ef-e8ec-41a1-b6ab-32ff77588e7b.png)

From the above output,i can infer:

* The p-Value for this model,p-Value: 5.35e-11, is much smaller than the assumed significance level of 0.05%. This indicates there is sufficient evidence to reject our null hypothesis.

* In the summary output, each Pr(>|t|) value represents the probability that each coefficient contributes a random amount of variance to the linear model.the result shows the indepedent variables vehicle_length and ground_clearance (as well as intercept) are statistically unlikely to provide random amounts of variance to the linear model.Only the vehicle_length and ground_clearance have a significant impact on mpg. When an intercept is statistically significant, it means that the intercept term explains a significant amount of variability in the dependent variable when all independent vairables are equal to zero.

This multiple linear model has an r-squared value of 0.7149, which means that approximately 71% of all mpg predictions will be determined by this model. Relatively speaking, this multiple regression model will strongely predict mpg of MechaCar prototypes .

when i  removed the less significant and unimpactful independent variables (vehicle weight, spoiler angle, and All Wheel Drive), the predictability of the model decresed, but not drastically: the model`s r-squared value falls from 0.7149 to 0.674.

![image](https://user-images.githubusercontent.com/64270455/201454798-f1c15238-6139-4e19-a245-8c806ae92795.png)
         
![image](https://user-images.githubusercontent.com/64270455/201454845-edafa19e-64e9-4d6b-ace8-5cafd59ebc35.png)
