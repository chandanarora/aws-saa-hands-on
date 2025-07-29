✅ Task 02: EC2 Instance Launch and SSH Access
📌 Objective
Launch a virtual EC2 instance (Amazon Linux 2023) and connect to it via SSH using a key pair.

🧰 Tools & Services
Amazon EC2

Key pair (.pem)

Security Group (port 22 open)

SSH terminal or PuTTY

🪜 Steps Performed
1. Launch EC2 Instance
Service: EC2 → Launch instance

Name: saa-ec2-instance

AMI: Amazon Linux 2023 (64-bit x86)

Instance type: t3.micro (Free Tier eligible)

Key pair: saa-key.pem (generated and downloaded)

Network settings:

Auto-assign public IP: Enabled

Inbound rule: SSH (port 22) from My IP

Storage: Leave default (8 GB gp2)

Launch


2. Update Security Group (If Needed)
Go to Security Groups

Edit inbound rules:

Type: SSH

Source: My IP

Save changes

📝 Take Screenshot of updated inbound rule.

3. Connect via SSH
Use a terminal (Linux/macOS) or Git Bash on Windows:

ssh -i "saa-key.pem" ec2-user@<EC2_PUBLIC_IP>

Or, with PuTTY:

Convert .pem to .ppk using PuTTYgen

Hostname: ec2-user@<EC2_PUBLIC_IP>

In PuTTY → SSH → Auth → Browse .ppk file

Open session

4. Test Commands (Optional)
Inside your EC2 terminal:
uname -a
sudo yum update -y

5. Terminate Instance
EC2 → Select instance → Instance State → Terminate

Confirm termination
