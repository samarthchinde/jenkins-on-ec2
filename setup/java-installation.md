# Java Installation on EC2

Jenkins requires Java to run.

## Update system packages
sudo yum update -y

## Install Java (Amazon Linux)
sudo yum install java-11-amazon-corretto -y

## Install Java (Ubuntu)
sudo apt update -y
sudo apt install openjdk-11-jdk -y

## Verify Java installation
java -version

Java is now successfully installed on the EC2 instance.
