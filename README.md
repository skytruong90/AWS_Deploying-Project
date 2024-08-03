# AWS Deploying Project

## What is this?
This is a project where I deploy an end-to-end website on AWS from scratch. The project demonstrates the complete process of setting up, configuring, and deploying a fully functional website using various AWS services.

## What does this do?
This project sets up a scalable and secure web application on AWS. It includes:

- Hosting a static website on Amazon S3.
- Setting up a custom domain with Route 53.
- Configuring a backend using AWS Lambda and API Gateway.
- Implementing a relational database using Amazon RDS.
- Setting up user authentication with AWS Cognito.
- Managing infrastructure with AWS CloudFormation.

## Installation
To set up and deploy the website, follow these steps:

1. **Clone the repository**:
   ```bash
   git clone https://github.com/skytruong90/AWS_Deploying-Project.git
   cd AWS_Deploying-Project
   ```
   
2. **Install AWS CLI**:
   - Follow the AWS CLI installation guide to install and configure the AWS CLI.
     
3. **Configure AWS CLI**:
   ```bash
   aws configure
   ```
   - Provide your AWS Access Key ID, Secret Access Key, region, and output format.
  
4. **Deploy CloudFormation Stack**:
   - Navigate to the CloudFormation template directory and deploy the stack.
   ```bash
   aws cloudformation create-stack --stack-name MyWebsiteStack --template-body file://template.yml --capabilities CAPABILITY_NAMED_IAM
   ```

## How To Use
1. Upload Website Files to S3:
   - Navigate to the S3 bucket created by the CloudFormation stack.
   - Upload your static website files (HTML, CSS, JS) to the bucket.
2. Set Up Custom Domain:
   - Use Route 53 to create a hosted zone for your custom domain.
   - Update the domain's DNS settings to point to the S3 bucket.
3. Configure API Gateway and Lambda:
   - Create an API Gateway endpoint and link it to your Lambda functions.
   - Deploy the API to make it accessible over the internet.
4. Set Up Database:
   - Access the Amazon RDS instance created by the CloudFormation stack.
   - Configure your backend to connect to the RDS database.
5. Enable User Authentication:
   - Use AWS Cognito to set up user pools and identity pools.
   - Integrate Cognito authentication into your website.
6. Access Your Website:
   - Visit your custom domain to see the deployed website.
   - Test the backend functionality and user authentication.

## Enjoy your fully deployed and functional website on AWS!
