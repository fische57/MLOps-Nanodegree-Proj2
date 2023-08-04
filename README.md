# Proj2-Nanodegree
Operationalizing Machine Learning for Udacity ML-Ops Nanodegree

# Overview
In this project, I used Azure to configure a cloud-based machine learning production model, deploy it, and consume it. I also created, published, and consumed a pipeline. 

Project main steps:
1. Automated ML Experiment: In an Azure workspace, an AutoML experiment was ran for Classification using the Bank Marketing dataset. 
2. Deploy the best model: The best model was determined by weighted AUC, then deployed as a web service using Azure Container Instance. 
3. Enable logging: See the logs.py file. Application insights were also enabled. Outputs of this file showed any potential issue with the deployment. 
4. Swagger Documentation: A Swagger user interface was served locally using swagger.sh, swagger.json, and serve.py. The swagger.json comes from the Swagger URI provided in the deployed model's endpoints. 
5. Consume model endpoints: Using the REST API and the primary key in the endpoints.py file, I was able to send data to the model, and receive a "yes" or "no" result for each customer. 
6. Create and publish a pipeline: Each cell of the included file named aml-pipelines-with-automated-machine-learning-step.ipynb was completed, creating and publishing a pipeline from workspace, to dataset, to REST endpoint. 
7. Documentation: this README, including screenshots and screencast!
![image](https://github.com/fische57/Proj2-Nanodegree/assets/52047242/b6f1a337-5e2b-4621-89e4-5d77127cf0b7)

Source: Udacity Machine Learning Engineer with Microsoft Azure Nanodegree Project: Operationalizing Machine Learning

The dataset used in this model is the Bank Marketing dataset provided by the Udacity course, which has a binary outcome variable "y". It is used to determine best strategies for a bank to market its customers. Classification models were evaluated in an automated ML experiment to determine the best model based on AUC score. In this experiment, the best model was determined to be the VotingEnsemble algorithm, by its weighted AUC of 0.94799. This model was then deployed to a web service, using Azure Container Instance, and the REST endpoint was consumed by a Swagger User Interface. The final result is that a user can submit information about a customer based on the columns of the dataset, and receive a predicted outcome from the model, "yes" or "no" for that customer. 

# Architectural Diagram
![image](https://github.com/fische57/Proj2-Nanodegree/assets/52047242/4a1d0635-c075-4aeb-bf74-4c3d34511812)


# How to Improve
The purpose of this project was to practice deploying a model, so I did not fully evaluate the results of the AutoML experiment, other than noting the description of the best model and where to find metrics and logging. To improve, I would spend more time on this step, to make sure the model performance met my business constraints, and determine if other advanced settings should be considered. For example, I could try an alternative model rather than Classification. 

# Screenshots
![image](https://github.com/fische57/Proj2-Nanodegree/assets/52047242/a4afa3e7-918b-438e-b5ce-9d9d408f9733)

# Screencast 
https://youtu.be/8EHbbfI4wX8
