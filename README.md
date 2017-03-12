# AWS Lambda Hello World

## Node.js Setup on Ubuntu


## IAM Deployment User Setup
  - create an IAM user (e.g. lambda-deployer)
  - No console login for lambda-deployer
  - Assign key and secret to lambda-deployer
  - Create inline policy for lambda-deployer:
```bash

  {
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "Stmt1488419922000",
            "Effect": "Allow",
            "Action": [
                "lambda:GetFunction",
                "lambda:UpdateFunctionCode",
                "lambda:UpdateFunctionConfiguration"
            ],
            "Resource": [
                "arn:aws:lambda:*"
            ]
        }
    ]
}

```

## Create an IAM Role for Lambda Execution
*NOTE*:  Only assign the minimum set of permissions needed

E.g. lambda-exec-role

Policy:  AWSLambdaExecute




## Deployment to AWS

```bash

npm run deploy

```
