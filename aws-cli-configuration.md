# Setting up AWS CLI Configuration

## Prerequisites

- [AWS account](https://aws.amazon.com/)
- [AWS CLI](https://aws.amazon.com/cli/) installed on your local machine

# Step 1: Install AWS CLI

[Download and run](https://awscli.amazonaws.com/AWSCLIV2.msi) the AWS CLI MSI installer for Windows (64-bit):

> To confirm the installation, open the Start menu, search for cmd to open a command prompt window, and at the command prompt use the `aws --version` command. 

## Step 2: Configure the AWS CLI

Use the following command to configure the AWS CLI with your AWS credentials:

```
aws configure
```

You will be prompted for the following information:

- AWS Access Key ID: This is the access key for your IAM user.
- AWS Secret Access Key: This is the secret key for your IAM user.
- Default region name: The region where you want to create your resources.
- Default output format: The format in which you want the AWS CLI to return output. (optional)

## Step 3: Verify your configuration

Use the following command to verify that your configuration is working as expected:

```
aws s3 ls
```

This command will list all the S3 buckets in your account. If the configuration is successful, you should see a list of your S3 buckets.

Additional Resources

- [AWS CLI Docs](https://docs.aws.amazon.com/cli/index.html)
- [IAM User Guide](https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html)

> Please note that these are basic instructions for setting up AWS CLI configuration. Additional configuration and security measures may be necessary depending on your specific use case.
