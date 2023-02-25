
[![CircleCI](https://dl.circleci.com/status-badge/img/gh/andrea2025/devops_microservice-kubernetes/tree/master.svg?style=svg)](https://dl.circleci.com/status-badge/redirect/gh/andrea2025/devops_microservice-kubernetes/tree/master)


## Project Overview
The Operationalize ML project contains a Machine Learning Microservice, built on Scikit-Learn. It contains a model that predicts house prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on the data source site.

## What does this project do?
* Run a docker container
* Upload container into a public registry (hub.docker.com)
* Run the deployed application in a Kubernetes cluster
* Integrate with CircleCI for continuous integration
## Requirements
* Python 3.7
## START HERE
### Step 0
* Fork this repo and clone it to your local computer
### Step 1: Install dependencies
* Set up the environment by running make setup. This will create a virtual environment in your home directory called .devops
* Install dependencies by running make install
### Step 2: Run Docker container
* Run the application on docker by calling ./run_docker.sh
### Step 3: Upload to Docker Hub
* In the ./upload_docker.sh file, edit the dockerpath (line 8) and change the docker username to a personalized one (or leave it as is, to use the public andrea45/udademoproject1)
* To upload to docker hub, run ./upload_docker.sh
### Step 4: Kubernetes deployment
* To deploy to kubernetes, run ./run_kubernetes.sh

