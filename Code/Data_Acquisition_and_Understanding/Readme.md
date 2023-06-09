# This folder hosts code for data acquisition and understanding 

Data Source: https://catalog.data.gov/dataset/autonomous-vehicle-survey-of-bicyclists-and-pedestrians-in-pittsburgh

## Exploratory Data Analysis
The purpose of this project is to perform an initial exploration of the given dataset and gain insights into its structure, patterns, and potential relationships between variables. <br>

### Dataset
The dataset used for this analysis is located in the Data directory. It consists of Survey Responses 2019, Member Responses 2017 and Public Responses 2017. <br>

### Code
The code for the 2019 dataset EDA is written in Python. The main script for the 2019 data analysis is EDA.ipynb, located in the Code directory. This script performs the following steps: 

- Data loading: The dataset is loaded into memory from the data directory. <br>
- Data cleaning: Any missing values or outliers are handled, and necessary data transformations are performed. <br>
- Data exploration: Various statistical measures, visualizations, and descriptive analysis techniques are applied to understand the dataset's characteristics. <br>
- Insights and findings: Key findings and insights from the analysis are summarized and presented. <br>

The code for the bikepghpublic2017 EDA is also written in Python. The main script for this data analysis is bikepghpublic2017_EDA.ipynb, located in the Code directory. This script performs the following steps: 

- Data loading: The dataset is stored in a variable from the data directory to begin data exploring. <br>
- Data cleaning: Missing values are removed using pandas library's .dropna(inplace=True)<br>
- Data exploration: Printed descriptive analysis of dataset, performed statistical calculations (chi-squared, p-value, etc.), and displayed visualizations (histograms showing counts for categorical data). <br>
- Insights and findings: Analysis of the findings from the dataset are located [here](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/blob/main/Docs/Data_Report/). <br>

### Results
The findings from the exploratory data analysis are documented in the https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/tree/main/Docs/Data_Report. This report includes detailed analysis, visualizations, and insights gained from the dataset. <br>

### Contributing
Contributions to this project are welcome. If you have any suggestions, improvements, or additional analyses, please feel free to submit a pull request. <br>



