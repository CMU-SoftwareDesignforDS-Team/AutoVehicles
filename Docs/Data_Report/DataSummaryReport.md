# Data Report for 2019 Survey Responses
This file will be generated for each data file received or processed. The Interactive Data Exploration, Analysis, and Reporting (IDEAR) utility developed by TDSP team of Microsoft can help you explore and visualize the data in an interactive way, and generate the data report along with the process of exploration and visualization. 
Data Source: https://catalog.data.gov/dataset/autonomous-vehicle-survey-of-bicyclists-and-pedestrians-in-pittsburgh

IDEAR allows you to output the data summary, statistics, and charts that you want to use to tell the data story into the report. You only need to click a few buttons, and the report will be generated for you. 

## General summary of the data

1. 795 records in the file avsurvey2019data.csv <br>
2. There are no duplicates in the av_2019 Survey data. <br>
3. Respondent ID are populated for all records.  <br>
4. Majority of participants think the Auto Vehicles will have a better impact on traffic injuries and fatalities. <br>
5. Within the positive AvImpact category, the age group 25-34 has the most respondents. <br>
6. Age Group 25-34 has the most number of respondents. <br>

## Data quality summary
There are no duplicates in the file.

RangeIndex: 795 entries, 0 to 794
Data columns (total 23 columns):
 #   Column                Non-Null Count  Dtype  
---  ------                --------------  -----  
 0   RespondentID          795 non-null    int64  
 1   StartDate             795 non-null    object 
 2   EndDate               795 non-null    object 
 3   FamiliarityNews       794 non-null    object 
 4   FamiliarityTech       794 non-null    object 
 5   SharedCyclist         792 non-null    object 
 6   SharedPedestrian      793 non-null    object 
 7   SafeAv                787 non-null    float64
 8   SafeHuman             792 non-null    float64
 9   AvImpact              788 non-null    object 
 10  ProvingGround         792 non-null    object 
 11  Speed25Mph            792 non-null    object 
 12  TwoEmployeesAv        792 non-null    object 
 13  SchoolZoneManual      793 non-null    object 
 14  ShareTripData         793 non-null    object 
 15  SharePerformanceData  791 non-null    object 
 16  ReportSafetyIncident  794 non-null    object 
 17  ArizonaCrash          792 non-null    object 
 18  ZipCode               763 non-null    object 
 19  BikePghMember         787 non-null    object 
 20  AutoOwner             792 non-null    object 
 21  SmartphoneOwner       791 non-null    object 
 22  Age                   788 non-null    object 
dtypes: float64(2), int64(1), object(20)


## Target variable
AvImpact

## Individual variables
RespondentID
StartDate
EndDate
FamiliarityNews
FamiliarityTech
SharedCyclist
SharedPedestrian
SafeAv
SafeHuman
ProvingGround
Speed25Mph
TwoEmployeesAv
SchoolZoneManual
ShareTripData
SharePerformanceData
ReportSafetyIncident
ArizonaCrash
ZipCode
BikePghMember
AutoOwner
SmartphoneOwner
Age

![image](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/75749274/6eff8e4d-b2f2-4404-8661-36198647912c)

![image](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/75749274/a190f081-f32b-46c3-a40c-a5f88e5568f1)


## Variable ranking

## Relationship between explanatory variables and target variable
![image](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/75749274/82e1c3e3-d2cf-4553-8272-06f1ea1c7b17)


