# Amazon SageMaker Training Job

### Steps: 
* Return to your Cloud9 SageMakerOnAWS environment.
* Use the AWS CLI to copy your training.csv file to the newly created S3 bucket. NOTE In the following command, replace REPLACE_WITH_YOUR_INITIALS with your initials to match the bucket you created earlier.

    aws s3 cp ~/environment/ex-driver/training.csv s3://REPLACE_WITH_YOUR_INITIALS-sagemaker

* In the console, click Services, and then click Amazon SageMaker to open the Amazon SageMaker dashboard.
  - Make sure you are in the Oregon Region.
  - In the left navigation pane, click Training jobs, and then click Create training job.
  - For Job name, enter driving-training.
  - For IAM role, select Create a new role.
  - In Create an IAM role, choose Any S3 bucket, and then click Create role.
  - For Algorithm, select Linear Learner.
  - Scroll to the Hyperparameters section.
  - For feature_dim, enter 250. This is the shape of the road representation – 10 rows * 25 columns = 250 features.
  - For mini_batch_size, enter 100. For the small set of training data, you need to lower this size.
  - For predictor_type, enter multiclass_classifier.
  - For num_classes, enter 3. You are classifying the data into three classes – turn left, drive straight, and turn right.
  - Scroll to the Input data configuration section.
  - For Content type, enter text/csv.
  - For S3 data type, choose S3Prefix.
  - For S3 location, enter s3://REPLACE_WITH_YOUR_INITIALS-sagemaker/training.csv.
  - Click Done.
* Scroll to the Output data configuration section.
  - For S3 output path, enter s3://REPLACE_WITH_YOUR_INITIALS-sagemaker/.
* Click Create training job.
