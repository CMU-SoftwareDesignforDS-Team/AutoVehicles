# Data Report for 2019 Survey Responses
This file will be generated for each data file received or processed. The Interactive Data Exploration, Analysis, and Reporting (IDEAR) utility developed by TDSP team of Microsoft can help you explore and visualize the data in an interactive way, and generate the data report along with the process of exploration and visualization. <br>
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

![image](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/75749274/3a42e552-8928-4baf-be1b-30dc215891af)



## Target variable
AvImpact

## Individual variables
RespondentID,  StartDate,  EndDate,  FamiliarityNews, FamiliarityTech, SharedCyclist, SharedPedestrian, SafeAv, SafeHuman <br>
,ProvingGround, Speed25Mph, TwoEmployeesAv, SchoolZoneManual, ShareTripData, SharePerformanceData, ReportSafetyIncident, ArizonaCrash, ZipCode, BikePghMember, AutoOwner, SmartphoneOwner, Age



## Variable ranking

## Relationship between explanatory variables and target variable

Chi-Square Test of Independence between AvImpact and FamiliarityNews:
Chi-square statistic: 107.89976254046921
p-value: 1.1230747446149663e-15
Interpretation: The p-value is very small, indicating that there is significant evidence to suggest an association between AvImpact and FamiliarityNews variable. 
<br>
Chi-Square Test of Independence between AvImpact and FamiliarityTech:
Chi-square statistic: 104.41011509622234
p-value: 7.58239390786594e-17
Interpretation: The p-value is very small, indicating that there is significant evidence to suggest an association between AvImpact and FamiliarityTech variable.
<br>
Chi-Square Test of Independence between AvImpact and SharedCyclist:
Chi-square statistic: 25.326990355545824
p-value: 0.0013680640510576533
Interpretation: The p-value is very small, indicating that there is significant evidence to suggest an association between AvImpact and SharedCyclist variable.
<br>
Chi-Square Test of Independence between AvImpact and SharedPedestrian:
Chi-square statistic: 31.770161501708184
p-value: 0.00010239522867610294
Interpretation: The p-value is very small, indicating that there is significant evidence to suggest an association between AvImpact and SharedPedestrian variable.
<br>

Chi-Square Test of Independence between AvImpact and ReportSafetyIncident:
Chi-square statistic: 27.432193943794726
p-value: 0.000595175525812886
Interpretation: The p-value is very small, indicating that there is significant evidence to suggest an association between AvImpact and ReportSafetyIncident variable.
<br>
Chi-Square Test of Independence between AvImpact and ArizonaCrash:
Chi-square statistic: 267.17157620904067
p-value: 1.5328841708201278e-47
Interpretation: The p-value is very small, indicating that there is significant evidence to suggest an association between AvImpact and ArizonaCrash variable.
<br>
Chi-Square Test of Independence between AvImpact and Age:
Chi-square statistic: 38.5402521362788
p-value: 0.030499256116509887
Interpretation: The p-value is relatively large, indicating that there is no significant evidence to suggest an association between AvImpact and ReportSafetyIncident Age.
<br>


![image](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/75749274/82e1c3e3-d2cf-4553-8272-06f1ea1c7b17)

![image](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/75749274/8e5e889d-54cf-4533-89e5-320577462dfa)

