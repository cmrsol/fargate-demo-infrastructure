## Fargate Demo Infrastructure:
This repo contains three CloudFormation stacks and needed configuration files.
The stacks include:
* ```vpc/admin``` - a CloudFormation stack to create a central VPC for an AWS account.
* ```vpc/work``` - a CloudFormation stack to create an application VPC for an AWS account. This VPC is peered to the admin VPC.
* ```iam/fargateDemo``` - a CloudFormation stack to create an IAM role for a demo of the AWS ECS Fargate service.

## Build the Stacks How-To:
