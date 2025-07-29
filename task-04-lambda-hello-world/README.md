# Task 04 – Deploy a Lambda Function (Hello World)

## 🎯 Objective
Create a basic AWS Lambda function using the AWS Management Console that returns a simple message: `"Hello from Lambda!"`

---

## 📍 Steps Performed

### ✅ 1. Access Lambda Console
- Open the AWS Console.
- Go to **Services → Lambda**.
- Click on **Create function**.

---

### ✅ 2. Function Configuration
- **Author from scratch**
  - **Function name**: `lambda-hello-world`
  - **Runtime**: Python 3.12
  - **Architecture**: x86_64
  - **Permissions**: Create a new role with basic Lambda permissions

📸 `lambda-create.png`

---

### ✅ 3. Function Code

Replaced default code with:

```python
def lambda_handler(event, context):
    return {
        'statusCode': 200,
        'body': 'Hello from Lambda!'
    }

✅ 4. Test the Function
Click Deploy to save the changes

Navigate to the Test tab

Created a new test event with default settings

Clicked Test

✅ Output:

{
  "statusCode": 200,
  "body": "Hello from Lambda!"
}

✅ 5. Clean-Up
This Lambda function runs under the free tier.

It can be deleted later via Actions → Delete if needed.

🧠 Notes
Lambda allows running code without provisioning servers.

Ideal for serverless microservices and automation scripts.

This was a basic "Hello World" — future tasks may include API Gateway triggers and S3 events. 

