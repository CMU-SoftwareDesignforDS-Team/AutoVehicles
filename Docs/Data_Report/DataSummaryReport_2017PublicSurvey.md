# Data Report for 2017 Public Survey Responses
Data Source: https://catalog.data.gov/dataset/autonomous-vehicle-survey-of-bicyclists-and-pedestrians-in-pittsburgh

## General summary of the data

1. There are 813 records in the file bikepghpublic2017.csv <br>
2. There are no duplicates in the bikepghpublic2017 survey data. <br>
3. Respondent ID are populated for all records.  Below are the missing value count for all variables: 
   
  Response ID                 0
  Start Date                  0
  End Date                    0
  Status                      0
  Source Type                 0
  InteractPedestrian         14
  InteractBicycle            14
  CircumstancesCoded        410
  FeelingsProvingGround      14
  SafetyHuman                14
  SafetyAV                   14
  AVSafetyPotential          14
  RegulationTesting          14
  RegulationSpeed            14
  RegulationSchoolZone       14
  RegulationShareData        14
  AdvocacyIssues             20
  BikePghPosition            14
  PayingAttentionAV          14
  FamiliarityTechnoology     14
  ZipCode                    14
<br> 
  
4. The majority of participants in the 2017 public survey think the Autonomous Vehicles will have a better impact on injuries and fatalities. 
  
  AVSafetyPotential
  Maybe       174
  No           63
  Not sure     69
  Yes         493
<br>
 
5. The majority of surveyed people in 2017 public survey were somewhat familiar with the technology behind AVs.

  FamiliarityTechnoology
  Extremely familiar      74
  Mostly Unfamiliar      165
  Mostly familiar        170
  Not familiar at all     54
  Somewhat familiar      336
<br>

6. The majority of people in the 2017 public dataset paid a moderate amount of attention to the subject of AVs in the news.

PayingAttentionAV
Not at all               12
To a large extent       208
To a moderate extent    261
To little extent         78
To some extent          240

7. The people in this 2017 survey had a better outlook on safety with AVs versus human-driven vehicles.

  SafetyAV
  1                 50
  2                 80
  3                177
  4                255
  5                153
  No experience     84

  SafetyHuman
  1                 43
  2                215
  3                308
  4                193
  5                 34
  No experience      6
<br>

## Data quality summary
- There are no duplicates in the file.
- Categorical missing values: treat missing values as a separate category. 

## Target variable
AvSafetyPotential

## Individual variables
Response ID, Start Date, End Date, Status, Source Type, InteractPedestrian, InteractBicycle, CircumstancesFreeText, CircumstancesCoded,<br>
FeelingsProvingGround, SafetyHuman, SafetyAV, AVSafetyPotential, RegulationTesting, RegulationSpeed, RegulationSchoolZone, RegulationShareData, <br>
OtherRegulations, AdvocacyIssues,BikePghPosition, BikePghElaborate, PayingAttentionAV, FamiliarityTechnoology, MoreToShare, ZipCode <br>

## Relationship between explanatory variables and target variable

- Chi-Square Test of Independence between AvSafetyPotential and InteractPedestrian:
  - Chi-square statistic: 17.753718398683787
  - p-value: 0.006878060817184138
  - Interpretation: The low p-value (p-value <= 0.05) suggests a potential association between AvSafetyPotential and InteractPedestrian

- Chi-Square Test of Independence between AvSafetyPotential and InteractBicycle:
  - Chi-square statistic: 13.983662786207557
  - p-value: 0.029819192970087352
  - Interpretation: The low p-value (p-value <= 0.05) suggests a potential association between AvSafetyPotential and InteractBicycle

- Chi-Square Test of Independence between AvSafetyPotential and SafetyHuman:
  - Chi-square statistic: 14.540929459947856
  - p-value: 0.484961461359284
  - Interpretation: The low p-value (p-value <= 0.05) suggests that there is a statistically significant association between AvSafetyPotential and SafetyHuman

- Chi-Square Test of Independence between AvSafetyPotential and SafetyAV:
  - Chi-square statistic: 339.10094276311753
  - p-value: 3.984269194143067e-63
  - Interpretation: The low p-value (p-value <= 0.05) suggests that there is a significant association between AvSafetyPotential and SafetyAV

- Chi-Square Test of Independence between AvSafetyPotential and PayingAttentionAV:
  - Chi-square statistic: 82.76657270422899
  - p-value: 1.2212077281265502e-12
  - Interpretation: The low p-value (p-value <= 0.05) suggests that there is a significant association between AvSafetyPotential and PayingAttentionAV:

- Chi-Square Test of Independence between AvSafetyPotential and FamiliarityTechnoology:
  - Chi-square statistic: 94.23745665148141
  - p-value: 7.429142771739588e-15
  - Interpretation: The low p-value (p-value <= 0.05) suggests that there is a statistically significant association between AvSafetyPotential and FamiliarityTechnoology
<br>