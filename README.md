# Docker container app

This containerised app shows an user account settings screen. User can update their account (name, age, location)

All components are docker-based.

## Table of Contents

1. [Tech Stack](#tech-stack)
1. [Diagram](#diagram)
1. [Dockerfile](#dockerfile)
1. [AWS ECR](#aws-ecr)
1. [To run the application](#to-run-the-application)
1. [To be continued](#to-be-continued)

## Tech Stack

1. HTML/CSS/Javascript
1. Nodejs backend
1. Mongodb and Mongo Express
1. Docker/Docker Hub
1. AWS ECR for custom app image storage

## Diagram

![alt text](https://github.com/mviisan/docker-node-aws/blob/master/diagram.png?raw=true)

## Dockerfile

    docker build -t my-app:1.0 .       

The dot "." at the end of the command denotes location of the Dockerfile in the current directory

## AWS ECR

Now that the image is built, we can upload it to Amazon Elastic Container Registry.
1. Download a set of key id and secret access key from AWS console
1. aws configure (enter the keys and region)
1. docker push 1234567891011.dkr.ecr.eu-west-2.amazonaws.com/my-app:1.0 

## To run the application

1. docker-compose -f docker-compose.yaml up
1. Access http://localhost:3000

## To be continued

Next, run the app image using ECS (Fargate/EC2)
