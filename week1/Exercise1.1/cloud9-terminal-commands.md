# Cloud9 terminal commands

Download and run the training code.

In this section, you will download and extract the source code for this exercise. The source package contains the training.py script, which you will use to create training data for your SageMaker model.

To download and extract the application code, run the following commands in your AWS Cloud9 terminal:

    cd ~/environment
    
    wget http://us-west-2-tcdev.s3.amazonaws.com/courses/AWS-100-MLS/v1.0.0/exercises/ex-driver.zip -O ex-driver.zip
    
    unzip ex-driver.zip

Change to the ex-driver directory, and use pip to install the Python requirements. This command installs boto3 onto your Cloud9 instance. This is needed later in the exercise when you run inference.py.


    cd ~/environment/ex-driver
    
    pip-3.6 install -r requirements.txt --user

Use the following command to launch training.py. Use the arrow keys to drive the car on the sine wave track. The road display is always relative to the car. Think of it as data from a sensor array on the front of the car.

    python3 training.py

The training.py command generates a CSV file from your training session. The file contains labeled data of your steering decisions and a representation of how the road looked at the time you made each decision.
