[![asantosnav](https://circleci.com/gh/asantosnav/microservices.svg?style=svg)](https://github.com/asantosnav/microservices)

## Project Overview

In this project operationalize a Machine Learning Microservice API, a Python flask app—in a provided file, `app.py`—that serves out predictions (inference) about housing prices through API calls.


## Files in the repository

- app.py: Flask app written in Python that makes prediction of housing prices
- Dockerfile: Builds a container
- Makefile: File with the necessary steps to prepare the enviroment and make lint tests
- run_docker.sh: Runs a container
- requirements.txt: Lists all the dependencies needed for creating the enviroment
- run_kubernetes.sh: Runs a container inside a Kubernetes pod
- make_prediction.sh: Sends necessary JSON data as input to make a prediction (must be run inside a container)
- upload_docker.sh: Upload container to Docker repo



## Setup the Environment

* Create a virtualenv and activate it. In the terminal:
	Run `make create`
	Run `make activate`

* Run `make install` to install the necessary dependencies

* Run `make lint` to check the app and the Dockerfile locally

### Making a prediction

1. Run in Docker:  `./run_docker.sh`
	In a separate tab, `sh make_prediction.sh`
2. Run in Kubernetes:  `./run_kubernetes.sh`
	In a separate tab, `sh make_prediction.sh`



### Upload Docker container

* Run `upload_docker.sh`

