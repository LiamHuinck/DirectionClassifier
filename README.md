# MLflow example using a cnn model.

This repository will include an example of how to use mlflow a machine learning toolkit to implement ci/cd for the ml/ai models.

Based on the following reference tutorial"https://mlflow.org/docs/latest/ml/getting-started/deep-learning/

## Requirements
This project is written in python using uv as a package manager. I am using pytorch with cuda capabilities as my machine learning package to train the cnn mode.


# How to initialize the MLflow process

We can start a MLflow local server using the following command in a bash script: ``` mlflow server --port 5000```
This will start a local hosted server with the MLflow UI that lets you explore the trained model's metrics as well as other information.

(Should be updated when its more clear what can be done with MLflow)

When the local hosted server is running we can use the following to test if the connection is working:

```python
import mlflow

# Print connection information
print(f"MLflow Tracking URI: {mlflow.get_tracking_uri()}")
print(f"Active Experiment: {mlflow.get_experiment_by_name('my-first-experiment')}")

# Test logging
with mlflow.start_run():
    mlflow.log_param("test_param", "test_value")
    print("✓ Successfully connected to MLflow!")
```

After this we can implement it in our training 
