# lambda-deploy-test
Deploy a lambda
Following this documentation:
http://docs.aws.amazon.com/es_es/lambda/latest/dg/serverless-deploy-wt.html

1. Package the app
$ aws cloudformation package --template-file example.yaml --output-template-file serverless-output.yaml --s3-bucket ctomas-test

2. Deploy to a stack:
$ aws cloudformation deploy --template-file /Users/Carlos/lambda-deploy-test/serverless-output.yaml --stack-name ctomas-test --capabilities CAPABILITY_IAM
