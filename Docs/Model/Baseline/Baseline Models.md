# Baseline Model Report

## Analytic Approach
* Target Definition
  SafeAv : On a typical day; how safe do you feel sharing the road with autonomous vehicles? (1 being very unsafe and 5 being very safe)
  </br>
  
* Model Inputs </br>
  ![image](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/75749274/08483f67-454c-476e-a7f5-aa95e1834a7c)
  </br>

## Model Description 
  Classification Model
   ** Models and Parameters
      - Data flow graph
        ![image](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/75749274/4cd6f28a-f11a-433a-abc7-7674183b2ba2) 
	 </br>
      - Learner(s) were used
        Logistic Regression 
	

## Results (Model Performance)

![image](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/75749274/ab0645b5-924b-45d7-bfef-8e452c5c99b6)

* From the above chart, AUC is 0.88, which Indicates a good discriminatory ability of the model. It performs well in distinguishing between the classes and can be considered as having a reliable predictive power. 
* Accuracy score is 0.9371


## Model Understanding

### Variable Importance (significance)

Significant Features:
x0_Mostly familiar, x0_Not familiar at all, x0_Somewhat familiar: These variables represent different levels of familiarity with Tech. It suggests that familiarity with tech is an important factor in predicting the target variable. </br>

x1_Yes: This variable is from SharePerformanceData. Its inclusion suggests that the presence of this condition is an important predictor. </br>

x3_No change: This variable is from ArizonaCrash which suggests that the absence of change about ArizonaCrash is predictive of the target variable. </br>

x4_No, x4_Not sure: These variables are from Speed25Mgh. Their inclusion suggests that these attribute levels play a role in predicting the target variable. </br>

x5_Approve, x5_Disapprove, x5_Somewhat Approve, x5_Somewhat Disapprove: These variables are from ProvingGround. Their presence indicates that the degree of approval or disapproval is important for predicting the target variable.</br>

x6_No effect, x6_Significantly Better, x6_Slightly Better, x6_Slightly Worse: These variables are from AvImpact. Their inclusion suggests that how people think about AV’s impact on traffic injuries and fatalities is influential in predicting the target variable. </br>

x7_Not sure, x7_Yes: These variables are from SchoolZoneManual. Their inclusion suggests that people’s opinion on AVs operating in manual mode while in an active school zone are important predictors. </br>


### Insights Derived from the Model
From the model coefficients below, we can see that the top 3 influence variables are x5, x6, and x1 which represent ProvingGround, AvImpact and FamiliarityTech. 

Variable: x5_Disapprove [ProvingGround]
 - Coefficient: -1.985329
 - Interpretation: Holding all other variables constant, each unit increase in x5_Disapprove is associated with a decrease in the log-odds (or probability) of the 'SafeAv' outcome by approximately 1.985329.

Variable: x6_Slightly Worse [AvImpact]
 - Coefficient: -1.391531
 - Interpretation: Holding all other variables constant, each unit increase in x6_Slightly Worse is associated with a decrease in the log-odds (or probability) of the 'SafeAv' outcome by approximately 1.391531.

Variable: x6_Significantly Worse [AvImpact]
- Coefficient: -0.811621
- Interpretation: Holding all other variables constant, each unit increase in x6_Significantly Worse is associated with a decrease in the log-odds (or probability) of the 'SafeAv' outcome by approximately 0.811621.

Variable: x1_Yes [FamiliarityTech]
- Coefficient: -0.712680
- Interpretation: Holding all other variables constant, having a value of "Yes" for x1 is associated with a decrease in the log-odds (or probability) of the 'SafeAv' outcome by approximately 0.712680.

Variable: x1_Missing [FamiliarityTech]
 - Coefficient: 0.554717
 - Interpretation: Holding all other variables constant, having a missing value for x1 is associated with an increase in the log-odds (or probability) of the 'SafeAv' outcome by approximately 0.554717.

Variable: x6_Slightly Better [AvImpact]
 - Coefficient: 0.808791
 - Interpretation: Holding all other variables constant, each unit increase in x6_Slightly Better is associated with an increase in the log-odds (or probability) of the 'SafeAv' outcome by approximately 0.808791.

Variable: x5_Somewhat Approve [ProvingGround]
 - Coefficient: 0.964861
 - Interpretation: Holding all other variables constant, each unit increase in x5_Somewhat Approve is associated with an increase in the log-odds (or probability) of the 'SafeAv' outcome by approximately 0.964861.

Variable: x6_Significantly Better [AvImpact]
 - Coefficient: 1.027432
 - Interpretation: Holding all other variables constant, each unit increase in x6_Significantly Better is associated with an increase in the log-odds (or probability) of the 'SafeAv' outcome by approximately 1.027432.
 
Variable: x5_Approve [ProvingGround]
 - Coefficient: 1.247081
 - Interpretation: Holding all other variables constant, each unit increase in x5_Approve is associated with an increase in the log-odds (or probability) of the 'SafeAv' outcome by approximately 1.247081.

![image](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/75749274/3ac91e2f-f296-4ba1-b760-9754bd78fa43)  </br>


## Conclusion and Discussions for Next Steps

 - Using the minimum viable dataset approach, the team decided to use the 2019 dataset only, since the accuracy rate proved to be over 90% as compared to the 2017 set. The 2017 dataset could not be combined with 2019 dataset due to incompatible responses even though column names were similar between the sets. Also, comparing the 2017 dataset to the 2019; there is improvement in positive feedback over time. This may be due to an increased amount of media on AV’s along with more basic knowledge and familiarity. Based on the 2019 data, overall more people tend to feel safe and comfortable sharing the roads with AV’s. </br>

 - Based on the model, the target audience for our free AV taxi ride promotion should be sent to the group of individuals who are familiar with AV technology from news or other media, who have a positive outlook on using Pittsburg streets as a proving ground for AV’s, and who tend to think that AV’s will improve crash rate and injuries. There are a few other contributing factors to help decide who the target audience for the AV taxi app would be, but described here are the top 5. Also, the top responders to the survey are in the age group 25-34. </br>
 - All of these variables have the highest impact on whether or not a person has a positive outlook on sharing the road with AV’s. Using [SafeAV] as the target variable. </br>
Discussion on overfitting
 - The training accuracy is not significantly higher than the test accuracy, which suggests no overfitting. 
![image](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/75749274/8d4ed7d6-67a7-4d09-acbb-ab0ddbfa128b)
</br>

 - There are many other features that can be generated from the current data. A few examples include: rules and regulations on AV’s in Pittsburg (eg. should AV’s be used in school zones or have a capped speed limit), the improvement of feelings for cyclists on sharing the road with vehicles through the use of AV’s, and how tentative are road users in a world of AV’s vs manual driving. </br>

 - Consolidated 2017 data set can help show the trend over time of the test group’s opinion on safety and comfortability sharing the road with AV’s. With more information and familiarity through media on AV’s, road users seem to trend more towards positive feelings on sharing the road with AV’s. With Original Engineering Manufacturer’s (OEM) focusing more research and development in the world of AV’s, this seems to correlate with the trend of overtime people feeling more comfortable sharing the road with AV’s. </br>

 - General Motors (and other OEMs) keep large data sets of the impact of AV’s, although proprietary information, data sources could significantly help the model accuracy.
