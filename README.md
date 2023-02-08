# Final_Project_Bike_Pedestrian_Crash_Analysis


## Background

The data provided for this project is a collection of information on accidents involving bicyclists and pedestrians in North Carolina. It is sourced from police reports of collisions between bicycles and motor vehicles and pedestrian and motor vehicle accidents that occurred on public roadways, vehicular areas, and private properties (if reported) from January 2007 to December 2019. The primary objective of this data is to gain a deeper understanding of the patterns and frequency of these types of accidents in the state, which can be used to inform the development of safety measures and policies aimed at reducing their occurrence.

## Dataset Description

 - The dataset is collected from the Kaggle website. The link for the data is https://www.kaggle.com/datasets/atharvaingle/bikepedcrash. Our dataset holds all the information related to the bike crash, including the bike rider's information, the driver's information and the other objective conditions such as weather and road conditions etc., which will allow us to understand the attributions that lead to the bike crash and correlated circumstances.
 - We select this dataset to gather the main factors that cause bike accidents and determine their negative impact.

## Dataset Cleaning

<img width="1285" alt="Screen Shot 2023-02-08 at 17 23 58" src="https://user-images.githubusercontent.com/111800568/217665081-e8603b7c-638a-4dea-b9ee-7b1b827ce26a.png">

 - Drop the columns 'X', 'Y', 'OBJECTID_1','BikeAge','DrvrAge','NumBicsAin', 'NumBicsBin', 'NumBicsCin', 'NumBicsKil',
       'NumBicsNoi', 'NumBicsTot', 'NumBicsUin'

<img width="1139" alt="Screen Shot 2023-02-08 at 17 26 15" src="https://user-images.githubusercontent.com/111800568/217665431-55145f5e-49c5-4181-b3d4-2045ec90fc1b.png">

- Create more condense groups for DrvrAgeGrp in order to deal with some potential outliers. I did this before hand because as "Over 70", it wouldnt convert in the codes below.
- Drop "unknown" rows from Driver age group

<img width="1143" alt="Screen Shot 2023-02-08 at 17 29 47" src="https://user-images.githubusercontent.com/111800568/217665917-39d68dcf-6b62-4d09-a458-f81278387077.png">

- Create more condense groups for BikeAgeGrp in order to deal with some potential outliers. I did this before hand because as "Over 70", it wouldnt convert in the codes below.
- Drop "unknown" rows from Biker age group


<img width="1146" alt="Screen Shot 2023-02-08 at 17 32 17" src="https://user-images.githubusercontent.com/111800568/217666428-f2cd8945-0d98-46f9-8dc0-e6be207edde8.png">

 - create time of day feature with Morning Rush, Day, Noon Rush, Afternoon, After Work Rush, Night.
 - create CrashTimeofDay grouping
 

<img width="1121" alt="Screen Shot 2023-02-08 at 17 34 07" src="https://user-images.githubusercontent.com/111800568/217666703-7d2befa1-59b8-4bb9-88b1-cdfa534f598e.png">

- Creating Seasons Column for ML
- Number of Crashes Season wise

<img width="1440" alt="Screen Shot 2023-02-08 at 17 35 50" src="https://user-images.githubusercontent.com/111800568/217667105-c86e0287-2ae4-446a-829e-b5a98c595921.png">

 - Dropping unknown option from CrashSeverity group
 - create new Column for Machine Learning and Visualization with Fatal & Non- Fatal



### Information for each crash includes: 

County, City, Crash Date, Crash Day, Crash Group, Crash Location, Crash Time, Crash Severity, Bike/Pedestrian Age Group, Bike/Pedestrian Alcohol Detected, Bike Direction, Bike/Pedestrian Injury, Bike/Pedestrian Position, Bike/Pedestrian Race, Bike/Pedestrian Sex, Ambulance Response, Driver Age Group, Driver Estimated Speed, Speed Limit, Driver Alcohol Detected, Driver Injury, Driver Race, Driver Sex, Driver Vehicle Type, Hit and Run, Development, Light Condition, Locality, Number of Lanes, Road Characteristics/Class/Condition/Configuration, Road Defects/Features, Traffic Control, Crash Type, and/or Weather.


