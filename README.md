# Project by Valeriy Chernyy

## An overview of the project
The objective of this project is to create a machine learning model, deploy it to production and to allow the users to consume it.
In order to do this, several steps were taken. Firstly, I created a machine learning model usn the AutoML. The model was trained and tested on the

## An architectural Diagram

![alt text](https://github.com/vcherny/project_2_final/blob/main/Architectural%20diagram.JPG)

## Key Steps
# 1. Create a new AutoML run
1.1. Upload the required data:
![alt text](https://github.com/vcherny/project_2_final/blob/main/Registered_datasets.PNG)
1.2. Create, and run the experiment: 
![alt text](https://github.com/vcherny/project_2_final/blob/main/Experiment_completed.PNG)
# 2. Deploy and consume the model
2.1. The model is consume via an enpoint. one can enable the allpication insights to see e.g. if requests are failing: 
![alt text](https://github.com/vcherny/project_2_final/blob/main/application_insights_enabled.PNG)
2.2. One can enable the logs via the terminal. Output of the logs shown below indicate that the endpoint is healthy and can accept the reqursts:
![alt text](https://github.com/vcherny/project_2_final/blob/main/output_logs.PNG)
2.3. It is possible to consume the model using swagger. Insights the swagger there are a number of methods available:
![alt text](https://github.com/vcherny/project_2_final/blob/main/swagger_api_methods_responses_1.PNG)
2.4. Alternatively, one can send the data and receive results using python:
![alt text](https://github.com/vcherny/project_2_final/blob/main/Output%20from%20the%20modle.PNG)
# 3. Creation of a pipeline
3.1. A pipeline was created in Jupyter notebook. An overview of the completed pipelines can be found in Azure ML studio in the Pipelines section:
![alt text](https://github.com/vcherny/project_2_final/blob/main/pipelines%20overview.PNG)
3.2. The Automl module is assigned to the bankmarketing dataset (I called banking_dataset):
![alt text](https://github.com/vcherny/project_2_final/blob/main/bankmarketing%20with%20automl%20model.PNG)
3.3. Once the pipeline is published, an overview can be found in the corresponding section. Once the endpoint is ready, the status is ACTIVE:
![alt text](https://github.com/vcherny/project_2_final/blob/main/Published_pipeline_overview.PNG)
#4. Configure a pipeline with the Python SDK
4.1. It is possible to configure the pipeline via the notebook, here is the “Use RunDetails Widget” with the step runs:
![alt text](https://github.com/vcherny/project_2_final/blob/main/Jypyter_pipeline_run_4.JPG)
4.2. In Azure ML studio it is possible to verify that the endpoint is active (status):
![alt text](https://github.com/vcherny/project_2_final/blob/main/pipeline%20endpoint.PNG)
4.3. The pipeline run can also be seein in Azure ML studio: 
![alt text](https://github.com/vcherny/project_2_final/blob/main/scheduled%20run.JPG)
## A short description of how to improve the project in the future
The project can be improved by creating a more complete swagger documentation including utilization of the methods.
Another aspect of improvement is a more complete validation of the endpoint results. Currently the  The provided version of endpoint.py contains only two sets of data. However, one can potentially reproduce the metrics results produced by the model within Automl if the corresponding dataset is provided. That can be done relatively easy by improving the endpoint.py script.
# A link to te screencast vodeo on YouTube: https://youtu.be/PZa6OJJUFRc
