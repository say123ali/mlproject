# End-to-End-ML-Project

Complete project structure and understanding Structure for End to End Data Science Projects (For Production)



1. Create Virtual Environment: Virtual Environment for separate projects
2. Create Requirements.txt file: To install libraries (e.g., numpy, pandas)
3. Create setup.py file: Whenever we want to convert the whole project into the packages
4. Creating notebooks folder: it's just for to do our EDA purpose.
5. create config folder : it have files like
• config.yaml :contains configuration for all the project structure
• model.yaml : contains Model & parameters for Hyperparameter Tuning
• schema.yaml : It contains Data set Schema We use it in Data validation
6. Creating a project name folder: My entire machine learning life cycle should be run inside this folder. Whenever we create a folder, we should always create an init.py file. Because this source folder is also a package, we should be able to reuse it and install it somewhere else. We should create the below files and folders inside the source file.
(i) __init__.py - To convert this folder into a package
(ii) exception/exception.py - To handle the exceptions
(iii) logger/logger.py - To create a log file
(iv) util/utils.py - utils.py file basically means any generic functionality probably that I want to create for this entire project.
(v) config/configuration.py : It contains the project configuration and necessary function for it
(vi) constants/__init__.py: This file contains the that is been define for ease of flow
(vii) Entity
• artifact_entity.py: it contains all the artifacts predefined schema type in python data structure.
• config_entity.py: it contains configuration schema for each component steps
• model_facory.py: it contains function and classes for tune the hyperparameter for model
(viii) Components Folder
• __init__.py file (inside components folder) – To convert this component folder into a package
• data_ingestion.py file (inside components folder): To extract the dataset from databases or somewhere else.
• data_validation.py: validate the dataset schema if data us been changes the pipe should break.
• data_transformation.py file (inside components folder) - To do feature engineering.
• model_trainer.py file (inside components folder) - To create a model.
• model_evaluation.py: evaluation of model is done on testing data
• model_pusher.py: In that part model comparison with current production is been conducted if newly trained model better one model then been push to production
(ix) Pipeline/pipeline.py : running code in continuous pipeline
6. Artifacts folder - This folder will create by code not manually, this folder is for saving our outputs.
7. Logs - To saving the log details and this folder will create by code not manually.
8. app.py - To create a web application for our model
9. templates folder : Containes html file
10. Dockerfile - To deploy in the cloud.
