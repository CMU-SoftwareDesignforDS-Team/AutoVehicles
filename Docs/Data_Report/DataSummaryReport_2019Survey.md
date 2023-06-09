# Data Report for 2019 Survey Responses
Data Source: https://catalog.data.gov/dataset/autonomous-vehicle-survey-of-bicyclists-and-pedestrians-in-pittsburgh

## General summary of the data

1. 795 records in the file avsurvey2019data.csv <br>
2. There are no duplicates in the av_2019 Survey data. <br>
3. Respondent ID are populated for all records.  Below are the missing value count for all variables: 
   
  ![image](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/75749274/711ff1ee-cbf4-409d-90d8-20622d005f76) <br> 
  
4. Majority of participants think the Auto Vehicles will have a better impact on traffic injuries and fatalities. 
 ![image](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/75749274/538c24e0-d269-4dfa-b2a0-e0682978962d) <br>
 
5. Within the positive AvImpact category, the age group 25-34 has the most respondents. 
 ![image](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/75749274/82e1c3e3-d2cf-4553-8272-06f1ea1c7b17) <br>
 
6. Age Group 25-34 has the most number of respondents.
   | Age      | Count | 
   | -------- | ------|
   | 18-24    | 34    | 
   | 25-34    | 205   | 
   | 35-44    | 176   |
   | 45-54    | 129   |
   | 55-64    | 145   |
   | 65+      | 98    |
   | Under 18 | 1     |
 <br>

## Data quality summary
- There are no duplicates in the file.
- Categorical missing values: treat missing values as a separate category. 
- Numerical missing values: The variable SafeAv and SafeHuman are left-skewed. We chose to use Mean Imputation. <br>
  ![image](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/75749274/b18e4afc-7422-414c-b053-e3f84640683f)

  After imputation: <br>
  ![image](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/75749274/26731c66-e7bd-4421-92f8-6ced27315755)




## Target variable
AvImpact

## Individual variables
RespondentID,  StartDate,  EndDate,  FamiliarityNews, FamiliarityTech, SharedCyclist, SharedPedestrian, SafeAv, SafeHuman <br>
,ProvingGround, Speed25Mph, TwoEmployeesAv, SchoolZoneManual, ShareTripData, SharePerformanceData, ReportSafetyIncident, ArizonaCrash, ZipCode, BikePghMember, AutoOwner, SmartphoneOwner, Age

## Relationship between explanatory variables and target variable <br>

- Chi-Square Test of Independence between AvImpact and FamiliarityNews:
  - Chi-square statistic: 107.89976254046921
  - p-value: 1.1230747446149663e-15
  - Interpretation: The p-value is very small, indicating that there is significant evidence to suggest an association between AvImpact and FamiliarityNews variable. 

- Chi-Square Test of Independence between AvImpact and FamiliarityTech:
  - Chi-square statistic: 104.41011509622234
  - p-value: 7.58239390786594e-17
  - Interpretation: The p-value is very small, indicating that there is significant evidence to suggest an association between AvImpact and FamiliarityTech variable.

- Chi-Square Test of Independence between AvImpact and SharedCyclist:
  - Chi-square statistic: 25.326990355545824
  - p-value: 0.0013680640510576533
  - Interpretation: The p-value is small, indicating that there is significant evidence to suggest an association between AvImpact and SharedCyclist variable.

- Chi-Square Test of Independence between AvImpact and SharedPedestrian:
  - Chi-square statistic: 31.770161501708184
  - p-value: 0.00010239522867610294
  - Interpretation: The p-value is small, indicating that there is significant evidence to suggest an association between AvImpact and SharedPedestrian variable.

- Chi-Square Test of Independence between AvImpact and SafeAv:
  - Chi-square statistic: 791.5091669693057
  - p-value: 7.463046968349864e-151
  - Interpretation: The p-value is very small, indicating that there is significant evidence to suggest an association between AvImpact and SafeAv variable.
  
- Chi-Square Test of Independence between AvImpact and SafeHuman:
  - Chi-square statistic: 103.68913115677037
  - p-value: 1.489673081556701e-11
  - Interpretation: The p-value is very small, indicating that there is significant evidence to suggest an association between AvImpact and SafeHuman variable.
  
- Chi-Square Test of Independence between AvImpact and ReportSafetyIncident:
  - Chi-square statistic: 27.432193943794726
  - p-value: 0.000595175525812886
  - Interpretation: The p-value is small, indicating that there is significant evidence to suggest an association between AvImpact and ReportSafetyIncident variable.

- Chi-Square Test of Independence between AvImpact and ArizonaCrash:
  - Chi-square statistic: 267.17157620904067
  - p-value: 1.5328841708201278e-47
  - Interpretation: The p-value is very small, indicating that there is significant evidence to suggest an association between AvImpact and ArizonaCrash variable.

- Chi-Square Test of Independence between AvImpact and Age:
  - Chi-square statistic: 38.5402521362788
  - p-value: 0.030499256116509887
  - Interpretation: The p-value is relatively large, indicating that there is no significant evidence to suggest an association between AvImpact and ReportSafetyIncident Age.
<br>


![image](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/75749274/8e5e889d-54cf-4533-89e5-320577462dfa)

# Data Preparation
## Process Categorical Data
Use One Hot Encoder to handle categorical data to make them ready for classification models, such as random forest. 

![image](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/75749274/263dac05-a2a1-4867-804a-34aab800deb2)

