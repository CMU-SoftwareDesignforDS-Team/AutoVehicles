# Data Report for 2017 Public Survey Responses
Data Source: https://catalog.data.gov/dataset/autonomous-vehicle-survey-of-bicyclists-and-pedestrians-in-pittsburgh

## General summary of the data

1. There are 341 records in the file bikepghmembers2017.csv <br>
2. There are no duplicates in the bikepghmembers2017 survey data. <br>
3. Respondent ID are populated for all records.  Below are the missing value count for all variables:<br>
  Response ID                 0<br>
  Start Date                  0<br>
  End Date                    0<br>
  Status                      0<br>
  Source Type                 0<br>
  InteractPedestrian         20<br>
  InteractBicycle            20<br>
  CircumstancesCoded        173<br>
  FeelingsProvingGround      20<br>
  SafetyHuman                20<br>
  SafetyAV                   20<br>
  AVSafetyPotential          20<br>
  RegulationTesting          20<br>
  RegulationSpeed            20<br>
  RegulationSchoolZone       20<br>
  RegulationShareData        20<br>
  AdvocacyIssues             20<br>
  BikePghPosition            20<br>
  PayingAttentionAV          20<br>
  FamiliarityTechnoology     20<br>
  ZipCode                    20<br>
<br>
4. The majority of participants in the 2017 members survey think the Autonomous Vehicles will have a better impact on injuries and fatalities.<br>
<img width="399" alt="image" src="https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/83882370/ff94ee36-1edd-46ae-9302-a1056f846b0e">
<br>
  AVSafetyPotential<br>
  Maybe        54<br>
  No           11<br>
  Not sure     24<br>
  Yes         232<br>
<br>
5. The majority of surveyed people in 2017 members survey were somewhat familiar with the technology behind AVs.<br>
<img width="386" alt="image" src="https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/83882370/25f84c5e-5511-457e-b901-2da1d3156a69">
<br>
  FamiliarityTechnoology<br>
  Extremely familiar      33<br>
  Mostly Unfamiliar       71<br>
  Mostly familiar         56<br>
  Not familiar at all     17<br>
  Somewhat familiar      144<br>
<br>
6. The majority of people in the 2017 members dataset paid a moderate amount of attention to the subject of AVs in the news.<br>
<img width="391" alt="image" src="https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/83882370/a7bb3ece-39c7-47b1-9623-59a4a142067d">
<br>
  PayingAttentionAV<br>
  Not at all                3<br>
  To a large extent        87<br>
  To a moderate extent    110<br>
  To little extent         24<br>
  To some extent           97<br>
<br>
7. The members in this 2017 survey had a better outlook on safety with AVs versus human-driven vehicles.<br>
<img width="386" alt="image" src="https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/83882370/0e371612-46b9-4113-a8be-acbf700217ea">
<br>
   SafetyAV<br>
   1                  9<br>
   2                 26<br>
   3                 84<br>
   4                115<br>
   5                 54<br>
   No experience     33<br>
<br>
<img width="385" alt="image" src="https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/83882370/5b33ab59-51bb-45e4-ba57-0f3d44cfc0b1">
<br>
   SafetyHuman<br>
   1                 16<br>
   2                105<br>
   3                146<br>
   4                 47<br>
   5                  5<br>
   No experience      2<br>
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
  - Chi-square statistic: 8.318385385803097
  - p-value: 0.21569312496830564
  - Interpretation: The p-value is relatively large, indicating that there is no significant evidence to suggest an association between AvSafetyPotential and InteractPedestrian

- Chi-Square Test of Independence between AvSafetyPotential and InteractBicycle:
  - Chi-square statistic: 12.77440704883901
  - p-value: 0.0467615846000071
  - Interpretation: The low p-value (p-value <= 0.05) suggests a potential association between AvSafetyPotential and InteractBicycle

- Chi-Square Test of Independence between AvSafetyPotential and SafetyHuman:
  - Chi-square statistic: 11.982686473548252
  - p-value: 0.6803390873964937
  - Interpretation: The p-value is relatively large, indicating that there is no significant evidence to suggest an association between AvSafetyPotential and SafetyHuman

- Chi-Square Test of Independence between AvSafetyPotential and SafetyAV:
  - Chi-square statistic: 132.56193134665313
  - p-value: 6.6911578991268695e-21
  - Interpretation: The low p-value (p-value <= 0.05) suggests that there is a significant association between AvSafetyPotential and SafetyAV

- Chi-Square Test of Independence between AvSafetyPotential and PayingAttentionAV:
  - Chi-square statistic: 36.73091963551637
  - p-value: 0.00024698691748524314
  - Interpretation: The low p-value (p-value <= 0.05) suggests that there is a significant association between AvSafetyPotential and PayingAttentionAV:

- Chi-Square Test of Independence between AvSafetyPotential and FamiliarityTechnoology:
  - Chi-square statistic: 55.42700367932018
  - p-value: 1.5172468533163263e-07
  - Interpretation: The low p-value (p-value <= 0.05) suggests that there is a statistically significant association between AvSafetyPotential and FamiliarityTechnoology
