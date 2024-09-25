# simple-devops-project


## Project Overview

This is a simple web application built using Python and Flask, which is served with Gunicorn. The application demonstrates a CI/CD pipeline using GitHub Actions, Docker, and Kubernetes. This project is designed for learning and showcases the deployment process for a basic web app.

## Table of Contents

- [Features](#features)
- [Technologies Used](#technologies-used)
- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
- [Running the Application Locally](#running-the-application-locally)
- [CI/CD Pipeline](#cicd-pipeline)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [License](#license)

## Features

- Simple REST API built with Flask.
- Dockerized application for easy deployment.
- CI/CD pipeline using GitHub Actions.
- Deployment on Kubernetes.

## Technologies Used

- Python 3.8
- Flask
- Gunicorn
- Docker
- GitHub Actions
- Kubernetes

## Prerequisites

Before you begin, ensure you have the following installed:

- [Docker](https://www.docker.com/get-started)
- [kubectl](https://kubernetes.io/docs/tasks/tools/)
- A GitHub account
- A Docker Hub account (optional for pushing images)

## Getting Started

### Clone the Repository

Clone this repository to your local machine:

git clone https://github.com/YOUR_GITHUB_USERNAME/simple-devops-app.git
cd simple-devops-app

Build the Docker Image
Build the Docker image using the following command:
docker build -t simple-devops-app .

Running the Application Locally
Run the Docker container:
docker run -p 5000:5000 simple-devops-app
Access the application at http://localhost:5000.

CI/CD Pipeline
This project includes a CI/CD pipeline set up with GitHub Actions. On every push to the main branch, the following steps are executed:
1. Checkout the code.
2. Login to Docker Hub.
3. Build the Docker image.
4. Push the image to Docker Hub.
You can see the actions by navigating to the Actions tab in your GitHub repository.

Deployment
To deploy the application on a Kubernetes cluster:
1. Create the deployment and service:
kubectl apply -f k8s/deployment.yaml
kubectl apply -f k8s/service.yaml

2. Verify the deployment:
kubectl get pods
kubectl get services

3. Access the application using the Nodeport and minikubeip

