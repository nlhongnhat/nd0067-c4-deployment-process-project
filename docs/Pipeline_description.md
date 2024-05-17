# Pipeline Overview Description

## Developer:

Description: Writes code and pushes changes to the source code repository (e.g., GitHub).

## CircleCI:

* Description: CI/CD platform that automates the build, test, and deployment processes.
* Steps:
  * Checkout Code: CircleCI checks out the code from the repository.
  * Install Dependencies: Installs necessary dependencies for both frontend and backend.
  * Run Tests: Executes tests to ensure code quality and functionality.
  * Build Frontend: Builds the frontend static files.
  * Build Backend: Builds the backend application.
  * Deploy Frontend to S3: Deploys the built frontend files to AWS S3.
  * Deploy Backend to Elastic Beanstalk: Deploys the built backend application to AWS Elastic Beanstalk.

## AWS S3:

* Description: Stores the frontend static files.
* Delivery: Frontend files are delivered to users via AWS CloudFront.

## AWS Elastic Beanstalk:

* Description: Hosts and manages the backend application.
* Deployment: Backend application is deployed and managed here.