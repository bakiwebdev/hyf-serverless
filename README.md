# Getting Started with Serverless Application

This guide will help you to get started with building and deploying a serverless application on the AWS platform. Serverless applications allow you to quickly build and deploy an application without having to maintain servers and other infrastructure.

## Prerequisites

- [AWS account](https://aws.amazon.com/)
- [AWS CLI](https://aws.amazon.com/cli/) configured with your AWS credentials -> [or follow this step](https://github.com/bakiwebdev/hyf-serverless/blob/main/aws-cli-configuration.md)
- [Node.js](https://nodejs.org/) and [npm](https://www.npmjs.com/) installed
- [Serverless Framework](https://serverless.com/) [or follow this step](https://github.com/bakiwebdev/hyf-serverless/blob/main/install-serverless-framework.md)


<!-- Step by Step configuring AWS CLI credentials -->

<!-- ## Step 1: Download and Install the AWS CLI

The AWS Command Line Interface (CLI) is a unified tool that allows users to manage AWS services from the command line. This is the first step to using AWS for serverless applications. To get started, go to the AWS CLI page and choose the appropriate version for your system: [AWS CLI Download](https://aws.amazon.com/cli/). -->

<!-- ## Step 2: Create an AWS Account

In order to use AWS for serverless applications, you will need to create an AWS account. To do this, go to [Create an AWS Account](https://portal.aws.amazon.com/billing/signup#/start). Once you have completed the process, you will have access to the AWS Management Console, where you can manage your resources.  -->

<!-- ## Step 3: Configure the AWS CLI

Once you have installed the AWS CLI, you need to configure it with your account credentials. To do this, open a terminal window and enter the command `aws configure`. You will be prompted to enter your AWS access key, secret key, and default region. Once you have completed this process, you will be ready to use the AWS CLI for serverless applications. -->

<!-- ## Step 4: Create an IAM User

In order to deploy an application, you need to create an IAM user with appropriate permissions. To do this, open the AWS Management Console and select IAM from the list of services. Then, select “Users” and click the “Create New User” button. Enter the user name, select the appropriate permissions, and click “Create User”. After the user is created, make note of the access key and secret key, which you will need to configure the AWS CLI. -->

## Step 1: Create a new project

Use the following command to create a new project with the Serverless Framework:

```
serverless create --template aws-nodejs
```

This will create a new project with the basic file structure and configuration for a Node.js application on AWS.

## Step 2: Define your functions

In the serverless.yml file, you can define your serverless functions under the functions property. Each function should have a handler property that specifies the file and exported function to be used as the entry point for the function.

Example:

```
functions:
  hello:
    handler: handler.hello
```

## Step 3: Define your events

Under each function, you can define the events that trigger the function using the events property.

Example:

```
functions:
  hello:
    handler: handler.hello
    events:
      - http:
          path: /
          method: GET
```

This example will create an API Gateway endpoint that will trigger the hello function when a GET request is made to the root path.

## Step 4: Deploy your application

Use the following command to deploy your application to AWS:

```
serverless deploy
```

This will create the necessary resources on AWS and deploy your functions. The command will output the endpoint URLs for your functions.

## Step 5: Test your application

Use the endpoint URLs to test your application and make sure everything is working as expected.
Additional Resources

- [Serverless Framework Docs](https://www.serverless.com/framework/docs/)
- [AWS Lambda Docs](https://aws.amazon.com/lambda/)
- [AWS API Gateway Docs](https://aws.amazon.com/api-gateway/)

> Note: This is a basic example and it's possible that you'll need to add more configurations or resources depending on your specific use case.

Congratulations! You have successfully deployed your serverless application on the AWS platform.
