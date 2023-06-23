# Exit Report

Customer: General Motors (and other AV OEMs)

##	Overview
Using data from a 2019 Pittsburgh area based survey, we filtered the results to help us understand what type of individual was more likely to be a targeted user of a free AV taxi ride app.

##	Business Domain
Automobile companies that are beginning research and development on autonomous vehicles 

##	Business Problem
The automobile industry could be a key user of this application to understand what kind of customer is already comfortable with autonomous vehicles, and how they can improve the safety and comfortability of customers who may not be ready to share the road with AV’s.

##	Data Processing
The data processing phase of our project involved working with multiple datasets and transforming them into a suitable format for our model.<br>
The original datasets consist of 2017 and 2019 survey data regarding to individual’s opinion on how people feel about sharing roads with autonomous vehicles.<br>
To begin the data processing, we first analyzed the schemas of these datasets to understand their fields, data types, and relationships. Through correlation analysis,  we identified key variables that were relevant to our modeling task, such as FamiliarityTech, AvImpact and ProvingGround.<br>
Next, we performed data cleaning and preprocessing steps. This involved handling missing values, checking outliers, identifying/removing duplicates, and addressing any inconsistencies or errors in the data. In addition, we performed data transformations. For example, we used one-hot-encoding to transform categorical variables into numerical representations.<br>
After the data preprocessing and feature engineering steps, we arrived at the final input data schema for our model. This schema consisted of a structured dataset where each row represented an unique observation, and the columns represented the input variables or features. We carefully selected the relevant variables based on their predictive power and alignment with the modeling objective.<br>
By following this data processing approach, we were able to transform the original datasets into a consistent and well-prepared input data schema that could be effectively used for training and evaluating our model.

##	Modeling, Validation
Our main objective was to predict customers' feelings of safety when using AV taxis offered by our potential clients. To accomplish this, we considered numerous factors such as familiarity with technology, the impact that autonomous vehicles may have on traffic accidents, and whether AV companies should report all safety-related incidents to the appropriate authorities, even if a police report is not mandatory.<br>
To ensure accurate and reliable results, we embarked on a comprehensive data preparation phase. This involved addressing missing values and transforming categorical variables into a suitable format for analysis. <br>
Once the data was prepared, we divided it into a training set and a testing set. This division allowed us to train our models on a substantial portion of the data while also evaluating their performance on unseen instances. We  allocated 80% of the data for training and reserved the remaining 20% for validation purposes.<br>
Our modeling approach centered around the implementation of logistic regression. This algorithm is renowned for its ability to predict binary outcomes, making it an ideal choice for our classification task.<br>
Upon completing the training process, we evaluated the model's performance on the test dataset. Our analysis revealed encouraging results. The model achieved an impressive AUC score of 0.88, indicating a strong ability to distinguish between customers who feel safe and those who do not regarding autonomous vehicles.<br>
In addition, we evaluated the model's accuracy based on test data and found it to be an impressive 93.71%. To ensure that there was no overfitting, We verified the accuracy score of the training data set, which is 91.82%. 

##	Solution Architecture
The implemented solution involved deploying a Flask app on Heroku to serve a predictive model for generating outcomes based on input data. The architecture consists of the following key components:
* Data Ingestion and Preprocessing: The raw data in a CSV format is stored in the model repository. Python libraries, such as pandas and scikit-learn, are used to ingest and load the data into memory.
* The data is fed into a trained predictive model to generate outcomes ("Yes/No"). Logistic regression from the scikit-learn library is used as the modeling algorithm for this classification task. The model is integrated into a Flask app, allowing it to process input data and provide predictions.
* The Flask app, along with the integrated predictive model, is deployed on the Heroku platform. The Heroku Procfile specifies the configuration for running the app using the gunicorn WSGI server. Dependencies are specified in the requirements.txt file, ensuring that all necessary libraries are installed during deployment.
*Clients' systems can interact with the deployed Flask app by sending input data and receiving the predicted outcomes. The Flask app's endpoints and routes are designed to handle incoming requests and provide responses with the predicted outcomes. Clients can integrate the model outputs into their systems to utilize the information for further analysis or decision-making.

###	Architecture Benefits
* Heroku provides a scalable platform for hosting and managing the Flask app, allowing it to handle a large number of requests and users.
* Heroku simplifies the deployment process, making it easy to deploy the Flask app and update it with new versions.
* The Flask app architecture allows for easy customization and integration of the predictive model with other functionalities or APIs.
* The use of Python libraries, such as pandas and scikit-learn, provides a wide range of tools and resources for data processing and modeling tasks.
* The Flask app can be accessed via API endpoints, enabling seamless integration with clients' systems and workflows.
* With the app deployed on Heroku, clients can receive predictions in real-time, making it suitable for applications that require immediate responses.
 Compared to other architectures considered, this solution offers a lightweight and scalable approach by leveraging Flask and Heroku. It allows for easy development, deployment, and integration of the predictive model, making it suitable for small to medium-scale applications. 

