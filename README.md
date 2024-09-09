# Runbook for AWS Infrastructure Management with Terraform

## Overview
This runbook outlines the steps for managing the AWS infrastructure using Terraform. The infrastructure includes a VPC, EC2 instances, an EKS cluster, and other related resources.

## Prerequisites

### 1. Clone the Repository
Ensure the repository containing the Terraform configurations is cloned to your local machine.

```bash
git clone https://github.com/your-repo/infra-repo.git
cd infra-repo 
```

### 2. Install Required Tools
Ensure you have the following tools installed:
Terraform: Install from Terraform's official site.
AWS CLI: Install and configure the AWS CLI with appropriate credentials.
kubectl: For managing EKS clusters.

## Terraform Commands

### 1. Initialize Terraform
Before running any Terraform command, ensure that the project is properly initialized. This step will download necessary providers and set up the workspace.

```bash
terraform init
```


### 2. Plan the Infrastructure
The terraform plan command is used to preview the changes that will be made. This is especially helpful for reviewing any updates to the infrastructure before applying them.

``` bash
terraform plan -var-file=vpc-jenkins-01.tfvars
```


### 3. Apply the Terraform Configuration
Once you're ready to apply the changes, use the following command. It will provision the resources in AWS as defined in the configuration.

```bash
terraform apply -var-file=vpc-jenkins-01.tfvars
```



### 4. Verifying the Deployment
After applying the Terraform configurations, you can verify the deployed resources:
VPC: Check if the VPC is created with appropriate subnets.
EC2 Instances: Verify that EC2 instances are running in the right subnets and using the correct instance types.

### 5. Destroy the Infrastructure
When you no longer need the resources, you can destroy the infrastructure with the following command:

``` bash
terraform destroy -var-file=vpc-jenkins-01.tfvars
```









