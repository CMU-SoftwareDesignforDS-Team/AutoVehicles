# Data and Feature Definitions

This document provides a central hub for the raw data sources, the processed/transformed data, and feature sets. More details of each dataset are provided in the data summary report. 

For each data, an individual report describing the data schema, the meaning of each data field, and other information that is helpful for understanding the data is provided. If the dataset is the output of processing/transforming/feature engineering existing data set(s), the names of the input data sets, and the links to scripts that are used to conduct the operation are also provided. 

## Raw Data Sources
| Dataset Name | Original Location   | Destination Location  | Data Movement Tools / Scripts | Link to Report |
| ---:| ---: | ---: | ---: | -----: |
| bikepghmembers2017.csv | Data.GOV | [autonomous-vehicle-survey-of-bicyclists-and-pedestrians-in-pittsburgh](https://catalog.data.gov/dataset/autonomous-vehicle-survey-of-bicyclists-and-pedestrians-in-pittsburgh) | [bikepghmember2017_EDA.ipynb](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/blob/main/Code/Data_Acquisition_and_Understanding/bikepghmember2017_EDA.ipynb) | [bikepghmember2017 data report](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/blob/main/Docs/Data_Report/DataSummaryReport_2017MemberSurvey.md)|
| avsurvey2019data.csv | Data.GOV | [autonomous-vehicle-survey-of-bicyclists-and-pedestrians-in-pittsburgh](https://catalog.data.gov/dataset/autonomous-vehicle-survey-of-bicyclists-and-pedestrians-in-pittsburgh) | [AvSurvey2019_EDA.ipynb](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/blob/main/Code/Data_Acquisition_and_Understanding/AvSurvey2019_EDA.ipynb) | [avsurvey2019 data Report](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/blob/main/Docs/Data_Report/DataSummaryReport_2019Survey.md)|
| bikepghpublic2017.csv | Data.GOV | [autonomous-vehicle-survey-of-bicyclists-and-pedestrians-in-pittsburgh](https://catalog.data.gov/dataset/autonomous-vehicle-survey-of-bicyclists-and-pedestrians-in-pittsburgh) | [bikepghpublic2017_EDA.ipynb](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/blob/main/Code/Data_Acquisition_and_Understanding/bikepghpublic2017_EDA.ipynb) | [bikepghpublic2017 data report](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/blob/main/Docs/Data_Report/DataSummaryReport_2017PublicSurvey.md)|

## Processed Data
| Processed Dataset Name | Input Dataset(s)   | Data Processing Tools/Scripts | Link to Report |
| ---:| ---: | ---: | ---: | 
| av_2019Survey | [avsurvey2019data.csv]([link/to/dataset1/report](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/blob/main/Data/Raw/avsurvey2019data.csv)) | [AvSurvey2019_EDA.ipynb](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/blob/main/Code/Data_Acquisition_and_Understanding/AvSurvey2019_EDA.ipynb) | [avsurvey2019 data Report](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/blob/main/Docs/Data_Report/DataSummaryReport_2019Survey.md)|
| bikepghpublic2017 | [bikepghpublic2017.csv](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/blob/main/Code/Data_Acquisition_and_Understanding/bikepghpublic2017_EDA.ipynb) |[bikepghpublic2017_EDA.ipynb](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/blob/main/Code/Data_Acquisition_and_Understanding/bikepghpublic2017_EDA.ipynb) | [bikepghpublic2017 data report]([link/to/report2](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/blob/main/Docs/Data_Report/DataSummaryReport_2017PublicSurvey.md))|
| bikepghmembers2017 | [bikepghmembers2017.csv]([link/to/dataset2/report](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/blob/main/Data/Raw/bikepghmembers.csv)) |[bikepghmember2017_EDA.ipynb]([link/to/R/script/file/in/Code](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/blob/main/Code/Data_Acquisition_and_Understanding/bikepghmember2017_EDA.ipynb)) | [bikepghmember2017 data report]([link/to/report2](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/blob/main/Docs/Data_Report/DataSummaryReport_2017MemberSurvey.md))|

After conducting the necessary data preprocessing steps, the dataset has been transformed and cleaned to facilitate the subsequent analysis. The following summary provides an overview of the processed data and highlights the key processing techniques applied.
1. Missing Values Handling
During the initial exploration of the dataset, it was observed that several variables contained missing values. These missing values were handled using a combination of techniques, such as:
For categorical variables, missing values were imputed by creating a new category of “missing”. The approach minimizes any potential bias in subsequent analyses.
Numeric variables with missing values were imputed using the mean of the respective variable. This method provides a reasonable estimation for the missing values without significantly distorting the variable's distribution.
The handling of missing values is crucial to avoid biased or incomplete analyses. By imputing the missing values using appropriate strategies, we ensure the integrity and reliability of the dataset for further analysis.
2. Categorical Variable Encoding
To incorporate categorical variables into the analysis, they were appropriately encoded using one-hot encoding. This technique creates binary variables for each category within a categorical feature, enabling the inclusion of categorical data in regression models and other analyses. The encoded variables capture the presence or absence of each category, providing a comprehensive representation of the categorical data.
The encoding of categorical variables allows us to utilize the information contained within these variables for predictive modeling or exploratory analysis.


## Feature Sets

| Feature Set Name | Input Dataset(s)   | Feature Engineering Tools/Scripts | Link to Report |
| ---:| ---: | ---: | ---: | 
| 2019SurveryFeatures | [avsurvey2019data.csv](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/blob/main/Data/Raw/avsurvey2019data.csv) |[AvSurvey2019_EDA.ipynb](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/blob/main/Code/Data_Acquisition_and_Understanding/AvSurvey2019_EDA.ipynb) | [avsurvey2019 Data Report](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/blob/main/Docs/Data_Report/DataSummaryReport_2019Survey.md)|
| 2017PublicSurveyFeatures | [bikepghpublic2017.csv](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/blob/main/Data/Raw/bikepghpublic2017.csv) |[bikepghpublic2017_EDA.ipynb](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/blob/main/Code/Data_Acquisition_and_Understanding/bikepghpublic2017_EDA.ipynb) | [bikepghpublic2017 feature set](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/blob/main/Data/For_Modeling/2017PublicSurveyFeatures.csv)|
| 2017MembersSurveyFeatures | [bikepghmembers2017.csv](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/blob/main/Data/Raw/bikepghmembers.csv) |[bikepghmember2017_EDA.ipynb](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/blob/main/Code/Data_Acquisition_and_Understanding/bikepghmember2017_EDA.ipynb) | [bikepghmember2017 data report](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/blob/main/Docs/Data_Report/DataSummaryReport_2017MemberSurvey.md)|

* 2019SurveryFeatures contains 66 non-missing variables. Below is the snapshot of 2019SurveryFeatures:
![image](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/83882370/a735992c-9b7d-4525-8dcc-0fa46c5d7f4c)

* 2017PublicSurveyFeatures contains 54 non-missing variables. Below is a snapshot of the survey features:
![image](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/83882370/9021afe4-8a1f-42ab-b1ae-a4540a5a3938)
