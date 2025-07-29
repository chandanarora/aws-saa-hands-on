Task 05 – AWS Lambda Triggered by S3
📌 Goal
Invoke a Lambda function automatically when a file is uploaded to an Amazon S3 bucket.

✅ Steps Performed
1. Create an S3 Bucket
Bucket name: saa-s3-trigger-chandan (or similar)

Region: us-east-1

Created a folder named input inside the bucket (optional)

📸 bucket-setup.PNG

2. Create the Lambda Function
Function name: s3-trigger-lambda

Runtime: Python 3.12

Architecture: x86_64

IAM Role with:

AWSLambdaBasicExecutionRole

AmazonS3ReadOnlyAccess (optional)

📸 lambda-create.PNG

3. Add Lambda Code
def lambda_handler(event, context):
    print("Lambda triggered by S3 upload event")
    print(event)
    return {
        'statusCode': 200,
        'body': 'Success'
    }

📸 lambda-code.PNG

4. Add S3 Trigger to Lambda
Triggered by PUT event

Prefix: input/

Acknowledged recursive warning

📸 trigger.PNG

5. Upload Test File
Uploaded input.txt to the input/ folder in the S3 bucket

Lambda triggered automatically

📸 test-upload.PNG

6. Verify in CloudWatch Logs
Lambda was invoked

Event details were printed

Duration and memory usage shown

📸 lam bda-logs.PNG

📚 Learnings
Lambda can automatically respond to S3 events

Avoid recursive triggers — don’t write to the same path that triggers the function

CloudWatch is essential for visibility and debugging

✅ Status
Task completed successfully. Lambda trigger from S3 upload verified.
