# Udacity Reviews test project
Project Title: Deploy a high-availability web app using AWS CloudFormation


## Step 1: Deploy Server
Run servers.yml using the following commands:
`aws cloudformation create-stack --stack-name network --template-body file://network.yml --parameters file://network-params.json --capabilities CAPABILITY_IAM`

## Step 2: Bastion server
Run bastion-server.yml with the following commands:
`aws cloudformation create-stack --stack-name bastion-host-server --template-body file://bastion-server.yml --parameters file://bastion-server-params.json --capabilities CAPABILITY_IAM`

## Step 3: Application servers
Run application-servers.yml:
`aws cloudformation create-stack --stack-name application-servers --template-body file://application-servers.yml --parameters file://application-servers-params.json --capabilities CAPABILITY_IAM`

this should be able to deploy the project with the required configs