###	Reproducing a similar approach
* Set up Flask App
* Store the raw data in a CSV format in a suitable location, such as a local directory or a cloud storage service.and use pandas to ingest the data into memory by reading the CSV file using the `read_csv()` function..
* Train and Save the Predictive Model
* Build Flask App
* Deploy to Heroku
* Test and Verify

###	Scalable Solution Architecture 
To make the solution architecture scalable, here are proposed architecture updates: 
* Add systems to enable Load Balancing and Horizontal Scaling to distribute incoming requests across multiple instances of the Flask app and to better handle increased traffic 
* Instead of deploying a single instance of the Flask app on Heroku, use a container orchestration platform like Kubernetes for horizontal scaling to dynamically scale the application by adding or removing instances based on demand.
* Use a managed database service that can automatically scale resources as needed, such as Amazon RDS or Google Cloud Spanner.
* Implement caching mechanisms to store frequently accessed data or computed results, reducing the load on the Flask app and improving response times.
* Identify time-consuming or resource-intensive tasks in the architecture and offload them to asynchronous processes or worker queues
* Use message queues like RabbitMQ or Apache Kafka to decouple time-consuming tasks from the main request-response cycle.
* Use distributed file storage systems like Hadoop Distributed File System (HDFS) or Amazon S3 for efficient storage and retrieval of data.
* Implement monitoring and logging mechanisms to gain insights into the system's performance, identify bottlenecks, and detect anomalies. Tools like Prometheus and Grafana can help monitor key metrics and visualize the system's health.
* Use Heroku auto-scaling features to automatically adjust the number of instances based on defined metrics such as CPU usage or request throughput.

![image](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/83882370/e8b1e3fd-79b7-48b2-ae3f-00eec7d5ebe5)

##	Benefits

###	Team Benefit
Throughout the course of this project, our team had the opportunity to apply a breadth of knowledge acquired from the class, including but not limited to AGILE project management, the Cross-Industry Standard Process for Data Mining (CRISP-DM), as well as best practices in software and data science projects.<br>
The tri-weekly sprint cycle not only granted us invaluable hands-on experience but also demonstrated the efficacy of well-implemented data science project management principles. Following the established guidelines expedited our processes and enabled us to rapidly turn ideas into actionable insights.<br>
This project, therefore, served as an avenue for substantial skill growth and development within our team, promoting both individual and collective competence in the field of data science.

###	Customer Benefit
In addition to meeting all of the outlined business goals and metrics, the web application developed through this project offers significant benefits to our customers. It provides a swift and efficient way to gauge a customer's sentiment towards autonomous taxi services, all through a concise, eight-question survey. The architecture of the survey-estimation application, coupled with our predictive model, offers flexibility and adaptability. It enables our customers to rapidly modify both the survey and estimation content to suit a variety of similar scenarios, thereby enhancing its usability and potential application.

##	Learnings

### 	Project Execution
Microsoft's Team Data Science Process (TDSP), with CRISP-DM principles and AGILE approaches, is the most important learning and practice we have had through this project. Following TDSP helped us achieve our course project goals which seemed impossible at the beginning of the class. 

### Data Science / Engineering
Initially, we selected a random forest for our classification task, but the model's accuracy score was only 52%, indicating that its performance was only slightly better than random guessing.<br>
To address this issue, we attempted to incorporate additional data in order to enhance the model's accuracy. However, we encountered compatibility issues between the 2017 and 2019 datasets, preventing us from effectively leveraging the additional data.<br>
Subsequently, we decided to explore an alternative approach by utilizing logistic regression as our learner. Prior to applying this algorithm, we transformed the target variable into binary form to align it with the requirements of the prediction task.<br>
This time, we achieved a significantly improved outcome, with the model exhibiting an accuracy of over 90%, which is highly encouraging.<br>
Through this process, we learned the importance of evaluating different learners and techniques when faced with a classification task. Initially, the random forest model yielded unsatisfactory results, highlighting the need for exploration and experimentation. By attempting different approaches, such as incorporating additional data and utilizing logistic regression, we discovered the significant impact these decisions can have on the accuracy of our model.<br>
Furthermore, the challenges encountered with the compatibility of datasets served as a valuable lesson in the importance of data quality and consistency. It emphasized the need for thorough preprocessing and data validation to ensure seamless integration and optimal performance of the model.<br>
Ultimately, our experience demonstrated the iterative nature of model development and the importance of adapting and refining our approach based on feedback and results. By being open to alternative methods and continuously evaluating and improving our models, we were able to achieve substantial improvements in accuracy and gain valuable insights for future classification tasks.

