# NodeVersionChecker

NodeVersionChecker is a CI/CD pipeline project designed to check and print the version of Node.js along with its dependencies using Jenkins.

## Architecture

This project follows a Docker-based architecture, utilizing Docker containers as agents for Jenkins pipelines. Each Jenkins pipeline job runs inside a Docker container with the specified Node.js Alpine image, ensuring consistency and isolation.
