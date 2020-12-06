# Amazon SageMaker Inference and Endpoint

In this section, you will run the inference.py script to communicate with the Amazon SageMaker endpoint created in the previous task.

### Steps: 
* Return to your Cloud9 SageMakerOnAWS environment.
* Inspect the contents of the ex-driver/inference.py file. The following code invokes the new endpoint for an inference. The code passes in a representation of the road data and an inference is returned.

    # ask sagemaker linear learner for the car direction
    body = ",".join(road_csv)
    response = client.invoke_endpoint(
        EndpointName='driving-endpoint',
        Body=body,
        ContentType='text/csv'
    )
    interfence = json.loads(response['Body'].read())
    label = int(interfence["predictions"][0]["predicted_label"])

The inference JSON response contains predictions, scores for each label and a predicted_label. The code uses the predicted_label make a direction decision.

    {
      "predictions": [
        {
          "score": [
            0.9913098216056824,
            0.008546961471438408,
            0.000143218640005216
          ],
          "predicted_label": 0
        }
      ]
    }

* Run the following commands in your AWS Cloud9 terminal to change to the exercise folder and run the inference code:

    cd ~/environment/ex-driver
    python3 inference.py

* You have the option of running the simulated car against a random or sine wave road. Press CTRL+C or COMMAND+C to break out of the program, or wait for it to complete.
