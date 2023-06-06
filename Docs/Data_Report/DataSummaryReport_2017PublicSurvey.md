# Data Report for 2017 Public Survey Responses
Data Source: https://catalog.data.gov/dataset/autonomous-vehicle-survey-of-bicyclists-and-pedestrians-in-pittsburgh

## General summary of the data

1. There are 813 records in the file bikepghpublic2017.csv <br>
2. There are no duplicates in the bikepghpublic2017 survey data. <br>
3. Respondent ID are populated for all records.  Below are the missing value count for all variables:<br>
  Response ID                 0<br>
  Start Date                  0<br>
  End Date                    0<br>
  Status                      0<br>
  Source Type                 0<br>
  InteractPedestrian         14<br>
  InteractBicycle            14<br>
  CircumstancesCoded        410<br>
  FeelingsProvingGround      14<br>
  SafetyHuman                14<br>
  SafetyAV                   14<br>
  AVSafetyPotential          14<br>
  RegulationTesting          14<br>
  RegulationSpeed            14<br>
  RegulationSchoolZone       14<br>
  RegulationShareData        14<br>
  AdvocacyIssues             20<br>
  BikePghPosition            14<br>
  PayingAttentionAV          14<br>
  FamiliarityTechnoology     14<br>
  ZipCode                    14<br>
<br>
4. The majority of participants in the 2017 public survey think the Autonomous Vehicles will have a better impact on injuries and fatalities.<br>
<img width="399" alt="image" src="https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/83882370/ff94ee36-1edd-46ae-9302-a1056f846b0e">
<br>
  AVSafetyPotential<br>
  Maybe       174<br>
  No           63<br>
  Not sure     69<br>
  Yes         493<br>
<br>
5. The majority of surveyed people in 2017 public survey were somewhat familiar with the technology behind AVs.<br>
<img width="386" alt="image" src="https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/83882370/25f84c5e-5511-457e-b901-2da1d3156a69">
<br>
  FamiliarityTechnoology<br>
  Extremely familiar      74<br>
  Missing                 14<br>
  Mostly Unfamiliar      165<br>
  Mostly familiar        170<br>
  Not familiar at all     54<br>
  Somewhat familiar      336<br>
<br>
6. The majority of people in the 2017 public dataset paid a moderate amount of attention to the subject of AVs in the news.<br>
<img width="391" alt="image" src="https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/83882370/a7bb3ece-39c7-47b1-9623-59a4a142067d">
<br>
  PayingAttentionAV<br>
  Missing                  14<br>
  Not at all               12<br>
  To a large extent       208<br>
  To a moderate extent    261<br>
  To little extent         78<br>
  To some extent          240<br>
<br>
7. The people in this 2017 survey had a better outlook on safety with AVs versus human-driven vehicles.<br>
<img width="386" alt="image" src="https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/83882370/0e371612-46b9-4113-a8be-acbf700217ea">
<br>
   SafetyAV<br>
   1                 50<br>
   2                 80<br>
   3                177<br>
   4                255<br>
   5                153<br>
   No experience     84<br>
<br>
<img width="385" alt="image" src="https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/83882370/5b33ab59-51bb-45e4-ba57-0f3d44cfc0b1">
<br>
   SafetyHuman<br>
   1                 43<br>
   2                215<br>
   3                308<br>
   4                193<br>
   5                 34<br>
   No experience      6<br>
<br>

## Data quality summary
- There are no duplicates in the file.
- Categorical missing values: treat missing values as a separate category. 

## Target variable
AvSafetyPotential

## Individual variables
Response ID, Start Date, End Date, Status, Source Type, InteractPedestrian, InteractBicycle, CircumstancesFreeText, CircumstancesCoded,
FeelingsProvingGround, SafetyHuman, SafetyAV, AVSafetyPotential, RegulationTesting, RegulationSpeed, RegulationSchoolZone, RegulationShareData,
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
