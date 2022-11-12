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
  lm(mpg~vehicle_length +vehicle_weight + spoiler_angle + ground_clearance + AWD,data=MechaCar)
  Call:
  lm(formula = mpg ~ vehicle_length + vehicle_weight + spoiler_angle + 
    ground_clearance + AWD, data = MechaCar)

  Coefficients:
     (Intercept)    vehicle_length    vehicle_weight     spoiler_angle  ground_clearance               AWD  
      -1.040e+02         6.267e+00         1.245e-03         6.877e-02         3.546e+00        -3.411e+00 
 
  summary(lm(mpg~vehicle_length +vehicle_weight + spoiler_angle + ground_clearance + AWD,data=MechaCar)) 
  Call:
  lm(formula = mpg ~ vehicle_length + vehicle_weight + spoiler_angle + 
    ground_clearance + AWD, data = MechaCar)

  Residuals:
     Min       1Q   Median       3Q      Max 
 -19.4701  -4.4994  -0.0692   5.4433  18.5849 

 Coefficients:
                   Estimate Std. Error t value Pr(>|t|)    
(Intercept)      -1.040e+02  1.585e+01  -6.559 5.08e-08 ***
vehicle_length    6.267e+00  6.553e-01   9.563 2.60e-12 ***
vehicle_weight    1.245e-03  6.890e-04   1.807   0.0776 .  
spoiler_angle     6.877e-02  6.653e-02   1.034   0.3069    
ground_clearance  3.546e+00  5.412e-01   6.551 5.21e-08 ***
AWD              -3.411e+00  2.535e+00  -1.346   0.1852    
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Residual standard error: 8.774 on 44 degrees of freedom
Multiple R-squared:  0.7149,	Adjusted R-squared:  0.6825 
F-statistic: 22.07 on 5 and 44 DF,  p-value: 5.35e-11

From the above output,i can infer:

* The p-Value for this model,p-Value: 5.35e-11, is much smaller than the assumed significance level of 0.05%. This indicates there is sufficient evidence to reject our null hypothesis.

* In the summary output, each Pr(>|t|) value represents the probability that each coefficient contributes a random amount of variance to the linear model.the result shows the indepedent variables vehicle_length and ground_clearance (as well as intercept) are statistically unlikely to provide random amounts of variance to the linear model.Only the vehicle_length and ground_clearance have a significant impact on mpg. When an intercept is statistically significant, it means that the intercept term explains a significant amount of variability in the dependent variable when all independent vairables are equal to zero.

This linear model has an r-squared value of 0.7149, which means that approximately 71% of all mpg predictions will be determined by this model. Relatively speaking, this multiple regression model will strongely predict mpg of MechaCar prototypes .

when i  removed the less significant and unimpactful independent variables (vehicle weight, spoiler angle, and All Wheel Drive), the predictability of the model decresed, but not drastically: the model`s r-squared value falls from 0.7149 to 0.674.

lm(mpg ~ vehicle_length + ground_clearance, data=MechaCar)

Call:
lm(formula = mpg ~ vehicle_length + ground_clearance, data = MechaCar)

Coefficients:
     (Intercept)    vehicle_length  ground_clearance  
         -91.557             6.081             3.567 
         
summary(lm(mpg ~ vehicle_length + ground_clearance, data=MechaCar))
Call:
lm(formula = mpg ~ vehicle_length + ground_clearance, data = MechaCar)

Residuals:
    Min      1Q  Median      3Q     Max 
-17.493  -7.705   1.344   6.642  18.500 

Coefficients:
                 Estimate Std. Error t value Pr(>|t|)    
(Intercept)      -91.5573    13.9649  -6.556 3.86e-08 ***
vehicle_length     6.0811     0.6732   9.033 7.68e-12 ***
ground_clearance   3.5669     0.5401   6.604 3.26e-08 ***
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Residual standard error: 9.078 on 47 degrees of freedom
Multiple R-squared:  0.674,	Adjusted R-squared:  0.6601 
F-statistic: 48.59 on 2 and 47 DF,  p-value: 3.637e-12
