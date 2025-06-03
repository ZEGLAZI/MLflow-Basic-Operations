# MLflow-Basic-Operations


## For Dagshub

import dagshub
dagshub.init(repo_owner='ZEGLAZI', repo_name='my-first-repo', mlflow=True)

import mlflow
with mlflow.start_run():
  mlflow.log_param('parameter name', 'value')
  mlflow.log_metric('metric name', 1)


  # MLFLOW on AWS Setup:

  1. Login to AWS console
  2. Create IAM user with AdministratorAccess
  3. Export the credentials in your AWS CLI by running "aws configure"
  4. Create a s3 bucket
  5. Cretae EC2 machine (ubunto) & add Security groups 5000 port

  Run the following command on EC2 machine
  "" bach 
  sudo apt update
  sudo apt install python3-pip
  sudo pip3 install pipenv
  sudo pip3 install virtualenv
  mkdir mflow
  cd mlfow

  pipenv install mlflow
  pipenv install awscli
  pipenv install boto3
  pipenv shell

  # Then set aws credentials
  aws configure

  # finally

  mlflow server -h 0.0.0.0 -default-artifact-root s3://mlflow-test-23

  # open public IPv4 DNS to the port 5000

  # set uri in your local terminal and in your code
  export MLFLOW_TRACHINK_URI=http://ec2-54-147-36-34.compute-1.amazonaws.com:5000

"""



