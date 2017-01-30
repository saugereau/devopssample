# devopssample
Exemple of infrastructure as code with cloudformation and ECR cluster



## Copy all files to s3 bucket
aws s3 cp infra s3://devops-sample-201701/ --recursive --exclude "*" --include "*.yml"

## How to validate cloudformation template
aws cloudformation validate-template --template-body file:///Users/augereau/Ekino/Conf/Epitech/DevOps-Sample/infra/multifile/DevopsSample.yml
## How to create a stack
aws cloudformation create-stack --stack-name myteststack --capabilities CAPABILITY_NAMED_IAM --template-body file:///Users/augereau/Ekino/Conf/Epitech/DevOps-Sample/infra/multifile/DevopsSample.yml
## How to update the stack
aws cloudformation update-stack --stack-name myteststack --template-body file:///Users/augereau/Ekino/Conf/Epitech/DevOps-Sample/infra/multifile/DevopsSample.yml
