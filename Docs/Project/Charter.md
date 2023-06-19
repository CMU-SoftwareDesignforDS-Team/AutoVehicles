# Project Charter

## Business background

* The client is an autonomous vehicle (AV) manufacturing company, such as GM, Ford, or Tesla. The client is in both the automobile and high-tech industry.
* The client is rolling out an autonomous taxi service test in the Pittsburgh area. The client would like to do directed marketing. 
* Instead of sending invitations and promotion codes to random people, they would like to target people who are more interested, and feel comfortable using the AV taxi first, to increase the autonomous taxi app’s usage rate in 4 weeks after the promotion. This will help to increase market share, company image, and data collection for technology improvements. 
* The team will build an application to identify people who may show more interest in using autonomous taxi service, based on the Autonomous Vehicle Survey of Bicyclists and Pedestrians in Pittsburgh .

## Scope
* We are trying to identify customer characteristics using the data from the study that affect the success of direct marketing using an AV taxi ride app. We are using correlation analysis and clustering methods to identify people who may have more interest using the app. 
* We will run a promotion for free AV taxi rides and promote to interested users based on insights from the study
* Free AV taxi rides will be promoted through email and social media

	
## Personnel
* Diverse Data Dynamics team consists of:
	* Katerina Hrisopoulos
	* Matt McMonagle
	* Haoyu Wang
	* Yuli Huang
	* Eniola Akintayo

	
## Metrics
* We want to target road users who are interested in taking an AV Taxi Ride using data based on the study. We want to advertise to Increase user acceptance and safety outlook on AV taxi rides.
* We want to increase the number of people in the Pittsburgh area who would consider themselves comfortable and safe to use the AV taxi ride service. (We would consider comfortable to be a 3 or higher on a scale of 1-5, and safe to be a 3 or higher on a scale of 1-5)
* We want to increase the number of people who feel comfortable and safe sharing the road with AVs by 10%.
* Current road users who feel comfortable and safe sharing the road with AVs is 73% of surveyed users based on the study in 2017. In 2019, 83% of surveyed users feel comfortable and safe sharing the road with AV’s.
* After the promotion of the app, we will re-survey the population in 4 weeks' time to measure their comfortability and safety levels.


## Plan
* Deliverable 1: Project Charter, Initial Data Report - Define the business background and definite scope of the project along with quantifiable metrics. To be delivered by June 11th, 2023
* Deliverable 2: Data Report and Model Report. To be delivered June 18th, 2023
* Deliverable 3: Exit Report. To be delivered June 25th, 2023


## Architecture

### Data
Based on the data available and the business context, we can expect the following data:
1. Daw Data Sources:
   * bikepghmembers2017.csv: This dataset contains information about bike Pittsburgh members, which may include demographic data, preferences, and other relevant details.
   * avsurvey2019data.csv: This dataset represents the autonomous vehicle survey data collected in 2019. It likely contains responses from participants regarding their attitudes, preferences, and willingness to use AV taxi services.
   * bikepghpublic2017.csv: This dataset contains information about the general public's perceptions and attitudes toward autonomous vehicles and AV taxi services.
2. Processed Data:
   * av_2019Survey: This processed dataset is derived from the avsurvey2019data.csv. It may include transformed and cleaned survey data that is ready for analysis.
   * bikepghpublic2017: This processed dataset is derived from bikepghpublic2017.csv. It may include cleaned and transformed data related to public perceptions and attitudes toward AV taxi services.

### Data Movement
Based on the amount of data available in the datasets: "bikepghmembers2017.csv," "avsurvey2019data.csv," and "bikepghpublic2017.csv." We plan on moving all the data to have sufficient data for the model<br>

To build the model, the data movement process will involve the following steps:
* Data Collection & Extraction: Downloading  the raw data source files 
* Data Preprocessing: Reviewing the data 
* Data Splitting: Split the data into training and testing sets. 
* Model Training: Apply the algorithms to train the model using the training data. 
* Model Evaluation: Assess the performance of the trained model using the testing data.

