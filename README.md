# Terraform + AWS Lambda example

Using Terraform to manage AWS Lambda functions .

1. A Cloudwatch Event Rule configured to run at 1am every day. The Lamdba 
function is the target of that rule, and the target call has two input parameters: bucket and file_path.

2. The Lambda function that gets the S3 coordonates of the file from the input and checks if the file exists. 
The function needs to have read permissions for all the S3 buckets we want it to check.

Use Cases:
The example I’ll use for this post is a super simple python script that checks if a file exists on S3. 
If the file is there,the function returns true,if it’s not,it returns false.Also,I want this script to run once a day,every day at 1am. 
What the code does is not the important thing here, really. All we care about is how you automate the whole thing.
