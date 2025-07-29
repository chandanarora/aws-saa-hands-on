# Task 03 – S3 Public Access (AWS SAA Hands-on)

## 🎯 Objective:
Upload a text file to an S3 bucket and make it publicly accessible via a web browser.

---

## 📌 Steps Performed:

### ✅ 1. Create S3 Bucket
- Bucket Name: `saa-s3-task-chandan`
- Region: `us-east-1` (N. Virginia)
- Block Public Access: **Uncheck** “Block all public access”
- Saved screenshot: `bucket-creation.png`

---

### ✅ 2. Upload a File
- File uploaded: `hello.txt`
- File content: `Hello from AWS SAA Prep!`
- Screenshot: `file-upload.png`

---

### ❌ 3. Attempted ACL Access (Fails due to Bucket Owner Enforced)
- Bucket has **Object Ownership** set to "Bucket owner enforced"
- ACL-based public access not allowed
- Screenshot: `bucket-policy.png`

---

### ✅ 4. Applied Bucket Policy to Allow Public Read Access
**Policy Used:**
```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicRead",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::saa-s3-task-chandan/*"
    }
  ]
}

Applied via Permissions → Bucket Policy

Confirmed changes with screenshot: bucket-policy.png

✅ 5. Verified Public Access
Opened file URL:
http://saa-s3-task-chandan.s3.amazonaws.com/hello.txt

Successfully viewed contents in browser

Screenshot: text-file-public-access.png

task-03-s3-public-access/
│
├── bucket-creation.png
├── bucket-policy.png
├── file-upload.png
├── text-file-public-access.png
└── hello.txt

✅ Outcome:
S3 file successfully made public using Bucket Policy, not ACL.

🔐 Security Tip:
Don't allow public access unless required. This task is for learning purposes only.

