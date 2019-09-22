The zip contains an aws lambda function that does some operations and uploads Market Identifier Codes(MICs) list by country code as a json file to an S3 bucket.

# Setup/Execution
1. Create an AWS bucket named "mics-bucket".
2. Create an AWS lambda function and upload this zip into it.
  a. Make sure the runtime is "Python3.6" and handler name is "lambda_function.lambda_handler".
  b. Increase the timeout in function configuration from the default 3sec to 30sec.
3. Give the function full access to S3.
  a. Create an IAM role and chose Lambda as the service using this role.
  b. Choose AmazonS3FullAccess policy.
  c. Assign role name and save.
  d. Go to the lambda function configuration now and select this newly created role in Execution Role.
4. Trigger the function manually by creating a test event and clicking "Test".
