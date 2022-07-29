# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 5: Group Project
### A project by Ryan, Rick, and Sam

## The work

For this project, you will be doing work that focuses on social impact.

The prompts are there to help jump-start your ideation process. If you would like to change or combine prompts, that's fine! If you want to find your own idea, even better. **Consult your local instructor for final approval before getting started.**  

Remember to start with a good problem statement!

## Problem Statement
Obesity is an issue that affects people worldwide. While there are many factors that affect obesity rates, this project will utilize lifestyle survey data to predict if somebody is obese, and give personalized recommendations based on the factors that most contribute to their obesity.

Data:
* [`survey.csv`](./data/survey.csv): Dataset of Survey Results for Obesity in Mexico, Peru and Columbia from 2019 [source](https://archive.ics.uci.edu/ml/datasets/Estimation+of+obesity+levels+based+on+eating+habits+and+physical+condition+) 
* [`cleaned_cdc_2020.csv`](./data/cleaned_cdc_2020.csv): CDC Dataset of adult's diet, physical activity, and weight status from Behavioral Risk Factor Surveillance System. [source](https://chronicdata.cdc.gov/Nutrition-Physical-Activity-and-Obesity/Nutrition-Physical-Activity-and-Obesity-Behavioral/hn4x-zwk7) 

# CDC Data Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|**Year**|*int*|CDC|Year data collected|
|**LocationAbbr**|*str*|CDC|State Abbreviation|
|**LocationDesc**|*str*|CDC|State Name|
|**Data_Value**|*float*|CDC|Percentage of people with obesity|
|**Sample_Size**|*float*|CDC|Survey sample size|
|**GeoLocation**|*tuple*|CDC|Latitude and Longitude of State|
|**QuestionID**|*str*|CDC|ID for Questions|
|**StratificationCategoryId1**|*str*|CDC|Category ID for Stratifications|
|**StratificationID1**|*str*|CDC|Stratification ID|

# CDC Question Data Dictionary

|QuestionID|Question|Dataset|
|---|---|---|
|**Q036**|Percent of adults aged 18 years and older who have obesity|CDC|
|**Q037**|Percent of adults aged 18 years and older who have an overweight classification|CDC|
|**Q047**|Percent of adults who engage in no leisure-time physical activity|CDC|
|**Q046**|Percent of adults who engage in muscle-strengthening activities on 2 or more days a week|CDC|
|**Q043**|Percent of adults who achieve at least 150 minutes a week of moderate-intensity aerobic physical activity or 75 minutes a week of vigorous-intensity aerobic activity (or an equivalent combination)|CDC|
|**Q044**|Percent of adults who achieve at least 150 minutes a week of moderate-intensity aerobic physical activity or 75 minutes a week of vigorous-intensity aerobic physical activity and engage in muscle-strengthening activities on 2 or more days a week|CDC|
|**Q045**|Percent of adults who achieve at least 300 minutes a week of moderate-intensity aerobic physical activity or 150 minutes a week of vigorous-intensity aerobic activity (or an equivalent combination)|CDC|
|**Q018**|Percent of adults who report consuming fruit less than one time daily|CDC|
|**Q019**|Percent of adults who report consuming vegetables less than one time daily|CDC|


# CDC Stratification Data Dictionary

|StratificationCategory1|Stratification1|StratificationCategoryID1|StratificationID1|Dataset|
|---|---|---|---|---|
|**Age(years)**|18 - 24|AGEYR|AGEYR1824|CDC|
|**Age(years)**|25 - 34|AGEYR|AGEYR2534|CDC|
|**Age(years)**|35 - 44|AGEYR|AGEYR3544|CDC|
|**Age(years)**|45 - 54|AGEYR|AGEYR4554|CDC|
|**Age(years)**|55 - 64|AGEYR|AGEYR5564|CDC|
|**Age(years)**|65 or older|AGEYR|AGEYR65PLUS|CDC|
|**Education**|College graduate|EDU|EDUCOGRAD|CDC|
|**Education**|Some college or technical school|EDU|EDUCOTEC|CDC|
|**Education**|Less than high school|EDU|EDUHS|CDC|
|**Education**|High school graduate |EDU|EDUHSGRAD|CDC|
|**Gender**|Female|GEN|FEMALE|CDC|
|**Gender**|Male|GEN|MALE|CDC|
|**Income**|$15,000 - $24,999|INC|INC1525|CDC|
|**Income**|$25,000 - $34,999|INC|INC2535|CDC|
|**Income**|$35,000 - $49,999|INC|INC3550|CDC|
|**Income**|$50,000 - $74,999|INC|INC5075|CDC|
|**Income**|$75,000 or greater|INC|INC75PLUS|CDC|
|**Income**|Data not reported|INC|INCNR|CDC|
|**Race/Ethnicity**|2 or more races|RACE|RACE2PLUS|CDC|
|**Race/Ethnicity**|Asian|RACE|RACEASN|CDC||
|**Race/Ethnicity**|Non-Hispanic Black|RACE|RACEBLK|CDC|
|**Race/Ethnicity**|Hispanic|RACE|RACEHIS|CDC|
|**Race/Ethnicity**|Hawaiian/Pacific Islander|RACE|RACEHPI|CDC|
|**Race/Ethnicity**|American Indian/Alaska Native|RACE|RACENAA|CDC|
|**Race/Ethnicity**|Other|RACE|RACEOTH|CDC|
|**Race/Ethnicity**|Non-Hispanic White |RACE|RACEWHT|CDC|
|**Total**|Total|OVR|OVERALL|CDC|



#### Data Dictionary

<<<<<<< HEAD

Questions	Possible Answers
¿What is your gender?	
Female
Male

¿What is your age?	Numeric value

¿What is your height?	Numeric value in meters

¿What is your weight?	Numeric value in kilograms

¿Has a family member suffered or suffers from overweight?	
Yes
No

¿Do you eat high caloric food frequently?	
Yes
No

¿Do you usually eat vegetables in your meals?	
Never
Sometimes
Always

¿How many main meals do you have daily?	
Between 1 y 2
Three
More than three

¿Do you eat any food between meals?	
No
Sometimes
Frequently
Always

¿Do you smoke?	
Yes
No

¿How much water do you drink daily?	
Less than a liter
Between 1 and 2 L
More than 2 L

¿Do you monitor the calories you eat daily?	
Yes
No

¿How often do you have physical activity?	
I do not have
1 or 2 days
2 or 4 days
4 or 5 days

¿How much time do you use technological devices such as cell phone, videogames, television, computer and others?	
0–2 hours
3–5 hours
More than 5 hours

¿how often do you drink alcohol?	
I do not drink
Sometimes
Frequently
Always

¿Which transportation do you usually use?	
Automobile
Motorbike
Bike
Public Transportation
Walking
=======
| Feature | Type  | Question | Responses |
|------|------|--------|---------|
|Gender | category (one-hot encoded) | ¿What is your gender? | Female / Male |
|Age | object | ¿What is your age? | Numeric Value (years) |
|Height | object | ¿What is your height? | Numeric Value (meters) |
|Weight | object | ¿What is your weight? | Numeric Value (kg) |
|fam_hx_overweight | category | ¿Has a family member suffered or suffers from overweight? | Yes / No |
|high_cal_foods| category | ¿Do you eat high caloric food frequently? | Yes / No |
|vegetables| category | ¿Do you usually eat vegetables in your meals?| Never / Sometimes / Always |
|main_meals| object | ¿How many main meals do you have daily?| Numeric Value |
|food_bw_meals| category (one-hot encoded) | ¿Do you eat any food between meals? | No / Sometimes / Frequently / Always |
|smoke| category | ¿Do you smoke? | Yes / No |
|H2O| category | ¿How much water do you drink daily? | Less than a liter / Between 1 and 2 L / More than 2 L |
|monitor_cals| category | ¿Do you monitor the calories you eat daily? | Yes / No |
|physical_activity| category | ¿How often do you have physical activity? | None / 1 to 2 days / 2 to 4 days / 4 or more days |
|tech_use| category | ¿How much time do you use technological devices such as cell phone, videogames, television, computer and others? | 0-2 hours / 3-5 hours / More than 5 hours |
|alcohol| category (one-hot encoded) | ¿how often do you drink alcohol? | I do not drink / Sometimes / Frequently / Always |
|transport| category (one-hot encoded) | ¿Which transportation do you usually use? | Automobile / Motorbike / Bike / Public Transportation / Walking |
>>>>>>> 2aaf74b32ed1f7d1c88481ab8379e3e269c9a8be