### Product
During the development of our product, we made the decision to create separate pipelines for the Application and the Model, as depicted in the diagram found in the Software Architecture Document section of the report. This approach proved beneficial in maintaining code modularity and allowing our team to work simultaneously with minimal complications.<br>
Once the model and Web application were constructed on our local machines, we transferred the files to our team repository on GitHub. While using GitHub was an unfamiliar process for most of the team members, we quickly adapted and became proficient in pushing code to the shared repository. To handle user input received from the “index.html” file, we utilized a file named "routes.py". This file converted the input to JSON data and forwarded it to the model API. Subsequently, the routes.py file obtained the model's response (a recommendation of "yes" or "no") and passed it to the index.html file for display to the user.<br>
For testing our application locally, we employed Flask (Python). However, we encountered some issues related to Flask's default ports. After troubleshooting, we discovered that macOS uses port 5000, which conflicts with Flask's default port. To address this, we switched to another port using the command line instruction "flask run --port". We successfully tested the application using port 3000, ensuring proper functionality of both the model and the application.<br>
Once we confirmed the model's accuracy and ensured a user-friendly interface, we proceeded to set up the CI/CD pipeline on Heroku. We connected our GitHub repositories to Heroku and initiated the deployment process. During this stage, we encountered minor setbacks when performing manual deployment. Heroku did not support some of the Python libraries specified in our requirements.txt file. However, we managed to overcome this obstacle by removing the unsupported libraries. To ensure proper functionality, we conducted additional testing after deploying the model and application on Heroku.<br>
A few members of our team were unfamiliar with Flask and Heroku, so this project served as an excellent opportunity for us to learn and utilize these tools effectively. Acquiring the skills to locally test applications through Flask and subsequently deploy them to production using Heroku proved invaluable and can be applied to future data science projects.

###	Challenges
Our team opted to divide the development process into three main sections: the User Interface, Model, and Routing file. The User Interface and Routing file were part of the Application development pipeline, while the model had its own dedicated pipeline. This approach allowed us to work on the three main files simultaneously, which was largely successful, although we did encounter a few minor challenges.<br>
During the initial local testing of the application using Flask, we discovered that the application and model were not communicating properly. Whenever the button on the User Interface was clicked, an error page would appear. To address this issue, we organized a team meeting to investigate the root cause. Collectively, we reviewed the code and quickly identified an inconsistency in a variable name across the files. This inconsistency disrupted the communication between the HTML web form, the routes.py file, and the model. Once we corrected the variable name, the application and model functioned as intended.<br>
Through collaboration and troubleshooting, our team successfully resolved the communication issue between the User Interface, Routing file, and the model. This experience highlighted the importance of attention to detail and consistent variable naming in maintaining smooth interactions within the application. By addressing these challenges, we were able to ensure the proper functioning of the application and achieve our development goals.

##	Links
	* [Team GitHub Repo](https://github.com/orgs/CMU-SoftwareDesignforDS-Team/repositories)
	* [Application on Heroku](https://av-web-app-7937597eefbd.herokuapp.com/)

##	Next Steps
Based on the metrics stated earlier in the report, the goal is to improve the users feeling of safety and comfortability by 10% in 4 weeks time.<br>
After promotion of the free AV taxi-ride app for 4 weeks, we will re-survey people in the Pittsburgh area to hopefully improve the population's opinion on sharing the road with autonomous vehicles.

## Appendix
* Figure1
  ![image](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/83882370/cfa8ef23-07b3-470e-b07d-73692d2bbff1)
* Figure2
  ![image](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/83882370/1df5393c-daa6-4dad-a81d-bb7f0e697d75)
* Figure3
  ![image](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/83882370/e133b9a8-5c74-458f-a1d0-5000fcbef9af)
* Figure4 Model Accuracy
  ![image](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/83882370/24b73715-c622-4d73-a131-9c3c896cd60a)
* Figure5 Coefficients
  ![image](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/83882370/1f02c31f-9a31-447b-9a36-569ae24b0fce)
  
Feature Sets Summary
* 2019SurveryFeatures contains 66 non-missing variables. Below is the snapshot of
2019SurveryFeatures:
  ![image](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/83882370/e4e8b65e-9b17-4d37-a3a6-92927dbb91a4)
*  2017PublicSurveyFeatures contains 54 non-missing variables. Below is a snapshot of the
survey features:
  ![image](https://github.com/CMU-SoftwareDesignforDS-Team/AutoVehicles/assets/83882370/18d91959-2687-4d7a-8566-3c498f7e7e03)
