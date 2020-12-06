# Amazon SageMaker Model and Endpoint

In this section, you will create the Amazon SageMaker model. A model contains a reference to the location of your inference code and optionally associated artifacts. Next, you will create an Amazon SageMaker endpoint. The endpoint provisions resources and deploys the model for Amazon SageMaker hosting services.

### Steps:
* Return to the Amazon SageMaker dashboard.
    - In the left navigation pane, click Training jobs, and choose driving-training.
    - For Actions, click Create model.
* On the Create model screen, for Model name, enter driving-model.
    - Note Location of inference code image and Location of model artifacts are populated for you with details from your driving-training job.
    - Click Create model.
* To create an endpoint for your model, choose driving-model.
    - Click Create endpoint.
    - On the Create and configure endpoint screen, for Endpoint name, enter driving-endpoint.
    - Ensure Create a new endpoint configuration is selected.
    - For Endpoint configuration name, enter driving-endpoint-configuration.
    - In the Production variants table, click Edit.
    - Modify the Instance type to ml.t2.medium, and click Save.
    - Click Create endpoint configuration.
    - Click Create endpoint.

Creating the endpoint takes about 10 minutes to complete.
