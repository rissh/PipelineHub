# Multi-Stage Multi-Agent

Welcome to the Multi-Stage Multi-Agent project! This repository contains a CI/CD pipeline for building polyglot projects, supporting both back-end (Java with Maven) and front-end (JavaScript with Node.js) development.

## Overview

The Multi-Stage Multi-Agent project is designed to automate the build, test, and deployment processes for polyglot projects. It supports projects written in multiple programming languages, such as Java and JavaScript. The pipeline uses Jenkins to orchestrate the CI/CD process and leverages Docker containers as agents to provide an isolated and consistent build environment.

## Jenkins Setup and Pipeline Execution

### Set Up Jenkins

Ensure you have Jenkins installed and running on your server or local machine. Configure Jenkins to work with Docker, allowing it to use Docker containers as agents.

### Create Pipeline Job

In Jenkins, create a new pipeline job and configure it to use the Jenkinsfile(s) provided in this repository.

### Run Pipeline

Trigger the pipeline job in Jenkins. The pipeline will execute the defined stages, which include installing dependencies (if applicable) and printing the Node.js version along with npm version.

## Jenkinsfiles

### Jenkinsfile 1 - Maven 3.8.1 & Node 16

This Jenkinsfile defines a CI/CD pipeline with two stages: "Back-end" and "Front-end". In the "Back-end" stage, Maven 3.8.1 and AdoptOpenJDK 11 Docker image is used as the agent to build and test the back-end component. It prints the Maven version using the 'mvn --version' command. In the "Front-end" stage, Node.js 16 Alpine Docker image is used as the agent to build and test the front-end component. It prints the Node.js version using the 'node --version' command.

### Jenkinsfile 2 - Maven 3.8.3 & Node 16

This Jenkinsfile defines a CI/CD pipeline with two stages: "Back-end" and "Front-end". In the "Back-end" stage, Maven 3.8.3 and AdoptOpenJDK 11 Docker image is used as the agent to build and test the back-end component. It sets a timeout of 15 minutes for the stage and executes Maven commands to clean the project, package the application, and run tests. In the "Front-end" stage, Node.js 16 Alpine Docker image is used as the agent to build and test the front-end component. It sets a timeout of 10 minutes for the stage and executes Node.js commands to install dependencies, build the project, and run tests.
