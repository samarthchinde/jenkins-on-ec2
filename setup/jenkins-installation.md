# Jenkins Installation

## Add Jenkins repository
sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo
sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io-2023.key

## Install Jenkins
sudo yum install jenkins -y

## Start Jenkins service
sudo systemctl start jenkins

## Enable Jenkins at boot
sudo systemctl enable jenkins

## Check Jenkins status
sudo systemctl status jenkins

## Access Jenkins
http://<PUBLIC_IP>:8080

Jenkins is now running successfully.
