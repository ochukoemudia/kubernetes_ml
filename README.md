[![ochukoemudia](https://circleci.com/gh/ochukoemudia/kubernetes_ml.svg?style=svg)](https://app.circleci.com/pipelines/github/ochukoemudia/kubernetes_ml?branch=master)

## Project Overview

This is a pre-trained, sklearn model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on the data source site. This project tests your ability to operationalize a Python flask app—in a provided file, app.py—that serves out predictions (inference) about housing prices through API calls. This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.

### Files Explaination

Dockerfile - Contains commands used to create a docker image
Makefile - Contains useful set of commands to setup environment, run tests and run lints
app.py - Python flask app that returns predictions about housing prices when requested using API calls
make_prediction.sh - Send API request to Flash app running and receives response
run_docker.sh - Script to build and run docker image locally
upload_docker.sh - Script to tag and upload docker image to docker hub
run_kubernetes.sh - Script to setup and run app on kubernetes
.circleci/config.yml: CircleCI configuration file for running the tests
templates/index.html: Frontend of this project where you can send input and receive a prediction

## Requirements
Python 3.7

## Steps to take

Step 1: Fork and clone the repository

Step 2: Install dependencies
  Set up the environment by running make setup. This will create a virtual environment in your home directory called .devops
  Install dependencies by running make install
  
Step 3: Run Docker container
  Run the application on docker by calling ./run_docker.sh

Step 4: Upload to Docker Hub
  In the ./upload_docker.sh file, edit the dockerpath (line 8) and change the docker username
  To upload to docker hub, run ./upload_docker.sh

Step 5: Kubernetes deployment
  To deploy to kubernetes, run ./run_kubernetes.sh
