# cfn-example

This template `vpc.yaml` deploys a VPC, with public and private subnets spread across two or three Availabilty Zones. It deploys an Internet Gateway, with a default route on the public subnets. It deploys NAT Gateways (one in each AZ), and default routes for them in the private subnets.

# sample aws commands

```
# create vpc with 3 AZs.
$ aws cloudformation create-stack --stack-name vpc-dev --template-body file://vpc.yaml --parameters ParameterKey=AZs,ParameterValue=3AZs ParameterKey=EnvironmentName,ParameterValue=development
```

# reference

https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/conditions-section-structure.html

https://github.com/aws-samples/reactive-refarch-cloudformation/blob/master/infrastructure/vpc.yaml

https://github.com/aws-samples/aws-cidr-finder
