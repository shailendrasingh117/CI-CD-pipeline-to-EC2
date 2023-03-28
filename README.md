# CI-CD-pipeline-to-EC2
This project sets up a Continuous Integration and Continuous Deployment (CI/CD) pipeline to deploy code from a GitHub repository to an EC2 instance. <br>The pipeline uses AWS CodeBuild to build the code and create a Docker image, and AWS CodeDeploy to deploy the image to the EC2 instance.
# Prerequisites
Before you begin, you will need the following:

An AWS account with permissions to create EC2 instances, CodeBuild projects, and CodeDeploy applications.
A GitHub repository containing your code.
# Configuration Steps
1. Configure your EC2 instance

 Configure your EC2 instance with the necessary dependencies and services such as Node.js, Docker, and AWS CLI.<br> Make sure to also create an IAM role with permissions to pull the Docker image from the ECR repository and access the S3 bucket.

2. Create a CodeBuild project

 Create a CodeBuild project in AWS that will build your code and create a Docker image.<br> Set up the buildspec.yml file to define the build steps,<br> including building and pushing the Docker image to Amazon ECR.

3. Create a CodeDeploy application and deployment group

 Create a CodeDeploy application and deployment group to deploy the Docker image to your EC2 instance.<br> Set up the appspec.yml file to define the deployment steps, including pulling and running the Docker image from Amazon ECR.

4. Configure a webhook in GitHub

 Set up a webhook in GitHub that triggers your CodeBuild project when code changes are pushed to the repository.

# Usage
Once the pipeline is set up, any changes pushed to the GitHub repository will trigger the CodeBuild project, which will build the code and create a new Docker image. CodeDeploy will then automatically deploy the new image to the EC2 instance.

# Conclusion
By automating the build and deployment process with a CI/CD pipeline, developers can save time and reduce errors that may occur during manual deployments. This allows for faster and more reliable deployment of changes to the application.
