# Task 04 – Deploy a Lambda Function (Hello World)

## 🎯 Objective
Create a basic AWS Lambda function using the AWS Management Console that returns a simple message: `"Hello from Lambda!"`

---

## 📍 Steps Performed

### ✅ 1. Access Lambda Console
- Open the AWS Console
- Navigate to **Services → Lambda**
- Click on **Create function**

---

### ✅ 2. Configure the Function
- **Author from scratch**
  - **Function name**: `lambda-hello-world`
  - **Runtime**: `Python 3.12`
  - **Architecture**: `x86_64`
  - **Permissions**: Create a new role with basic Lambda permissions  
📸 Screenshot: `lambda-create.png`

---

### ✅ 3. Add Function Code

Replaced the default code with:

```python
def lambda_handler(event, context):
    return {
        'statusCode': 200,
        'body': 'Hello from Lambda!'
    }
```

###  📸 Screenshot: lambda-code.png

✅ 4. Test the Function
Click Deploy to save the changes

Switch to the Test tab

Create a new test event (default settings)

Click Test

🖥️ Output:

{
  "statusCode": 200,
  "body": "Hello from Lambda!"
}

### 📸 Screenshot: lambda-test-result.png
### 🧹 5. Clean-Up
This Lambda runs under the free tier

Can be deleted via Actions → Delete if needed

🧠 Notes
AWS Lambda runs code without provisioning or managing servers

Great for building serverless microservices, automation scripts, and event-driven apps

This was a simple "Hello World" function
✅ Future tasks may include API Gateway triggers and S3 events

### 🖼️ Screenshots
🛠️ Lambda Configuration

💻 Function Code

🧪 Test Output
