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
* [`cleaned_cdc.csv`](./data/cleaned_cdc.csv): CDC Dataset of adult's diet, physical activity, and weight status from Behavioral Risk Factor Surveillance System. [source](https://chronicdata.cdc.gov/Nutrition-Physical-Activity-and-Obesity/Nutrition-Physical-Activity-and-Obesity-Behavioral/hn4x-zwk7) 

####  Data Dictionary

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

## To Do: Format Questions into Table and Update Column names

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