#!/bin/bash

# Update package index
sudo yum update -y

# Install Docker
sudo yum install docker -y

# Start Docker service
sudo systemctl start docker

# Enable Docker service to start on boot
sudo systemctl enable docker

# Verify Docker installation
docker --version




git clone https://github.com/prasunasharma/php-hello-world.git

# Use a base image that includes a web server (nginx, apache, etc.)
FROM nginx:latest

# Copy the application files into the container
COPY . /usr/share/nginx/html

# Expose port 80 to the outside world
EXPOSE 80

cd php-hello-world
docker build -t php-hello-world .

Sudo docker tag php-hello-world prasunamudawari/php-hello-world
Sudo docker login

Sudo docker push prasunamudawari/php-hello-world



instructions for setting up Docker, building a Docker image, and pushing it to a GitHub repository


Step 1: Install Docker

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
sudo apt-get update

sudo apt-get install -y docker-ce docker-ce-cli containerd.io docker-compose 
Sudo docker run hello-world(to test docker)

Step 2: Build and Push Docker Image
git clone https://github.com/silarhi/php-hello-world.git



cd php-hello-world/

docker build -t my-php-hello-world .


docker tag my-php-hello-world prasunamudawari/php-hello-world

docker login

docker push prasunamudawari/php-hello-world

Step 3: Push Dockerfile and Docker Compose YAML to GitHub
git init
git remote add origin https://github.com/prasunasharma/intuji-devops-internship-challenge

git add .

git commit -m "Add Dockerfile and Docker Compose YAML"


git push -u origin main



Jenkins Setup Guide


 Installation


1. Update the package index:
    
    sudo apt update
    

   

2. Install OpenJDK 11, which is required to run Jenkins:
   
    sudo apt install openjdk-11-jdk
 

3. Verify the Java installation by checking its version:
   
    java --version


4. Add the Jenkins repository key to the system:
   
    curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key | sudo tee /usr/share/keyrings/jenkins-keyring.asc > /dev/null
   

5. Add the Jenkins repository to the system's list of package sources:
   
    echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] https://pkg.jenkins.io/debian-stable binary/ | sudo tee /etc/apt/sources.list.d/jenkins.list > /dev/null
  

6. Update the package index again to include the Jenkins repository:
    
    sudo apt update
   

7. Install Jenkins using apt:
 
    sudo apt install jenkins
  
Usage

Once Jenkins is installed, you can start, stop, and check its status using systemctl:

9.To start Jenkins:

    sudo systemctl start jenkins

10.To check Jenkins status

    sudo systemctl status jenkins










