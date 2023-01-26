# Final_Project_Bike_Pedestrian_Crash_Analysis


## Background

The data provided for this project is a collection of information on accidents involving bicyclists and pedestrians in North Carolina. It is sourced from police reports of collisions between bicycles and motor vehicles, as well as pedestrian and motor vehicle accidents that occurred on public roadways, vehicular areas, and private properties (if reported) from January 2007 to December 2019. The primary objective of this data is to gain a deeper understanding of the patterns and frequency of these types of accidents in the state, which can be used to inform the development of safety measures and policies aimed at reducing their occurrence.

## Dataset Description

- The dataset is collected from Kaggle website. The link for the data is https://www.kaggle.com/datasets/atharvaingle/bikepedcrash. Our dataset holds all of the information related to bike crash include the bike rider's information the driver's information and the other objective conditions such as weather and road conditions etc, which will allow us to understand the attributions that lead to the bike crash and coorelated circumastance. 

- We select this dataset to gather the main factors that cause the bike accidents and figure out the negative impact from them.

## Dataset Cleaning

- Drop Null values
- Renaming colunns
- Fill in certain age number with reasonable estimation 
-  Additional modification and deletion of data will be done during application of ML models

### Information for each crash includes: 

County, City, Crash Date, Crash Day, Crash Group, Crash Location, Crash Time, Crash Severity, Bike/Pedestrian Age Group, Bike/Pedestrian Alcohol Detected, Bike Direction, Bike/Pedestrian Injury, Bike/Pedestrian Position, Bike/Pedestrian Race, Bike/Pedestrian Sex, Ambulance Response, Driver Age Group, Driver Estimated Speed, Speed Limit, Driver Alcohol Detected, Driver Injury, Driver Race, Driver Sex, Driver Vehicle Type, Hit and Run, Development, Light Condition, Locality, Number of Lanes, Road Characteristics/Class/Condition/Configuration, Road Defects/Features, Traffic Control, Crash Type, and/or Weather.


## Objective

The main objective of this data is to analyze patterns and frequency of Serious & Fatal accidents in the state, in order to implement safety measures and policies that reduce their occurrence. We plan to utilize supervised Machine Learning techniques to identify the root causes of these accidents and develop strategies for prevention.

## List of Tools
- SQL
- Python
- R
- Tableau

## Data Exploration
- Crash Reports  - No of accidents considering the given parameters (County,City Speedlimit, City, Agegroup, Gender )
- Visualization of crash reports using latitude and longitudes and creating heat maps
- Yearly wise , Monthly , Weekly crash reports  

## Proposed Machine Learning Model
- Our model is going to predict the severity of injury by Bikecrash with relevant parameters. We will examine the statistical relationship of the data set's features to determine the coorelation among the possible attributions for bike crash. Then we apply a linear regression model to predict the severity of injury.
