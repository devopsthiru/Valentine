# Valentine-Devops-Project

Git token - 9/8/24
==================
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

Trivy Install
=============
sudo apt-get install wget apt-transport-https gnupg lsb-release
wget -qO - https://aquasecurity.github.io/trivy-repo/deb/public.key | sudo apt-key add -
echo deb https://aquasecurity.github.io/trivy-repo/deb $(lsb_release -sc) main | sudo tee -a /etc/apt/sources.list.d/trivy.list
sudo apt-get update
sudo apt-get install trivy


Jenkins Install
===============

sudo wget -O /usr/share/keyrings/jenkins-keyring.asc \
  https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key
echo "deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc]" \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install jenkins


Docker Install
==============

# Add Docker's official GPG key:
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update


sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin


Open Jenkins
==========
    	>> apt update 
    	>> setup Ctl script
    	>> aws configure
	>> Install eks

	>> java install (jre 17)
	>> Jenkins install and setup
	>> Install docker from official site
	>> sudo chmod 666 /var/run/docker.sock

Sonar Setup
==========
	>> sudo apt update
	>> install docker from official site
	>> sudo chmod 666 /var/run/docker.sock
	>> docker run -d — name sonar -p 9090:9090 sonarqube:its-community
	>> open browser with port
Nexus Setup
==========
	>> sudo apt update
	>> install docker from official site
	>> sudo chmod 666 /var/run/docker.sock
	>> docker run -d —name nexus3 -p 8081:8081 sone/type:nexus3:latest
	>> setup nexus in browser



