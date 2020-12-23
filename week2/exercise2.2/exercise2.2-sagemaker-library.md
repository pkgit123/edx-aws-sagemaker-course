# Exercise 2.2 - SageMaker Library

For more information about the Amazon SageMaker high-level Python library see:

    https://github.com/aws/sagemaker-python-sdk
    https://sagemaker.readthedocs.io/en/latest/

### 1. Start the Amazon SageMaker notebook instance.

In this section, you will return to your SageMaker notebook instance and start the instance.
Expand for step-by-step instructions.


### 2. Download notebook code to the notebook instance.

In this section, you will download the Amazon-SageMaker-high-level-Python-library.ipynb notebook and training.csv file to your instance.

* To download the Amazon-SageMaker-high-level-Python-library.ipynb notebook, open a terminal window. For New, click Terminal.
    * JupyterLab -> New Terminal
    ```
    $ pwd
    $ ls
    $ cd ~/SageMaker
    ```
* Run the following commands to change the directory, and download the notebook and .csv file.

    ```
    cd ~/SageMaker/
    wget https://us-west-2-tcdev.s3.amazonaws.com/courses/AWS-100-MLS/v1.0.0/exercises/notebooks/Amazon-SageMaker-high-level-Python-library.ipynb
    wget https://us-west-2-tcdev.s3.amazonaws.com/courses/AWS-100-MLS/v1.0.0/exercises/notebooks/training.csv
    ```

* Return to the Jupyter notebook home. The browser tab is labeled Home.

### 3. Run the notebook code on the notebook instance.

You now have everything on the notebook instance you need to run the high-level library demonstration. As with the previous notebook exercise, you can complete the exercise by running each cell in the notebook.

### 4. End running Jupyter processes, and stop the notebook instance.

* From the Jupyter notebook home, click Running.
* Click Shutdown next to the terminal and notebook.
* To stop the notebook instance, return to the AWS console, and click Services > Amazon SageMaker to open the Amazon SageMaker dashboard.
* In the left navigation pane, click Notebook instances, and then click Stop next to the edXSageMaker instance.

### 5. Delete the endpoint configuration and model.

* Return to the the Amazon SageMaker dashboard.
* In the left navigation pane, click Endpoints, and ensure the endpoint created by the notebook is removed.
* In the left navigation pane, click Endpoint configurations, and choose the option for the endpoint that starts with linear-learner.
* For Actions, click Delete.
* Click Delete to confirm.
* In the left navigation pane, click Models, and choose the option for the model that starts with linear-learner.
* For Actions, click Delete.
* Click Delete to confirm.

