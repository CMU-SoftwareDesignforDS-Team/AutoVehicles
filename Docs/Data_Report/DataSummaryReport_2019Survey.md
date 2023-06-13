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



## Target variable I
- AvImpact


## Individual variables
RespondentID,  StartDate,  EndDate,  FamiliarityNews, FamiliarityTech, SharedCyclist, SharedPedestrian, SafeAv, SafeHuman <br>
,ProvingGround, Speed25Mph, TwoEmployeesAv, SchoolZoneManual, ShareTripData, SharePerformanceData, ReportSafetyIncident, ArizonaCrash, ZipCode, BikePghMember, AutoOwner, SmartphoneOwner, Age

## Relationship between explanatory variables and target variable <br>

- Chi-Square Test of Independence between AvImpact and FamiliarityNews:
  - Chi-square statistic: 107.50592509742977
  - p-value: 3.316636579655523e-12
  - Interpretation: The p-value is very small, indicating that there is significant evidence to suggest an association between AvImpact and FamiliarityNews variable. 

- Chi-Square Test of Independence between AvImpact and FamiliarityTech:
  - Chi-square statistic: 226.59266476916468
  - p-value: 5.751783538627254e-37
  - Interpretation: The p-value is very small, indicating that there is significant evidence to suggest an association between AvImpact and FamiliarityTech variable.

- Chi-Square Test of Independence between AvImpact and SharedCyclist:
  - Chi-square statistic: 31.372917358951298
  - p-value: 0.007828392878542648
  - Interpretation: The p-value is small, indicating that there is significant evidence to suggest an association between AvImpact and SharedCyclist variable.

- Chi-Square Test of Independence between AvImpact and SharedPedestrian:
  - Chi-square statistic: 91.62168065200241
  - p-value: 4.937388750201591e-13
  - Interpretation: The p-value is very small, indicating that there is significant evidence to suggest an association between AvImpact and SharedPedestrian variable.

- Chi-Square Test of Independence between AvImpact and SafeAv:
  - Chi-square statistic: 791.5091669693057
  - p-value: 7.463046968349864e-151
  - Interpretation: The p-value is very small, indicating that there is significant evidence to suggest an association between AvImpact and SafeAv variable.
  
- Chi-Square Test of Independence between AvImpact and SafeHuman:
  - Chi-square statistic: 103.68913115677037
  - p-value: 1.489673081556701e-11
  - Interpretation: The p-value is very small, indicating that there is significant evidence to suggest an association between AvImpact and SafeHuman variable.


- Chi-Square Test of Independence between AvImpact and ProvingGround:
  - Chi-square statistic: 604.0164473307427
  - p-value: 1.7389562317054957e-111
  - Interpretation: The p-value is very small, indicating that there is significant evidence to suggest an association between AvImpact and ProvingGround variable.

- Chi-Square Test of Independence between AvImpact and Speed25Mph:
  - Chi-square statistic: 177.97885953715414
  - p-value: 6.0741361963891314e-30
  - Interpretation: The p-value is very small, indicating that there is significant evidence to suggest an association between AvImpact and Speed25Mph variable.

- Chi-Square Test of Independence between AvImpact and TwoEmployeesAv:
  - Chi-square statistic: 62.435624879943425
  - p-value: 9.570999980627404e-08
  - Interpretation: The p-value is very small, indicating that there is significant evidence to suggest an association between AvImpact and

- Chi-Square Test of Independence between AvImpact and SchoolZoneManual:
  - Chi-square statistic: 108.40083884846736
  - p-value: 3.2676663261339515e-16
  - Interpretation: The p-value is very small, indicating that there is significant evidence to suggest an association between AvImpact and SchoolZoneManual variable. 

- Chi-Square Test of Independence between AvImpact and ShareTripData:
  - Chi-square statistic: 44.48893195270169
  - p-value: 9.216345894982707e-05
  - Interpretation: The p-value is very small, indicating that there is significant evidence to suggest an association between AvImpact and ShareTripData variable.

- Chi-Square Test of Independence between AvImpact and SharePerformanceData:
  - Chi-square statistic: 66.39357759317298
  - p-value: 1.9445621717025522e-08
  - Interpretation: The p-value is very small, indicating that there is significant evidence to suggest an association between AvImpact and SharePerformanceData variable. 
  
