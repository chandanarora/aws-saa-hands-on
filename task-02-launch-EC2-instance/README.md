Task 02 – EC2 Instance Launch and SSH Access
This task involved launching a virtual EC2 instance using Amazon Linux 2023 and connecting to it securely over SSH using a key pair. The instance was later terminated to avoid ongoing charges.

🎯 Objective
Launch an EC2 instance (Amazon Linux 2023)

Enable SSH access using a key pair

Connect via terminal (SSH or PuTTY)

Terminate instance after verification

🧰 Tools & Services Used
Amazon EC2

Key Pair (.pem file)

Security Group (SSH port 22 open)

SSH terminal / Git Bash / PuTTY

🪜 What I Did
1. Launched EC2 Instance
Service: EC2 → Launch Instance

Name: saa-ec2-instance

AMI: Amazon Linux 2023 (64-bit x86)

Instance Type: t3.micro (Free Tier eligible)

Key Pair: saa-key.pem (downloaded at creation)

Network Settings:

Auto-assign Public IP: ✅ Enabled

Inbound Rule: SSH (Port 22) from My IP

Storage: Default (8 GB gp2)

2. Updated Security Group (If Needed)
Navigated to EC2 → Security Groups

Edited Inbound Rules:

Type: SSH

Source: My IP

Saved changes

3. Connected via SSH
a. Using Git Bash / Linux / macOS Terminal:
ssh -i "saa-key.pem" ec2-user@<EC2_PUBLIC_IP>

b. Using PuTTY on Windows:
Converted .pem to .ppk using PuTTYgen

In PuTTY:

Hostname: ec2-user@<EC2_PUBLIC_IP>

SSH → Auth → Browse to .ppk file

Click Open

4. Ran Test Commands
Once connected to the instance:
uname -a
sudo yum update -y

5. Terminated Instance
Navigated to EC2 → Instances

Selected saa-ec2-instance

Instance State → Terminate

| Action               | Screenshot Preview                      |
| -------------------- | --------------------------------------- |
| EC2 Instance Details | ![EC2 Instance](./screenshots/ec2.png)  |
| Security Group (SSH) | ![Security Group](./screenshots/sg.png) |

🔐 Notes
SSH access was limited to my IP for security.

Instance was terminated after testing to avoid charges.

⏭️ Next Task
Task 03 – S3 Bucket Public Access & Permissions
