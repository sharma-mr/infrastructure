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
aws cloudformation create-stack <br />
--stack-name demo <br />
--template-body file://./{fileName}} <br />
--parameters <br />
ParameterKey=appDomainName,ParameterValue={domainName}} <br />
ParameterKey=HostedZoneId,ParameterValue={hostedZoneId} <br />
ParameterKey=s3BucketForCodeDeploy,ParameterValue={s3bucketForCodeDeploy}} <br />
ParameterKey=subnetcidrblock,ParameterValue={subnetCidrBlock}} <br />
ParameterKey=VPCName,ParameterValue={vpcName} <br />
ParameterKey=AWSRegion,ParameterValue={REGION}} <br />
ParameterKey=vpccidrblock,ParameterValue={vpcciderblock}} <br />
ParameterKey=AMI,ParameterValue={ami} <br />
ParameterKey=certificateArn,ParameterValue={certificateArn}} <br />
ParameterKey=keyname,ParameterValue={sshKeyName}} <br />
--capabilities CAPABILITY_NAMED_IAM <br />
--region us-east-1 <br />
--profile prod<br />

Install ssl certificate command:- <br />
aws acm import-certificate --certificate fileb://{certificate}.pem<br />
                                 --certificate-chain fileb://{certificateChain}.pem<br />
                                 --private-key fileb://{privatekey}.pem<br />
                                 --profile {profile}<br />


Delete stack command:- <br />
aws cloudformation delete-stack --stack-name csye6225demo --region us-east-1 --profile dev<br />