### Data Storage And Analytics
To manage the data and perform analytics in the project, we’ll use the following tools and resources:
* Our data is small enough to be saved in a file. We will use a .csv file 
* We will use Python libraries like pandas, NumPy, and SciPy for data processing and analysis.
* We will use Scikit-learn for classification, regression, clustering, etc.

### Model Consumption
The scores generated from the solution can be consumed in the business workflow of the customer through API calls. The customer's application or system can make HTTP requests to the web service API endpoints to obtain the desired predictions or results. Below is a pseudo code example illustrating how the web service API calls can be made:

```Python
import requests

# Define the API endpoint URL
api_url = "https://av-model-app-6f2c9d64a330.herokuapp.com/api"
# Define the input data for the API call
input_data = {
   “FamiliarityTech”: value1,
    “SharePerformanceData”: value2,
    ReportSafetyIncident: value3,
    ArizonaCrash: value4,
    Speed25Mph: value5,
    ProvingGround: value6,
    AvImpact: value7,
    SchoolZoneManual: value8
}

# Make a POST request to the API endpoint with the input data
response = requests.post(api_url, json=input_data)

# Check the response status code
if response.status_code == 200:
    # API call was successful
    result = response.json()
    # Process the result or use it in the business workflow
    # ...
else:
    # API call failed
    print("Error: API call failed with status code", response.status_code)
    # Handle the error condition appropriately
    # ...
```

### Model Use for Decision Making
Our potential clients will use the model results to make decisions related to targeted marketing strategies, promotional activities, and customer engagement efforts for their autonomous taxi service. The model results, which predict customer interest in using the AV taxi service, will help the customer identify and prioritize potential customers who are more likely to be interested and feel comfortable using the service.<br>

Here is a high-level overview of how the customer may use the model results to make decisions:
* The trained predictive model(s) will be deployed as a web service or API, allowing clients to make predictions on new data.
* The client(s) will make API calls to the deployed model(s) using relevant customer data.
* The model(s) will generate predictions indicating the likelihood of customer interest in using the AV taxi service for each input customer.
* The client(s) will use the model results to inform their decision-making processes in the following ways:
    * The client(s) can identify segments of potential customers who have higher predicted interest in using the service. They can tailor their marketing messages and strategies to specifically target these segments, increasing the effectiveness of their marketing campaigns.
    * Based on the model results, the customer can prioritize promotional activities, such as offering discounts, incentives, or special offers, to the customers who are more likely to be interested in using the AV taxi service. This targeted approach can enhance customer engagement and encourage adoption of the service.
    * The client(s) can use the model results to personalize their customer engagement efforts. They can customize their communication channels, messages, and offers based on the predicted customer interest, increasing the chances of attracting and retaining potential customers.
* The client(s) can continuously evaluate the effectiveness of their decisions and refine their marketing strategies based on the feedback and outcomes. They can analyze the success metrics, such as customer adoption rate, app usage, feedback, and customer satisfaction, to assess the impact of their decisions and make further improvements.

### Data Movement in Production
* The CSV file containing the raw data is saved in the application folder
* Use Python libraries to ingest the data and load it into memory
* Feed the data into the predictive model to generate outcomes “Yes/No”
* Deploy the model on Heroku
* Model outputs are captured and utilized by the client(s)’ systems

### End to End Data Flow and Decision Architecture
![image](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/83882370/f3694b99-ca7e-4235-a37d-f07191aa062c)

## Communication
* Weekly meetings are conducted to make sure work has been completed per the schedule
	* May 23rd
		* Team kickoff where we narrowed down the topic and picked a team name
	* June 3rd
		* Task assignments for phase 1 and direction for the project
	* June 6th
		* Check on team progress and finalize project report 1
	* June 9th
		* Record video for checkpoint review 1
  	* June 12th
		* Project Delivery 2 Task assignment
	* June 15th
		* Team discussion on App and Model development
	* June 16th
		* Record video for checkpoint review 2
	* June 19th : 
		* Slides and exit report task assignment
		* Team GitHub update 
	* June 21st
		* Checkpoint-3 recording and finalizing project report 
	* June 23rd 
		* Submit project report -3 and checkpoint-3
