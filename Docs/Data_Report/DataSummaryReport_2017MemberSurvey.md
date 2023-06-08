# Data Report for 2017 Members Survey Responses
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
<img width="400" alt="image" src="https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/134182318/2a593ebd-7d81-4592-afab-6e6b7362b6e4">
<br>
  AVSafetyPotential<br>
  Maybe        54<br>
  No           11<br>
  Not sure     24<br>
  Yes         232<br>
<br>
5. The majority of surveyed people in 2017 members survey were somewhat familiar with the technology behind AVs.<br>
<img width="400" alt="image" src="https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/134182318/ed627194-3d3b-4f64-a47f-ee2c5ab0bf4d">
<br>
  FamiliarityTechnoology<br>
  Extremely familiar      33<br>
  Mostly Unfamiliar       71<br>
  Mostly familiar         56<br>
  Not familiar at all     17<br>
  Somewhat familiar      144<br>
<br>
6. The majority of people in the 2017 members dataset paid a moderate amount of attention to the subject of AVs in the news.<br>
<img width="400" alt="image" src="https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/134182318/3c8e9689-8af4-49c6-be17-7071df3aee1d">
<br>
  PayingAttentionAV<br>
  Not at all                3<br>
  To a large extent        87<br>
  To a moderate extent    110<br>
  To little extent         24<br>
  To some extent           97<br>
<br>
7. The members in this 2017 survey had a better outlook on safety with AVs versus human-driven vehicles.<br>
<img width="400" alt="image" src="https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/134182318/bd0d218d-12b2-4141-b27e-8b5ac2b3f5da">
<br>
   SafetyAV<br>
   1                  9<br>
   2                 26<br>
   3                 84<br>
   4                115<br>
   5                 54<br>
   No experience     33<br>
<br>
<img width="400" alt="image" src="https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/134182318/1395989c-d4d0-47b2-bd14-2458a6ff866c">
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
