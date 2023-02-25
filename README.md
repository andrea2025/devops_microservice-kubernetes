
[![CircleCI](https://dl.circleci.com/status-badge/img/gh/andrea2025/devops_microservice-kubernetes/tree/master.svg?style=svg)](https://dl.circleci.com/status-badge/redirect/gh/andrea2025/devops_microservice-kubernetes/tree/master)


Project Overview
The Operationalize ML project contains a Machine Learning Microservice, built on Scikit-Learn. It contains a model that predicts house prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on the data source site.

What does this project do?
Run a docker container
Upload container into a public registry (hub.docker.com)
Run the deployed application in a Kubernetes cluster
Integrate with CircleCI for continuous integration
Requirements
Python 3.7
START HERE
Step 0
Fork this repo and clone it to your local workstation (obviously)
Step 1: Install dependencies
Set up the environment by running make setup. This will create a virtual environment in your home directory called .devops
Install dependencies by running make install
(Optionally) Lint application (requires hadolint)
Step 2: Run Docker container
Run the application on docker by calling ./run_docker.sh
Step 3: Upload to Docker Hub
In the ./upload_docker.sh file, edit the dockerpath (line 8) and change the docker username to a personalized one (or leave it as is, to use the public kcemenike/microproject:v1.0.0)
To upload to docker hub, run ./upload_docker.sh
Step 4: Kubernetes deployment
To deploy to kubernetes, run ./run_kubernetes.sh
Footer
© 2023 GitHub, Inc.
Footer navigation
Terms
Privacy
Security
Status

# You should have Python 3.7 available in your host. 
# Check the Python path using `which python3`
# Use a command similar to this one:
python3 -m virtualenv --python=<path-to-Python3.7> .devops
source .devops/bin/activate
```
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
