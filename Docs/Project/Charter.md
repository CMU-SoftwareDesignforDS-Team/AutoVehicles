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
* We want to increase the amount of people who feel comfortable and safe sharing the road with AV’s by 10%.
* Current road users who feel comfortable and safe sharing the road with AV’s is 73% of surveyed users based on the study in 2017. In 2019, 83% of surveyed users feel comfortable and safe sharing the road with AV’s.
* After promotion of the app, we will re-survey the population in 4 weeks time to measure their comfortability and safety levels.


## Plan
* Deliverable 1: Project Charter, Initial Data Report - Define business background and definite scope of project along with quantifiable metrics. To be delivered by June 11th, 2023
* Deliverable 2: Data Report and Model Report. To be delivered June 18th, 2023
* Deliverable 3: Exit Report. To be delivered June 25th, 2023


## Architecture
* We expect to have access to the data from the online survey conducted by the client. This data may include information such as demographic data, preferences, attitudes towards autonomous vehicles, past usage of ride-hailing services, and any other relevant information that can help identify potential customers for the AV taxi service.
* The entire dataset from the online survey can be moved to Azure for further analysis.
	* After some pre-aggregation on-prem: If there is a need to perform pre-aggregation on the on-premises infrastructure, the pre-aggregated data can be moved to Azure for subsequent analysis.
	* Sampled data enough for modeling: If the dataset is too large, a representative sample of the data can be moved to Azure for modeling purposes.
* Azure Stream Analytics (ASA) for stream aggregation: ASA can be used to perform real-time analysis on the streaming data, if applicable.
* HDInsight/Hive/R/Python for feature construction, aggregation, and sampling: These tools can be utilized for data preprocessing, feature engineering, and generating aggregated or sampled datasets for modeling.
* Azure Machine Learning (Azure ML) for modeling and web service operationalization: Azure ML can be used to build predictive models based on the data and operationalize them as web services.
* Azure Data Factory (ADF) or other data movement tools: ADF or other similar tools can be used to orchestrate the movement of data from on-premises to Azure.
* Once the predictive models are built and operationalized as web services, the client can consume them in their business workflow by using the web service APIs to make predictions for new customer data. The pseudo code for calling the web service API might look like this:
	```
	# Pseudo code for calling the web service API
	import requests

	# Endpoint URL of the deployed web service
	url = "https://<service_endpoint>/predict"

	# Data to be sent for prediction
	data = {
   	    "customer_id": "12345",
    	    "age": 30,
    	    "gender": "Male",
    	    "income": 50000,
    	    # Other relevant features...
	}

	# Send a POST request to the web service endpoint
	response = requests.post(url, json=data)

	# Extract the prediction result from the response
	prediction = response.json()["prediction"]
	```

*The customer can use the model results, which predict the likelihood of a customer's interest in using the AV taxi service, to make decisions regarding targeted marketing efforts. By identifying customers who are more likely to be interested in the service, the client can focus their promotional efforts on those individuals, such as offering them free AV taxi rides through email and social media. This targeted approach can help increase the usage rate of the autonomous taxi app and ultimately improve market share and company image.

*In production, the data movement pipeline can be set up using Azure Data Factory (ADF) or other similar tools. The pipeline will orchestrate the movement of data from the client's on-premises infrastructure to Azure, ensuring that the necessary data is available for analysis and modeling.


* End to end data flow
	* Before
		![image](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/83882370/fe1b5031-3296-4498-92c8-c4c72e72465c)
		![image](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/83882370/d37bb31f-6ac1-44e1-9787-bcbe2750147c)
	* After
		![image](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/83882370/ca78f95d-7fea-44d7-86f6-eab1e9be1af6)
		![image](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/83882370/607e7952-0e1e-4ca4-9f8f-8cc7a1dfe1e3)


## Communication
* Weekly meetings are conducted to make sure work has been completed per schedule
	* May 23rd
		* Team kickoff where we narrowed down the topic and picked a team name
	* June 3rd
		* Task assignments for phase 1 and direction for project
	* June 6th
		* Check on team progress and finalize project report 1
	* June 9th
		* Record video for checkpoint review 1