- Chi-Square Test of Independence between AvImpact and ReportSafetyIncident:
  - Chi-square statistic: 27.432193943794726
  - p-value: 0.000595175525812886
  - Interpretation: The p-value is small, indicating that there is significant evidence to suggest an association between AvImpact and ReportSafetyIncident variable.

- Chi-Square Test of Independence between AvImpact and ArizonaCrash:
  - Chi-square statistic: 267.17157620904067
  - p-value: 1.5328841708201278e-47
  - Interpretation: The p-value is very small, indicating that there is significant evidence to suggest an association between AvImpact and ArizonaCrash variable.

- Chi-Square Test of Independence between AvImpact and ZipCode:
  - Chi-square statistic: 742.2386156775215
  - p-value: 0.00010780058560351683
  - Interpretation: The p-value is small, indicating that there is significant evidence to suggest an association between AvImpact and ZipCode variable.

- Chi-Square Test of Independence between AvImpact and BikePghMember:
  - Chi-square statistic: 25.132761735398155
  - p-value: 0.048188622037265164
  - Interpretation: The p-value is relatively large, indicating that there is no significant evidence to suggest an association between AvImpact and BikePghMember variable.


- Chi-Square Test of Independence between AvImpact and AutoOwner:
  - Chi-square statistic: 15.15639341678869
  - p-value: 0.12646321491943868
  - Interpretation: The p-value is relatively large, indicating that there is no significant evidence to suggest an association between AvImpact and AutoOwner variable.

- Chi-Square Test of Independence between AvImpact and SmartphoneOwner:
  - Chi-square statistic: 44.59986672270586
  - p-value: 2.567601748012208e-06
  - Interpretation: The p-value is pretty small, indicating that there is significant evidence to suggest an association between AvImpact and SmartphoneOwner variable

- Chi-Square Test of Independence between AvImpact and Age:
  - Chi-square statistic: 38.5402521362788
  - p-value: 0.030499256116509887
  - Interpretation: The p-value is relatively large, indicating that there is no significant evidence to suggest an association between AvImpact and ReportSafetyIncident Age.
<br>

![image](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/75749274/8e5e889d-54cf-4533-89e5-320577462dfa)

## Variables Ranking

From the strongest association to the least association based on the above p-value of the Correlation Analysis: <br>

SafeAv, ProvingGround, ArizonaCrash, FamiliarityTech, Speed25Mph, ReportSafetyIncident, SchoolZoneManual, SharedPedestrian, FamiliarityNews, SafeHuman, SharePerformanceData, TwoEmployeesAv, 
SmartphoneOwner, ShareTripData, ZipCode, SharedCyclist


## Target variable II
- SafeAv


## Individual variables
RespondentID,  StartDate,  EndDate,  FamiliarityNews, FamiliarityTech, SharedCyclist, SharedPedestrian, AvImpact, SafeHuman <br>
,ProvingGround, Speed25Mph, TwoEmployeesAv, SchoolZoneManual, ShareTripData, SharePerformanceData, ReportSafetyIncident, ArizonaCrash, ZipCode, BikePghMember, AutoOwner, SmartphoneOwner, Age

## Relationship between explanatory variables and target variable <br>
| Cramér's V  |SafeAv |  Rank   | 
|--------|------------|--------|
| SafeAv | 1.000      | 1      |    
| AvImpact | 0.441      | 2      |    
| ProvingGround | 0.413      | 3      |    
| Speed25Mph | 0.280      | 4      |    
| ArizonaCrash | 0.266      | 5      |    
| ReportSafetyIncident | 0.244      | 6      |   
| SharePerformanceData | 0.237      | 7      |    
| FamiliarityTech | 0.235      | 8      |   
| SchoolZoneManual | 0.207      | 9      |  
| ShareTripData | 0.198      | 10      |   
| SharedPedestrian | 0.179      | 11      |  
| ZipCode | 0.166      | 12      | 
| TwoEmployeesAv | 0.154      | 13      | 
| SmartphoneOwner | 0.145      | 14      | 
| FamiliarityNews | 0.132      | 15      | 
| SafeHuman | 0.120      | 16      |
| SharedCyclist | 0.115      | 17      |  
| BikePghMember | 0.085      | 18      |   
| AutoOwner | 0.033      | 19      |  
| Age | 0.000      | 20      |


# Data Preparation
## Process Categorical Data
Use One Hot Encoder to handle categorical data to make them ready for classification models, such as random forest. 

![image](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/75749274/263dac05-a2a1-4867-804a-34aab800deb2)




