[![HasanDevOps2003](https://circleci.com/gh/HasanDevOps2003/project-4.svg?style=svg)](https://app.circleci.com/pipelines/github/HasanDevOps2003/project-4/1/workflows/378c2d0f-99cb-4eed-af9d-fff52d075a98)

# Project-4

## Project Overview

In this project, you will be able to deploy Python flask application. The purpose of the application is to predict house prices through API calls. The application uses a pre-trained, sklearn model which has been trained to predict the price of houses in Boston.

### Project Tasks

- Create a docker file which containerizes the application
- Check quality of code using linting
- Deploy application using docker and make a prediction through API
- Create a kubernetes cluster and deploy application into the cluster and make a prediction through API
- Configure CircleCi

## Setup the Environment

* Create a virtualenv with Python 3.7 and activate it. Refer to this link for help on specifying the Python version in the virtualenv. 
```bash
python3 -m pip install --user virtualenv
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

## Repository Files

- [.circleci](https://github.com/HasanDevOps2003/project-4/tree/main/.circleci) - contains config file for circleci workflows
- [model_data](https://github.com/HasanDevOps2003/project-4/tree/main/model_data) - contains model data for the application
- [output_txt_files](https://github.com/HasanDevOps2003/project-4/tree/main/output_txt_files) - contains files which has the outputs when running run_docker.sh and run_kubernetes.sh scripts
- [Dockerfile](https://github.com/HasanDevOps2003/project-4/blob/main/Dockerfile) - Dockerfile which containerizes the application
- [Makefile](https://github.com/HasanDevOps2003/project-4/blob/main/Makefile) - The Makefile includes instructions on environment setup and lint tests
- [app.py](https://github.com/HasanDevOps2003/project-4/blob/main/app.py) - Python flask app
- [make_prediction.sh](https://github.com/HasanDevOps2003/project-4/blob/main/make_prediction.sh) - Interacts with application and returns a prediction
- [requirements.txt](https://github.com/HasanDevOps2003/project-4/blob/main/requirements.txt) - List of requirements installed in make install
- [run_docker.sh](https://github.com/HasanDevOps2003/project-4/blob/main/run_docker.sh) - Deploys application using docker locally
- [run_kubernetes.sh](https://github.com/HasanDevOps2003/project-4/blob/main/run_kubernetes.sh) - Deploys application in kubernetes cluster
- [upload_docker.sh](https://github.com/HasanDevOps2003/project-4/blob/main/upload_docker.sh) - Uploads docker application to docker