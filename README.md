# Infrastructure<br />
<b>Network infrastructure for CSYE6225<br /></b>

Contact Information-<br /> 
Mrinal Sharma<br /> 
NUID-001448287<br /> 
Email- sharma.mr@husky.neu.edu<br /> 

This repository can be used to setup networking resources such as Virtual Private Cloud (VPC), Internet Gateway, Route Table and Routes<br />

Prerequisites for running the aws cli commands<br /> 
You should have AWS Command Line Interface installed and configured for your dev and prod profile<br /> 


An example of create stack command:- <br />
aws cloudformation create-stack   --stack-name csye6225  --parameters ParameterKey=VPCName,ParameterValue=VPCName    ParameterKey=myVPCCIDR,ParameterValue=10.0.0.0/16   ParameterKey=mySubnet1CIDR,ParameterValue=10.0.1.0/24   ParameterKey=mySubnet2CIDR,ParameterValue=10.0.2.0/24   ParameterKey=mySubnet3CIDR,ParameterValue=10.0.3.0/24   --template-body file://networking.json --region us-east-2 --profile dev<br />

Delete stack command:- <br />
aws cloudformation delete-stack --stack-name csye6225demo --region us-east-1 --profile dev<br />