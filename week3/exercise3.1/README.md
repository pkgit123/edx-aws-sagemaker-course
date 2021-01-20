# Exercise 3.1 Instructions

### 1. Start the Amazon SageMaker notebook instance.
1. Sign in to the AWS Management Console as the edXSageMakerUser IAM user.
1. In the console, click Services > Amazon SageMaker to open the Amazon SageMaker dashboard.
1. Make sure you are in the Oregon Region.
1. In the left navigation pane, click Notebook instances, and then click Start next to the edXSageMaker instance.
1. When the notebook instance status moves to InService, click Open to open the notebook in a new browser tab.
1. In this section, you will launch the sample kmeans_mnist.ipynb notebook into your notebook instance.
1. The Amazon SageMaker examples are maintained in a Git repository at https://github.com/awslabs/amazon-sagemaker-examples.

### 2. Start the Amazon SageMaker example.
1. From the Jupyter notebook home, click SageMaker Examples.
   * Harder to navigate in JupyterLab ... easier to navigate in JupyterNotebook
   * There are over 20 sections of examples, with dozens of notebooks in each section
   * In JupyterLab, this is on left-pane-menu
1. Locate the kmeans_mnist example in SageMaker Python Sdk > kmeans_mnist.ipynb, and click Use.
1. Click Create copy to copy and launch the example.
1. To complete the example notebook, run each individual cell, and inspect the output from each run.
  * sagemaker -> get_execution_role()
  * sagemaker.session -> Session()
  * role
  * bucket
  * Download data, unzip, pickle
  * sagemaker -> KMeans() -> output_path, data_location
  * kmeans.fit()
  * kmeans.fit(kmeans.record_set(train_set[0]))
  * kmeans.deploy()
  * kmeans.deploy().predict()
  
  

### 3. End running Jupyter processes, and stop the notebook instance.
1. From the Jupyter notebook home, click Running.
1. Click Shutdown next to the terminal and notebook.
1. To stop the notebook instance, return to the AWS console, and click Services > Amazon SageMaker to open the Amazon SageMaker dashboard.
1. In the left navigation pane, click Notebook instances, and then click Stop next to the edXSageMaker instance.


### 4. Delete the endpoint configuration and model.
1. Return to the the Amazon SageMaker dashboard.
1. In the left navigation pane, click Endpoints, and ensure the endpoint created by the notebook has been removed.
1. In the left navigation pane, for Endpoint configurations, click the the endpoint that starts with kmeans.
1. For Actions, click Delete.
1. Click Delete to confirm.
1. In the left navigation pane, for Models, click the model that starts with kmeans.
1. For Actions, click Delete.
1. Click Delete to confirm.
