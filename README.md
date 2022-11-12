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

* In the summary output, each Pr(>|t|) value represents the probability that each coefficient contributes a random amount of variance to the linear model.the result shows the indepedent variables vehicle_length and ground_clearance (as well as intercept) are statistically unlikely to provide random amounts of variance to the linear model.Only the vehicle_length and ground_clearance have a significant impact on mpg. The intercept is statistically significant  and it is not zero, which means that there is a significant amount of variability in the dependent variable when all independent vairables are equal to zero.

This multiple linear model has an r-squared value of 0.7149, which means that approximately 71% of all mpg predictions will be determined by this model. Relatively speaking, this multiple regression model will strongely predict mpg of MechaCar prototypes .

when i  removed the less significant and unimpactful independent variables (vehicle weight, spoiler angle, and All Wheel Drive), the predictability of the model decresed, but not drastically: the model`s r-squared value falls from 0.7149 to 0.674.

![image](https://user-images.githubusercontent.com/64270455/201454798-f1c15238-6139-4e19-a245-8c806ae92795.png)
         
![image](https://user-images.githubusercontent.com/64270455/201454845-edafa19e-64e9-4d6b-ace8-5cafd59ebc35.png)

### Summary Statistics on Suspension Coils
   ![image](https://user-images.githubusercontent.com/64270455/201456525-1202ba01-afe9-42ea-bfc0-645a276c6152.png)
   
   ![image](https://user-images.githubusercontent.com/64270455/201456580-203f051f-ce07-4dce-a517-e605de4b733d.png)
   
   The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch.
   The current manufacturing does data meet this design specification for all manufacturing lots in total but not each all individual lot because in the total            summary, the current variance is approximately 76.23 PSI meaning that is does meet the design specification. When looking at the lots individuals, the first
   two lotas meet the design specification at a varaince of approximately 1.14 PSI and 10.13 PSI respectfully, but the third lot does not. This is becasue the third      lot's variance is approximately 220.01 PSI, exceeding the design specification by more than double the alotted amount. Therefore, the manufacturing team should        work with the cars in lots 1 and 2 compared to those in lot 3.
   
#### T-Tests on Suspension Coils 
    ![image](https://user-images.githubusercontent.com/64270455/201488430-9c8d249e-764c-421f-89f9-664c93b50aa4.png)
    
    From the result we can see the true mean of the sample is 1498.78, which we also saw in the summary statistics above. With a p-Value of 0.06, which is higher than     the common significance level of 0.05, there is NOT enough evidence to support rejecting the null hypothesis. we invariably saying the mean of all three of these     manufacturing lots is statistically similar to the presumed population mean of 1500.
    
    But when each of the lots are considered,
       * Lot 1 with the true sample mean of 1500, and a p-Value of 1,  we cannot reject (i.e. accept) the null hypothesis that there is no statistical difference               between the observed sample mean and the presumed population mean (1500).
       * Lot 2  with a sample mean of 1500.02, a p-Value of 0.61; the null hypothesis cannot be rejected, and the sample mean and the population mean of 1500 are               statistically similar.
       *  However, Lot 3,which the sample mean is 1496.14 and the p-Value is 0.04, which is lower than the common significance level of 0.05. we can reject                     the null hypothesis that this sample mean and the presumed population mean are not statistically different.


    ![image](https://user-images.githubusercontent.com/64270455/201457579-c9d5cbed-2a33-4c82-bc7f-2dfb5a485e97.png)

    ![image](https://user-images.githubusercontent.com/64270455/201457639-6e3ed24e-182a-4c46-96a5-c956919910a2.png)
    
    ![image](https://user-images.githubusercontent.com/64270455/201457700-de7ef2d9-3d72-4b65-a7e8-cc93835a88d8.png)
    
    ##### Study Design: MechaCar vs Competition
    The statistical study design has the following:
     * A metric to be tested is mentioned
     * A null hypothesis or an alternative hypothesis is described
     * A statistical test is described to test the hypothesis
     
     This study would involve collecting data on MechaCar and its comparable models across several different manufacturers over the last 3 years.
     * What are the competitions' comparable models,
     * Which cars will MechaCar be competing with head-to-head? which cars will be included in the study?
     * Which factors will look at the study to determine the relevant to selling price?
     
     *Metrics
      Collecting data for comparable models across all major manufacturers for past 3 years for the following metrics:
      Safety Feature Rating
     Current Price (Selling)
     Drive Package
     Engine (Electric, Hybrid, Gasoline / Conventional)
     Resale Value
     Average Annual Cost of ownership
     MPG
     Hypothesis: Null and Alternative
     After determining which factors are key for the MechaCar's genre:

     Null Hypothesis (Ho): MechaCar is  not priced correctly based on its performance of key factors compared to compititors
     Alternative Hypothesis (Ha): MechaCar is priced correctly based on performance of key factors compared to compititors.
     Statistical Tests
     A multiple linear regression would be used to determine the factors that have the highest correlation/predictability with the list selling price (dependent            variable); which combination has the greatest impact on the price  

     
     



