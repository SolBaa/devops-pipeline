# Dockerized Application Deployment and Orchestration

### Objective
This task is aimed at assessing your skills and understanding of Docker containerization and deployment. You will be required to containerize a sample application, set up a Docker-based deployment pipeline, and configure container orchestration using Kubernetes.

### Instructions

#### Application Description
- Choose a sample application or create a simple application of your choice (e.g., web application, microservice, etc.).
- The application should be containerized using Docker, allowing it to run consistently across different environments.

#### Dockerization Requirements
- Write a Dockerfile to build a Docker image for your application.
- Ensure the Docker image includes all necessary dependencies and configurations.
- The Docker image should be lightweight, optimized, and follow best practices.

#### Deployment Pipeline
- Set up a CI/CD pipeline using any CI/CD tool of your choice (Github Actions).
- Configure the pipeline to trigger a build whenever changes are pushed to the application's Git repository.
- Implement the following stages in your pipeline:
  1. **Build**: Build the Docker image using the Dockerfile.
  2. **Test**: Run tests against the Docker image or the deployed container.
  3. **Publish**: Push the Docker image to a Docker registry (Docker Hub).
  4. **Deploy**: Deploy the Docker image to a Kubernetes cluster.

#### Kubernetes Orchestration
- Set up a Kubernetes cluster with a minimum of two nodes.
- Configure the cluster to use a load balancer for distributing traffic to the deployed application.
- Automate the deployment and scaling of the application using Kubernetes deployments and services.

#### Additional Requirements
- Include a README file with instructions on how to set up and run the Dockerized application and the deployment pipeline.
- Utilize environment variables or configuration files for application-specific configurations.
- Consider security best practices, such as securing the Docker daemon, managing secrets, and restricting access to sensitive information.


# How to run the app


This is a simple FastAPI application which can be containerized using Docker.

## Requirements
- Git
- Docker

## Clone the repository
```bash 
git clone https://github.com/SolBaa/devops-pipeline.git
cd devops-pipeline
```
## Build Docker Image

To build a Docker image for the application, navigate to the root directory of the application where the `Dockerfile` is located and run the following command:

```bash
docker build -t fastapi-app .
```

## Run Docker Container
```bash
docker run -p 8000:80 -d fastapi-app

```
## Access the Application
With the container running, you should be able to access the application at http://localhost:8000.

## Docker Container Management
```bash 
To stop the container, first get the CONTAINER ID or NAMES from the docker ps command, then use it in the following command:

docker stop [CONTAINER_ID_OR_NAME]
```