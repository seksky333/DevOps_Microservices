Status: [![CircleCI](https://circleci.com/gh/seksky333/DevOps_Microservices.svg?style=svg)](https://circleci.com/gh/seksky333/DevOps_Microservices)

## Project Overview
This project uses a pre-trained, `sklearn` model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. This project will also use Python Flask to serve out predictions (inference) about housing prices through API calls, and the app will be running in Kubernete Cluster. 

### Project Tasks
Your project goal is to operationalize this working, machine learning microservice using [kubernetes](https://kubernetes.io/), which is an open-source system for automating the management of containerized applications. In this project you will:
* Test your project code using linting
* Complete a Dockerfile to containerize this application
* Deploy your containerized application using Docker and make a prediction
* Improve the log statements in the source code for this application
* Configure Kubernetes and create a Kubernetes cluster
* Deploy a container using Kubernetes and make a prediction
* Upload a complete Github repo with CircleCI to indicate that your code has been tested


## Setup the Environment

* Create a virtualenv and activate it
* Run `make install` to install the necessary dependencies

### Running `app.py`

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  `./run_kubernetes.sh`

### Kubernetes Steps

* Setup and Configure Docker locally
* Setup and Configure Kubernetes locally
* Create Flask app in Container
* Run via kubectl

## File structure
Dockerfile - Docker configuration
app.py - Contains the main logic of the application
make_prediction.sh - Using curl to make a POST request with predefinied input to request a prediction from the server from port 8000
output_txt_files - Contains log file outputs from the Docker Container and the Kubernete
requirements.txt - Indicate what libraries and which version should be downloaded to run the Python app
run_docker.sh - A shell script to run the Docker Container
run_kubernetes.sh - A shell script to run the Kubernete
upload_docker.sh - A shell script to tag and push the Docker Container to the remote repo
