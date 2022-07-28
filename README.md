# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 5: Group Project
### BY: Ryan Pedersen, Rick Powell, Samuel Hewitt

## Problem Statement
Obesity is an issue that affects people worldwide. While there are many factors that affect obesity rates, this project will utilize lifestyle survey data to predict if somebody is obese, and give personalized recommendations based on the factors that most contribute to their obesity.

## Data:
* [`survey.csv`](./data/survey.csv): Dataset of Survey Results for Obesity in Mexico, Peru and Columbia from 2019 [source](https://archive.ics.uci.edu/ml/datasets/Estimation+of+obesity+levels+based+on+eating+habits+and+physical+condition+) 
* [`cleaned_cdc.csv`](./data/cleaned_cdc.csv): CDC Dataset of adult's diet, physical activity, and weight status from Behavioral Risk Factor Surveillance System. [source](https://chronicdata.cdc.gov/Nutrition-Physical-Activity-and-Obesity/Nutrition-Physical-Activity-and-Obesity-Behavioral/hn4x-zwk7) 



#### Data Dictionary

=======
| Feature | Type  | Question | Responses |
|------|------|--------|---------|
|Gender | category (one-hot encoded) | ¿What is your gender? | Female / Male |
|Age | float | ¿What is your age? | Numeric Value (years) |
|Height | float | ¿What is your height? | Numeric Value (meters) |
|Weight | float | ¿What is your weight? | Numeric Value (kg) |
|fam_hx_overweight | category | ¿Has a family member suffered or suffers from overweight? | Yes / No |
|high_cal_foods| category | ¿Do you eat high caloric food frequently? | Yes / No |
|vegetables| category | ¿Do you usually eat vegetables in your meals?| Never / Sometimes / Always |
|main_meals| int | ¿How many main meals do you have daily?| Numeric Value |
|food_bw_meals| category (one-hot encoded) | ¿Do you eat any food between meals? | No / Sometimes / Frequently / Always |
|smoke| category | ¿Do you smoke? | Yes / No |
|H2O| category | ¿How much water do you drink daily? | Less than a liter / Between 1 and 2 L / More than 2 L |
|monitor_cals| category | ¿Do you monitor the calories you eat daily? | Yes / No |
|physical_activity| category | ¿How often do you have physical activity? | None / 1 to 2 days / 2 to 4 days / 4 or more days |
|tech_use| category | ¿How much time do you use technological devices such as cell phone, videogames, television, computer and others? | 0-2 hours / 3-5 hours / More than 5 hours |
|alcohol| category (one-hot encoded) | ¿how often do you drink alcohol? | I do not drink / Sometimes / Frequently / Always |
|transport| category (one-hot encoded) | ¿Which transportation do you usually use? | Automobile / Motorbike / Bike / Public Transportation / Walking |

## Modeling:

### Survey Regression Model:

The goal of the regression model was to predict a person's weight based upon their answers in the survey. The best performing model was random forest. Feature engineering was performed by creating 2nd degree polynomial features on height, high_cal_foods, vegetables, main_meals, and h2o columns. This model had a mean squared error of 94.9 and a training and testing r2 score of .987 and .866 respectively.

### CDC Regression Model:

The goal of the regression model was to predict a state's obesity percentage based on diet and exercise habits. The best performing model was knn with n = 8 with a mean squared error of 6.46. The r2 for the training and testing sets were .670 and .592 respectively.  

## Conclusion:

Daily Exercise and a Healthy diet are obvious ways to reduce obesity, but simple lifestyle changes such as biking or walking to work (if possible), or monitoring the calories you eat can help manage your weight.


## Next Steps:

We could improve our results with more data points, our survey had over 2000 responses, but our models and predictions would have been better with more data.
