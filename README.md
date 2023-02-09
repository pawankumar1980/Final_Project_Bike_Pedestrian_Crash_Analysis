# Final_Project_Bike_Pedestrian_Crash_Analysis

[link to Dashboard](https://public.tableau.com/authoring/Capstone_project_16745201462500/CrashesByCity_1#1)
 - Exploratory analysis using variables such as Geographic location, Speed limit, Day of the Week, Type of Development and etc.

## Background

The data provided for this project is a collection of information on accidents involving bicyclists and pedestrians in North Carolina. It is sourced from police reports of collisions between bicycles and motor vehicles and pedestrian and motor vehicle accidents that occurred on public roadways, vehicular areas, and private properties (if reported) from January 2007 to December 2019. The primary objective of this data is to gain a deeper understanding of the patterns and frequency of these types of accidents in the state, which can be used to inform the development of safety measures and policies aimed at reducing their occurrence.

## Dataset Description

 - The dataset is collected from the Kaggle website. The link for the data is https://www.kaggle.com/datasets/atharvaingle/bikepedcrash. Our dataset holds all the information related to the bike crash, including the bike rider's information, the driver's information and the other objective conditions such as weather and road conditions etc., which will allow us to understand the attributions that lead to the bike crash and correlated circumstances.
 - We select this dataset to gather the main factors that cause bike accidents and determine their negative impact.


## Objective

The main objective of this data is to analyze patterns and frequency of Serious & Fatal accidents in the state, in order to implement safety measures and policies that reduce their occurrence. We plan to utilize supervised Machine Learning techniques to identify the root causes of these accidents and develop strategies for prevention.

## List of Tools
- SQL
- Python
- R
- Tableau

## Data Cleaning & Features Rationalization

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

![image](https://user-images.githubusercontent.com/111800568/217667461-6ba61fe4-9bcd-4af7-9431-6b087f9e6b75.png)


 - Dropping unknown option from CrashSeverity group
 - create new Column for Machine Learning and Visualization with Fatal & Non- Fatal




## Data Visualization

- Crashes by weekday per year
![crashesbyweekdayperyear](https://user-images.githubusercontent.com/111814578/216847881-f8270065-b07d-4ec9-b00c-86dd6aae6881.png)

Fridays are the day of the week where the most accidents occur in most of the years. More information required to explain this occurrence. 

- Crashes per month
![crashespermonth](https://user-images.githubusercontent.com/111814578/216847882-5abd348c-0b83-4ee0-aab4-bfe8231ccde3.png)


- Crashes per season
![crashesperseason](https://user-images.githubusercontent.com/111814578/216847883-0ed9e020-b779-455c-b5a2-0f5b52b668e7.png)

Summer & Fall have the highest number of crashes. The authorities need to further analyze the reasons for the same.


- Crashes per tod 
![crashespertod](https://user-images.githubusercontent.com/111814578/216847884-e88a24c1-5635-44cf-97db-f2ce6d3c1d9e.png)

From the visualizations it can be interpreted that the evening and after work hours are more prone to occurrence of crash

- Crashes per year
![crashesperyear](https://user-images.githubusercontent.com/111814578/216847885-132eedf6-e3da-4b72-8a3c-ac5f3f59ea61.png)

The distribution of crash over the subsequent years from 2007 to 2019 doesn’t imply any potential decline in the accident occurrence


## Coorelation

For correlation, we used pearson correlation coefficient

 - These features were found to have the highest relation to Crash Fatality. 
 - We will discuss few of the factors in the subsequent slides using visualizations. 
 - For better visuals, we had   created two separate data frames.

### Visualizations in Relation to Crash Fatality

- Ambulance Availability
![AmbulanceR](https://user-images.githubusercontent.com/111814578/216847878-74a14e29-dcc3-4970-bd31-3de5b875ed14.png)

 - Ambulances were available for 95% of the fatal crashes.
 - In Non-Fatal cases, Ambulance were available in 70% of the cases.
 - We are not aware of whether they reached on time and people received the required first aid or treatment on time.


- Road Class
![Road_Class](https://user-images.githubusercontent.com/111814578/216847886-06329db1-6a03-456d-b3f0-99db59d50003.png)

 - Interstate roads are the biggest contributes to Fatal and non-Fatal crashes.
 - Further analysis on the possible reasons needs to be done.


- Speed limit
![speed_limit](https://user-images.githubusercontent.com/111814578/216847887-668ebe4a-4d90-4672-80ac-6fcf10ec3a37.png)

 - Speed Limit of 50-55 MPH was the biggest cause of Fatal crashes.
 - Would need more information on actual speed at the time of crash. Were there cases of over speeding?


- Traffic Control
![Traffic_control](https://user-images.githubusercontent.com/111814578/216847888-9cefe4a7-19d1-43fc-92fb-343afb9a1d48.png)

- Absence of Traffic Control is the biggest reason of crashes ( Fatal & Non-Fatal)
- This needs to be implemented on priority

- Urban or rural area
![urban_or_rural_area](https://user-images.githubusercontent.com/111814578/216847889-d289bb10-cb98-4f58-9a0c-c556401fbed3.png)

- Rural areas had a higher percentage of Fatal crashes. This might have been due to 
- Unavailability of hospitals or Ambulance at the site. This information is not available. 


## Proposed Machine Learning Model

### Preprocessing

<img width="1117" alt="Screen Shot 2023-02-08 at 23 48 03" src="https://user-images.githubusercontent.com/111800568/217720825-55f5980c-023c-489f-9fd2-6f2e5d4079e0.png">

### ML models

#### Random Forest Regressor Model

Mean Absolute Error(MAE): 0.0034987029831387807
Residual Sum of Squares(MSE): 0.0016745953307392997
R2-Score: 0.9777628961567513

### Simple Linear Regression

Mean Absolute Error(MAE): 0.15286614394522233
Residual Sum of Squares(MSE): 0.0642310381624294
R2-Score: 0.14707019698481794

### Decision Tree

Mean Absolute Error(MAE): 0.0025940337224383916
Residual Sum of Squares(MSE): 0.0025940337224383916
R2-Score: 0.965553590052538

### Gradient Boosting Regressor

Mean Absolute Error(MAE): 0.003993844148352212
Residual Sum of Squares(MSE): 0.0015333907849524402
R2-Score: 0.979637964174775

### Support Vector Machine regressor

Mean Absolute Error(MAE): 0.1655890468230072
Residual Sum of Squares(MSE): 0.07562714033184946
R2-Score: -0.004259681164184181


- Crash Fatality
![crash_Fatality](https://user-images.githubusercontent.com/111814578/216847880-bac5d90d-6a8e-43a3-948c-6a765b450309.png)

The data in the dataset is imbalanced for the prediction (refer graph). We resampled the data as under sampling, where we reduced the number of majority (Non-Fatal) crashes.

## Undersampling

<img width="1110" alt="Screen Shot 2023-02-08 at 23 59 16" src="https://user-images.githubusercontent.com/111800568/217722298-9013a3f3-f3ac-4950-a988-75c3cedf46f4.png">

The Machine Learning classifier algorithms that we used
 - Bagging Classifier (Sklearn)
 - Adaboost Classifier (sklearn)
 - Random Forrest Classifier (sklearn)

<img width="1006" alt="Screen Shot 2023-02-09 at 00 02 46" src="https://user-
                                                                
<img width="183" alt="image" src="https://user-images.githubusercontent.com/111800568/217722706-9c6f0ed6-9bd4-4085-8ad6-36e431abfc82.png">
                                                                                                                                         
                                                                                                                                         <img width="178" alt="image" src="https://user-images.githubusercontent.com/111800568/217722728-11a59ac6-5fe6-40d8-aeea-2e1d3c1e7e1d.png">

Based on the performance metrics, Random Forest Classifier is the best model in this case. Although all the models have high accuracy, Random Forest has the lowest log loss and error rate compared to Bagging Classifier and AdaBoost Classifier. Also, the recall and F1 score are similarly high for all three models.

## Limitations

The possible limitations of the data set are:
 - The data was highly imbalanced, with most of the accidents being non-fatal. This affected the model performance, and under sampling was done to improve accuracy.

 - Some crucial factors related to accidents were not included, such as information on speeding by drivers, cell phone usage, time of arrival of emergency units, and information on passengers.

 - The low correlation values indicated weak relationships between the features and the target variable.

Some suggestions to overcome these limitations could be:
 - Collecting data on driver behaviour, such as speeding and cell phone usage, to improve the understanding of factors contributing to accidents.
 - Collecting information on the arrival time of emergency units and passengers to get a more comprehensive view of the situation.
 - To improve the model performance, consider alternative techniques to handle imbalanced data, such as oversampling or synthetic data generation.


 
 
                                                              
