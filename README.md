# Final_Project_Bike_Pedestrian_Crash_Analysis
We are doing this as part of our final project requirement for the Data Analytics Boot Camp.

## Background

The data provided allows users to visualize the locations of accidents involving bicyclists and pedestrians in North Carolina. It is sourced from police reports of collisions between bicycles and motor vehicles and pedestrian and motor vehicle accidents that occurred on public roadways, vehicular areas, and private properties (if reported) from January 2007 to December 2019. The primary purpose of this data is to provide insights into the patterns and frequency of these types of accidents in the state that can help develop safety measures and policies.

## Dataset Description

- The dataset is collected from Kaggle website. The link for the data is https://www.kaggle.com/datasets/atharvaingle/bikepedcrash. Our dataset holds all of the information related to bike crash include the bike rider's information the driver's information and the other objective conditions such as weather and road conditions etc, which will allow us to understand the attributions that lead to the bike crash and coorelated circumastance. 

- We select this dataset to gather the main factors that cause the bike accidents and figure out the negative impact from them.

## Dataset Cleaning

- Drop Null values
- Fill in certain age number with reasonable estimation

### Information for each crash includes: 

County, City, Crash Date, Crash Day, Crash Group, Crash Location, Crash Time, Crash Severity, Bike/Pedestrian Age Group, Bike/Pedestrian Alcohol Detected, Bike Direction, Bike/Pedestrian Injury, Bike/Pedestrian Position, Bike/Pedestrian Race, Bike/Pedestrian Sex, Ambulance Response, Driver Age Group, Driver Estimated Speed, Speed Limit, Driver Alcohol Detected, Driver Injury, Driver Race, Driver Sex, Driver Vehicle Type, Hit and Run, Development, Light Condition, Locality, Number of Lanes, Road Characteristics/Class/Condition/Configuration, Road Defects/Features, Traffic Control, Crash Type, and/or Weather.

## Project Overview
- Predicting severity of the injury from Bike Crash with relevant parameters

## Objective

The primary purpose of this data is to provide insights into the patterns and frequency of these types of accidents in the state that can help develop safety measures and policies.

## List of Tools
- SQL
- Python
- R
- Tableau

## Proposed Machine Learning Model
- Our model is going to predict the severity of injury by Bikecrash with relevant parameters. We will examine the statistical relationship of the data set's features to determine the coorelation among the possible attributions for bike crash. Then we apply a linear regression model to predict the severity of injury.
