# MechaCar_Statistical_Analysis
Using R and R Studio

# Background
A few weeks after starting his new role, Jeremy is approached by upper management about a special project. AutosRUs’ newest prototype, the MechaCar, is suffering from production troubles that are blocking the manufacturing team’s progress. AutosRUs’ upper management has called on Jeremy and the data analytics team to review the production data for insights that may help the manufacturing team.

In this challenge, you’ll help Jeremy and the data analytics team do the following:

Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes
Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots
Run t-tests to determine if the manufacturing lots are statistically different from the mean population
Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis, you’ll write a summary interpretation of the findings.

# What You're Creating
This new assignment consists of three technical analysis deliverables and a proposal for further statistical study. You’ll submit the following:

Deliverable 1: Linear Regression to Predict MPG
Deliverable 2: Summary Statistics on Suspension Coils
Deliverable 3: T-Test on Suspension Coils
Deliverable 4: Design a Study Comparing the MechaCar to the Competition

# Files
Use the following links to download the Challenge data sets.

Download the MechaCar MPG dataset (Links to an external site.).

Download the Suspension Coil dataset (Links to an external site.).

# Deliverable 1: Linear Regression to Predict MPG (30 points)
Deliverable 1 Instructions
The MechaCar_mpg.csv dataset contains mpg test results for 50 prototype MechaCars. The MechaCar prototypes were produced using multiple design specifications to identify ideal vehicle performance. Multiple metrics, such as vehicle length, vehicle weight, spoiler angle, drivetrain, and ground clearance, were collected for each vehicle. Using your knowledge of R, you’ll design a linear model that predicts the mpg of MechaCar prototypes using several variables from the MechaCar_mpg.csv file. Then, you’ll write a short interpretation of the multiple linear regression results in the README.md.

# Linear Regression to Predict MPG

1. Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?
When we run the Linear regression code we can see:

Lenght of an Automotive and its ground clearance are important factors that will impact milage. These will determine the drag and friction that will determine the energy required for forward propulsion and will provide non-random amounts of variance on the MechaCar prototype. But the weight + all wheel drive + spoiler angle can provide random amounts of varience in the data all based on the p-value.
![image](https://user-images.githubusercontent.com/96351897/163761737-d77d63fe-d5dd-435b-af2a-b5aaa9fb65dd.png)


2. Is the slope of the linear model considered to be zero? Why or why not?
 MechaCar has a p-Value: 5.35e-11 which is smaller than the significance level of 0.05%. The Evidence is enough to reject the null hypothesis, that means the slope of this linear model is not considered to be zero.

![image](https://user-images.githubusercontent.com/96351897/163761762-dfa9d0ee-ec88-434e-8874-27dbcb6a112d.png)


3. Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?
R Square is 0.7149 = 71% mpg variations due changes in vahicles length, weight, spoiler angle, AWD, ground clearance etc. Hence the linear model is not quiet efficient in predicting the Mpg of MechaCar. If these variables are removed the predictability reduces to r- squared value of 0.674 = 67% but then its much more efficient in predicting the Mpg of MechaCar prototypes due to lack of these variables.

![image](https://user-images.githubusercontent.com/96351897/163761797-35404223-57ca-4057-8697-7c2ef2c59913.png)


# Deliverable 2: Create Visualizations for the Trip Analysis (30 points)
Deliverable 2 Instructions
The MechaCar Suspension_Coil.csv dataset contains the results from multiple production lots. In this dataset, the weight capacities of multiple suspension coils were tested to determine if the manufacturing process is consistent across production lots. Using your knowledge of R, you’ll create a summary statistics table to show:

The suspension coil’s PSI continuous variable across all manufacturing lots
The following PSI metrics for each lot: mean, median, variance, and standard deviation.
Then, in the README.md, you’ll briefly detail and interpret the suspension coil summary statistics.

# Summary Statistics on Suspension Coils

1. The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?

Based on design specifications for MechaCar the variance of the suspension coils must not exceed 100 pounds per square inch however based on our findings the variance of the coils is 62.29 PSI, which is well within the requirements. In consideration of the different lots in Lot 1 the psi is 0.98 and in Lot 2 it is 7.47 and are more consistent compared to Lot 3 which is out of range for varience at psi of 170.29.
# Lot_Summary

![image](https://user-images.githubusercontent.com/96351897/163761856-f97f837e-84b8-412d-a09f-d03c0b977827.png)


![image](https://user-images.githubusercontent.com/96351897/163761893-82bcfda3-b986-42f7-a598-4c67e78756c8.png)

# Total_Summary

![image](https://user-images.githubusercontent.com/96351897/163761994-4fb84ee5-885d-48e8-8a41-64ce9581082a.png)


![image](https://user-images.githubusercontent.com/96351897/163762014-e276dbc5-227b-4feb-b3d4-3ee862fb9406.png)




# Deliverable 3: T-Tests on Suspension Coils (20 points)
Deliverable 3 Instructions
Using your knowledge of R, perform t-tests to determine if all manufacturing lots and each lot individually are statistically different from the population mean of 1,500 pounds per square inch.


## T-Tests on Suspension Coils

Total Summary
The mean is 1498.78, the p-Value is 0.06, and is higher than the common significance level of 0.05, the evidence is not enough for rejecting the null hypothesis. The data shows all means to be close to population mean of 1500.
![image](https://user-images.githubusercontent.com/96351897/163762080-e432406d-f872-473f-b071-c9d424d2fb47.png)

Lot Summary

Lot 1 has a mean of 1500, a p-Value of 1, we accept the null hypothesis because there is no significant difference in Lot 1 values and population mean.
![image](https://user-images.githubusercontent.com/96351897/163762096-a1edc852-e9f9-4285-a96a-5d90f62b12f6.png)

Lot 2 is fairly similar as well with a mean of 1500.02, a p-Value of 0.61; hence here as well we accept the the null hypothesis 
![image](https://user-images.githubusercontent.com/96351897/163762113-7283f3f6-1e98-4146-a298-95e3f216eb09.png)

Lot 3, has a sample mean of 1496.14, a p-Value of 0.04, which is lower than the significance level of 0.05. Here we will accept the null hypothesis because population mean and and sample mean are not different.
![image](https://user-images.githubusercontent.com/96351897/163762138-7a988707-ac14-490d-951f-0db1524470ac.png)


# Deliverable 4: Design a Study Comparing the MechaCar to the Competition (20 points)
Deliverable 4 Instructions
Using your knowledge of R, design a statistical study to compare performance of the MechaCar vehicles against performance of vehicles from other manufacturers.


# Study Design: MechaCar vs Competition.

Write a short description of a statistical study that can quantify how the MechaCar performs against the competition. In your study design, think critically about what metrics would be of interest to a consumer: for a few examples, cost, city or highway fuel efficiency, horse power, maintenance cost, or safety rating.




In your description, address the following questions:
1. What metric or metrics are you going to test?
Metrics to be tested:
1. cost- Variable based on features and Manufacturing constraints
2. city or highway fuel efficiency- Based on model, engine, shape, tires etc
3. horse power- engine type determines the power and torque this decision is dependent if its a commute car, all terrain, pickup etc.
4. maintenance cost- cars that are hybrid and electric have lower maintenance than fuel cars 
5. safety rating- crash testing, airbags, safety harnessas, safety receptors and computational features, geolocation for theft etc.


2. What is the null hypothesis or alternative hypothesis?

For the MechaCar:

Null Hypothesis: MechaCar price or features are similar to its competitors.
Alternative Hypothesis: MechaCar is NOT priced or featured similar to its competitors.


Each Hypothesis is dependent on performance metrics and has to be is statistically similar between the MechaCar prototype and all vehicle from the other manufacturers that fall in the same genre.

3. What statistical test would you use to test the hypothesis? And why?
A linear regression can be used to compare continuous numerical variables or metrics across a different groups of manufacturers including MechaCar.

Another way to do so is:-
ANOVA hypothesis testing
Analysis of variance, or ANOVA, is a method that separates observed variance data into different components to use for additional tests. A one-way ANOVA is used for three or more groups of data, to gain information about the relationship between the dependent and independent variables.

4. What data is needed to run the statistical test?

To perform the linear regression we would need a huge vairety if data from MechaCar and its competition, We will then compile it into a single dataframe place each metric adjacent in the column and then chart it on a linear plot. looking for similarities in data overlap between these companies and Mechacar and using color to distinguish Mechacar from the others. then we would look at the outliers and determine sources of bias as well as compare how they would perform or what finetuning the car would neet to have all vehicles produces with similar linear regression as other manufacturere. this will also help the manufacturer standardize its production quality in the long run.

