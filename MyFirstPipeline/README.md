# NodeVersionChecker

NodeVersionChecker is a CI/CD pipeline project designed to check and print the version of Node.js along with its dependencies using Jenkins.

## Architecture

This project follows a Docker-based architecture, utilizing Docker containers as agents for Jenkins pipelines. Each Jenkins pipeline job runs inside a Docker container with the specified Node.js Alpine image, ensuring consistency and isolation.

## Jenkins Setup and Pipeline Execution

### Set Up Jenkins

Ensure you have Jenkins installed and running on your server or local machine. Configure Jenkins to work with Docker, allowing it to use Docker containers as agents.

### Create Pipeline Job

In Jenkins, create a new pipeline job and configure it to use the Jenkinsfile(s) provided in this repository.

### Run Pipeline

Trigger the pipeline job in Jenkins. The pipeline will execute the defined stages, which include installing dependencies (if applicable) and printing the Node.js version along with npm version.

## Jenkinsfiles

### Original Jenkinsfile

The Jenkinsfile contains the original pipeline configuration that prints the version of Node.js.

### Modified Jenkinsfile

The ModifiedJenkinsfile includes an additional stage to install Node.js dependencies before printing the Node.js version.
