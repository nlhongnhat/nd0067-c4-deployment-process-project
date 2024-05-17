# Infrastructure Description

## Overview

This document provides a high-level overview of the infrastructure used to deploy the Udagram application, a full-stack application consisting of a frontend and a backend, leveraging various AWS services for hosting, management, and monitoring.

## Architecture Diagram

![Architecture Diagram of Infra](./Architecture%20Diagram%20of%20Infra.png)

## Components

### User

Description: End-users accessing the application via a web browser.

### AWS CloudFront

Description: A content delivery network (CDN) service that distributes content from AWS S3 to users with low latency and high transfer speeds.
Role: Distributes the frontend static files globally to ensure fast content delivery.

### AWS S3

Description: Amazon Simple Storage Service (S3) is an object storage service that provides scalable storage for data and static files.
Role: Hosts the static frontend files of the application.

### AWS Elastic Beanstalk

Description: AWS Elastic Beanstalk is an easy-to-use service for deploying and scaling web applications and services.
Role: Hosts and manages the backend application, automatically handling the deployment, from capacity provisioning, load balancing, and auto-scaling to application health monitoring.

### Amazon RDS

Description: Amazon Relational Database Service (RDS) makes it easy to set up, operate, and scale a relational database in the cloud.
Role: Provides a managed PostgreSQL database service for storing application data.

### CircleCI

Description: A continuous integration and continuous deployment (CI/CD) platform that automates the software development process.
Role: Manages the CI/CD pipeline, automating the deployment of the frontend to AWS S3 and the backend to AWS Elastic Beanstalk.

## Data Flow

### User Interaction:

* Users interact with the application via a web browser.
* Requests are routed through AWS CloudFront.

### Content Delivery:

* AWS CloudFront fetches static content from AWS S3 and delivers it to users with low latency.
* Dynamic requests are forwarded to AWS Elastic Beanstalk.

### Backend Processing:

* AWS Elastic Beanstalk hosts the backend application.
* The backend processes the requests and interacts with Amazon RDS for database operations.

### CI/CD Pipeline: 

* CircleCI automates the deployment process:
* Frontend files are deployed to AWS S3.
* Backend application is deployed to AWS Elastic Beanstalk.

## Conclusion

This document provides a comprehensive overview of the infrastructure used to deploy the Udagram application. The architecture leverages various AWS services to ensure scalability, reliability, and high performance, with automated deployment and monitoring to maintain the application's health and performance.
