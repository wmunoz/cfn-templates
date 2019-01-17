# cfn-templates
Created to store simple AWS cloudformation templates
Each stack has a parameters file asociated. At the moment, aws-cli only supports json for this file. See https://github.com/aws/aws-cli/issues/2275

# Create stack
```
aws cloudformation create-stack --profile default --stack-name simple-ec2 --template-body file://simple-ec2.yml --region us-west-1 --capabilities CAPABILITY_IAM --parameters file:///simple-ec2-parameters.json
```
# Delete stack
```
aws cloudformation delete-stack --profile default --stack-name simple-ec2
```

#Useful Links:

https://aws.amazon.com/blogs/devops/passing-parameters-to-cloudformation-stacks-with-the-aws-cli-and-powershell/
https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-sub.html