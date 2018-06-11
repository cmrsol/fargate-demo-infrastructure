## Fargate Demo Infrastructure:
This repo contains three CloudFormation stacks and needed configuration files.
The stacks include:
* ```vpc/admin``` - a CloudFormation stack to create a central VPC for an AWS account.
* ```vpc/work``` - a CloudFormation stack to create an application VPC for an AWS account. This VPC is peered to the admin VPC.
* ```iam/fargateDemo``` - a CloudFormation stack to create an IAM role for a demo of the AWS ECS Fargate service.

## Build the Stacks How-To:
**Build the Admin VPC:**
```
# Make and activate a python virtual environment
virtualenv fargate-demo-infrastructure
. fargate-demo-infrastructure/bin/activate
pip install -Ur requirements.txt
cd vpc/admin
stackility upsert -i config/east-1.ini
```


**Build the Application VPC:**
```
# Make and activate a python virtual environment iff needed
virtualenv fargate-demo-infrastructure
. fargate-demo-infrastructure/bin/activate
pip install -Ur requirements.txt
cd vpc/work
stackility upsert -i config/east-1.ini
```


**Build the IAM Role for the Fargate Demo:**
```
# Make and activate a python virtual environment iff needed
virtualenv fargate-demo-infrastructure
. fargate-demo-infrastructure/bin/activate
pip install -Ur requirements.txt
cd iam/fargateDemo
stackility upsert -i config.ini
```
