# SSH Connection to EC2 Instance

This document explains how to connect to an AWS EC2 instance using SSH (Secure Shell). SSH provides secure remote access to the Linux server, which is required for installing Jenkins and performing administrative and configuration tasks.

Prerequisites:
- EC2 instance must be in Running state
- Public IPv4 address or Public DNS should be available
- The key pair (.pem file) used during EC2 launch must be downloaded
- Security Group must allow inbound traffic on port 22 (SSH)
- SSH client should be available (Linux/macOS terminal, Windows PowerShell, or MobaXterm)

Step 1: Get the Public IP Address  
Go to AWS Console → EC2 → Instances → select the instance → copy the Public IPv4 address.

Example:
3.110.xxx.xxx

Step 2: Set Key File Permissions (Linux/macOS)  
To maintain security, SSH requires strict permissions on the private key file.

Command:
chmod 400 jenkins-key.pem

This ensures only the owner can read the key file.

Step 3: Connect to the EC2 Instance Using SSH  
Use the following command from the terminal:

ssh -i jenkins-key.pem ec2-user@<PUBLIC_IP>

Example:
ssh -i jenkins-key.pem ec2-user@3.110.xxx.xxx

For Amazon Linux AMI use:
ec2-user

For Ubuntu AMI use:
ubuntu

Step 4: Verify Successful Connection  
After connecting, the terminal prompt should look similar to:

[ec2-user@ip-172-31-xx-xx ~]$

This confirms that the SSH connection to the EC2 instance is successful.

Common Issues:
- Permission denied (publickey): Check key file, username, and permissions
- Connection timed out: Ensure port 22 is open in Security Group and instance is running

Result:
Secure SSH access to the EC2 instance is established successfully. The server is now ready for Java and Jenkins installation.

