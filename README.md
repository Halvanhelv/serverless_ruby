# AWS Serverless Workshop - Day 1 Overview

In these projects for the first day of the workshop, the following AWS technologies were utilized:

1. **Project: Basic Webhooks Function**
   - AWS::Serverless::Function (Lambda Function with Ruby runtime and ARM64 architecture)
   - FunctionUrlConfig for Lambda

2. **Project: Webhooks with S3 Integration**
   - AWS::Serverless::Function (Lambda Function with Ruby runtime, ARM64 architecture, and environment variables for S3 integration)
   - AWS::S3::Bucket
   - IAM Policy for S3 PutObject action

3. **Project: Webhooks with SQS and S3 Integration**
   - AWS::Serverless::Function (Two Lambda Functions for handling webhooks and processing SQS messages)
   - AWS::S3::Bucket
   - AWS::SQS::Queue
   - IAM Policies for S3 PutObject and SQS SendMessage actions

4. **Project: Scheduled Lambda Function**
   - AWS::Serverless::Function (Lambda Function with a scheduled event trigger)
   - Schedule event configuration (running every 1 minute)

Each project was constructed with AWS SAM templates, focusing on different aspects of serverless application development and deployment using AWS services.



# AWS Serverless Workshop - Day 2 Overview

For the second day of the workshop, the projects focused on integrating AWS Lambda with Amazon DynamoDB, utilizing various DynamoDB features. Here's a breakdown of the AWS technologies used:

1. **Basic Integration with DynamoDB**
   - AWS::Serverless::SimpleTable (DynamoDB)
   - AWS::Serverless::Function (Lambda with Ruby runtime, ARM64 architecture, and environment variables for DynamoDB integration)
   - DynamoDB IAM Policy for PutItem action
   - Function URL Configuration

2. **DynamoDB with Custom Schema**
   - AWS::DynamoDB::Table (Custom table schema with HASH and RANGE key attributes)
   - AWS::Serverless::Function (Lambda Function integration)
   - IAM Policy for DynamoDB access
   - Function URL Configuration

3. **DynamoDB with Local Secondary Index (LSI)**
   - AWS::DynamoDB::Table (Custom table with LSI)
   - AWS::Serverless::Function (Lambda Function integration)
   - DynamoDB IAM Policy
   - Function URL Configuration

4. **DynamoDB with Global Secondary Index (GSI)**
   - AWS::DynamoDB::Table (Custom table with both LSI and GSI)
   - AWS::Serverless::Function (Lambda Function integration)
   - IAM Policy for DynamoDB access
   - Function URL Configuration

Each of these projects was designed to demonstrate different aspects and capabilities of DynamoDB when integrated with AWS Lambda, providing a practical understanding of DynamoDB's indexing features and Lambda's interaction with DynamoDB.


# AWS Serverless Workshop - Day 3 Overview

The third day of the workshop introduced more advanced AWS serverless configurations, emphasizing on the integration of AWS Lambda with Amazon SQS, and the use of Docker containers in Lambda functions. Here are the key AWS technologies and features utilized in the Day 3 projects:

1. **Advanced AWS Lambda with Amazon SQS**
   - AWS::SQS::Queue (Standard queue configuration with visibility timeout and redrive policy)
   - AWS::SQS::Queue (Dead Letter Queue setup for message retention)
   - AWS::Serverless::Function (Lambda function with custom Docker container, environment variables for stage and SQS queue)
     - Docker container setup for Lambda function
     - Memory configuration and package type set to Image
     - IAM Policies for full SQS access
     - Function URL Configuration with no authentication
   - AutoPublishAlias and DeploymentPreference configurations for Lambda
   - VPC Configuration placeholders (commented out for customization)

2. **Lambda Function for Job Processing with SQS Trigger**
   - AWS::Serverless::Function (Lambda function specifically for job processing, triggered by SQS queue)
     - Dockerfile and Docker context setup
     - Command specification in ImageConfig for the Docker container
     - Memory and Timeout configuration tailored for job processing
     - IAM Policies for SQS access
     - Batch processing configuration for SQS trigger

These projects collectively focus on developing scalable serverless applications with AWS Lambda using containerized environments, and managing asynchronous job processing using SQS. This setup offers a real-world scenario of complex serverless architectures, leveraging the benefits of both Lambda and SQS in a distributed environment.