## Objective

The main objective of this data is to analyze patterns and frequency of Serious & Fatal accidents in the state, in order to implement safety measures and policies that reduce their occurrence. We plan to utilize supervised Machine Learning techniques to identify the root causes of these accidents and develop strategies for prevention.

## List of Tools
- SQL
- Python
- R
- Tableau

## Data Cleaning & Features Rationalization
- Crash Reports  - No of accidents considering the given parameters (County,City Speedlimit, City, Agegroup, Gender )
- Visualization of crash reports using latitude and longitudes and creating heat maps
- Yearly wise , Monthly , Weekly crash reports  

## Data Visualization
- Accidents by weekday per year
![accidentsbyweekdayperyear](https://user-images.githubusercontent.com/111814578/216847822-14fc5e7c-feff-456f-a5ba-06da4d74133b.png)
- Accidents per month
![accidentspermonth](https://user-images.githubusercontent.com/111814578/216847847-4e83cb88-c602-42a0-96e7-7a7d9d9f4a06.png)
- Accidents per tod
![accidentspertod](https://user-images.githubusercontent.com/111814578/216847875-3f83b5c5-614d-44cd-b210-7da4862ac3bb.png)
- Accidents per year
![accidentsperyear](https://user-images.githubusercontent.com/111814578/216847876-e49b24e7-2968-4a3f-aa13-10a29db7de38.png)
- Ambulance
![AmbulanceR](https://user-images.githubusercontent.com/111814578/216847878-74a14e29-dcc3-4970-bd31-3de5b875ed14.png)
- Crash Fatality
![crash_Fatality](https://user-images.githubusercontent.com/111814578/216847880-bac5d90d-6a8e-43a3-948c-6a765b450309.png)
- Crashes by weekday per year
![crashesbyweekdayperyear](https://user-images.githubusercontent.com/111814578/216847881-f8270065-b07d-4ec9-b00c-86dd6aae6881.png)
- Crashes per month
![crashespermonth](https://user-images.githubusercontent.com/111814578/216847882-5abd348c-0b83-4ee0-aab4-bfe8231ccde3.png)
- Crashes per season
![crashesperseason](https://user-images.githubusercontent.com/111814578/216847883-0ed9e020-b779-455c-b5a2-0f5b52b668e7.png)
- Crashes per tod 
![crashespertod](https://user-images.githubusercontent.com/111814578/216847884-e88a24c1-5635-44cf-97db-f2ce6d3c1d9e.png)
- Crashes per year
![crashesperyear](https://user-images.githubusercontent.com/111814578/216847885-132eedf6-e3da-4b72-8a3c-ac5f3f59ea61.png)
- Road Class
![Road_Class](https://user-images.githubusercontent.com/111814578/216847886-06329db1-6a03-456d-b3f0-99db59d50003.png)
- Speed limit
![speed_limit](https://user-images.githubusercontent.com/111814578/216847887-668ebe4a-4d90-4672-80ac-6fcf10ec3a37.png)
- Traffic Control
![Traffic_control](https://user-images.githubusercontent.com/111814578/216847888-9cefe4a7-19d1-43fc-92fb-343afb9a1d48.png)
- Urban or rural area
![urban_or_rural_area](https://user-images.githubusercontent.com/111814578/216847889-d289bb10-cb98-4f58-9a0c-c556401fbed3.png)

## Proposed Machine Learning Model
- Our model is going to predict the severity of injury by Bikecrash with relevant parameters. We will examine the statistical relationship of the data set's features to determine the coorelation among the possible attributions for bike crash. Then we apply a linear regression model to predict the severity of injury.
