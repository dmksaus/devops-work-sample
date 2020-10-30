# CI/CD Pipeline
This repo have simple node js app shows 'Hello World!' as response. Dockerfile is available to build and run the app as Docker container. Jenkins pipeline is available for CI/CD configuration.

## CI/CD Pipeline
The pipeline is built on Jenkins and have the below steps,
* Test
    * Unit Test using Mocha
    * Static code analysis using ESLint
    * Code Coverage using nyc
* Build
    * Docker image will be build based on Dockerfile using latest node as base image
    * Built image artifact will be copverted to tar and will be saved in ~/jenkins/artifact-repository folder
* Deploy
    * Artifact from the previous step will be exploed in ~/jenkins/deployment folder.

## Jenkins Plugin Required
Apart from the default plugins, below plugins are required to run the pipeline.
* Copy Artifact Plugin
* Docker Pipeline    
* Docker plugin


