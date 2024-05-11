# Hosting a Static Website on AWS using Terraform

This Terraform configuration sets up the necessary infrastructure to host a static website on AWS. It includes the following files:

- main.tf: Defines the AWS resources to be created, such as an S3 bucket, CloudFront distribution, and Route 53 record.

- providers.tf: Specifies the AWS provider and its version.

- variables.tf: Defines the input variables for the Terraform configuration. [2]

- outputs.tf: Defines the output values that will be returned after the Terraform deployment.

## Prerequisites
Before you begin, make sure you have the following:

- AWS Account: You'll need an AWS account with the necessary permissions to create the required resources.

- Terraform: Ensure you have Terraform installed on your local machine. You can download it from the official Terraform website.

- AWS CLI: Install the AWS CLI on your local machine to interact with your AWS account. You can download it from the official AWS CLI website.

- Domain Name: You'll need a domain name that you own or have access to, which will be used for your static website.

## Getting Started
- Clone the repository: Clone the repository containing the Terraform configuration files to your local machine.

- Configure AWS credentials: Set up your AWS credentials by either:

- Configuring the 
AWS_ACCESS_KEY_ID
 and 
AWS_SECRET_ACCESS_KEY
 environment variables.

Creating an AWS profile in your 
~/.aws/credentials
 file.

- Customize the Terraform configuration:

Open the variables.tf file and update the following variables:

- domain_name: The domain name you want to use for your static website.

- bucket_name: The name of the S3 bucket that will host your website files.

- index_document: The name of the index document for your website (e.g., 
index.html
).

- error_document: The name of the error document for your website (e.g., 
error.html
).

- Initialize Terraform: In the project directory, run the following command to initialize Terraform:

`terraform init`
`Plan the deployment`: Run the following command to see the changes that Terraform will make to your AWS infrastructure:

`terraform plan`
`Apply the changes`: If you're satisfied with the plan, apply the changes by running:

`terraform apply`

Terraform will now create the necessary resources, including the S3 bucket, CloudFront distribution, and Route 53 record.
Upload your website files: After the deployment is complete, upload your static website files to the S3 bucket created by Terraform.

Verify the website: Once the files are uploaded, you can access your website using the CloudFront distribution URL or the Route 53 domain name.

Outputs
After the Terraform deployment, you'll see the following output values:

- website_bucket_name: The name of the S3 bucket that hosts your website files.

- cloudfront_domain_name: The domain name of the CloudFront distribution.

- website_url: The URL of your static website.

## Cleanup
To destroy the resources created by Terraform, run the following command:

`terraform destroy`

