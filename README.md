creating Cloud formation with VS code

below are the steps to follow and the command you can use 
always make sure you have the following properties but in place. see example below

AWSTemplateFormatVersion: "2010-09-09"
Description: "My cloud formation Template"
Resources:
    MyBucket:
        Type: AWS::S3::Bucket
        Properties:
            BucketName: lizybucket (note bucket names cannot be in Capital Letters if not you will have a roll back)
            Accesscontrol: Private/Public

on your Terminal Run the following command 

1. to create a stack use 
aws cloudformation deploy --template-file s3-template.yaml --stack-name ngoh1stack

2. To describe the stack use
aws cloudformation describe-stacks --stack-name ngoh1stack

3. To update the stack use
aws cloudformation update --template-file s3-template.yaml --stack-name ngoh1stack

4. To delete your stack use
aws cloudformation delete-stack --stack-name ngoh1stack


![cloudformation ](https://user-images.githubusercontent.com/116527791/233254804-f151432d-80a8-463b-a0f3-ebf365b8827e.jpg)

this discribe the image of the stack i created


![s3 bucket](https://user-images.githubusercontent.com/116527791/233255032-e0b1fc66-ce6d-44da-a214-4507ec97aa29.jpg)

this discribe the bucket i created 
