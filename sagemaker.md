# Sagemaker

## intro

docs: <https://aws.amazon.com/sagemaker/>

- end to end cloud-hosted machine learning environment.
- includes tooling for building, training, deploying and managing Machine Learning (ML) models.
- Sagemaker Studio is cloud native IDE for managing all of these services.
- uses Jupyter notebooks and a Sagemaker SDK to manage resources (eg. containers for hosting ML models).

## how it works

- can build models in cloud hosted jupyter notebooks using off the shelf algorithms like XGBoost or custom written ones (with custom training scripts).
- then use the Sagemaker SDK to provision resources in AWS for training and running models.
- models are run in docker containers which are stored in Elastic Container Repository (ECR) and run in Elastic Container Service (ECS).
- these containers can then be deployed to endpoints where they are available to be accessed by HTTPS by external apps.

**All infrastructure can be entirely managed by code in the notebooks which creates is using the SDK.**

## breakdown of services

Bunch of subservices including, but not limited to:

- Sagemaker Ground Truth - for creating/managing test data sets for training models
- Sagemaker Autopilot - used for automating building and training ML models, but with complete visibility into the code (I presume this means you can manually edit the code as well)
- Sagemaker Debugger - debug and profile the training runs

## alternatives

[Amazon Forecast](https://aws.amazon.com/forecast/) is a fully managed forecasting ML tool. Used for time series data.
You don't manage the ML models, Forecast automatically does all the algo selection, training, accuracy metrics and forecasting.
All you need to do is upload historic data to S3 and link it to Forecast.

**No visibility into the code and less customisable but may be easier/faster to set up and use.**
