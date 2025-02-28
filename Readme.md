#  Java Application Deploy by Pipeline

	Login as Root User
	sudo su -
	apt-get update && apt-get upgrade
	
	Go to Home Location
	cd /home/ubuntu/
	
# Repository	For This Project
	https://github.com/praveen1994dec/Java_app_3.0.git
	
### Prerequisites Tools  And these are the command which are run on Main instance
		Lunch 2 Instances of t2.medium size
		Connect them and update those server 
		sudo apt-get update
		java --version
		apt install openjdk-17-jre-headless 
		cd /home/ubuntu/
		Clone the Repository
		git clone https://github.com/praveen1994dec/Java_app_3.0.git

# Install Java Version 17
	cd /home/ubuntu/
	java --version
	apt install openjdk-17-jre-headless 

# Install	Jenkins
	sudo wget -O /usr/share/keyrings/jenkins-keyring.asc \
	https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key
	echo "deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc]" \
	https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
	/etc/apt/sources.list.d/jenkins.list > /dev/null
	sudo apt-get update
	sudo apt-get install jenkins

	sudo systemctl enable jenkins 
	sudo systemctl start jenkins 
	sudo systemctl status jenkins 

# Installing Docker into VM
		sudo apt update -y
		sudo apt install apt-transport-https ca-certificates curl software-properties-common -y
		curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
		sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable" -y
		sudo apt update -y
		apt-cache policy docker-ce -y
		sudo apt install docker-ce -y
		
#### sudo systemctl status docker
		sudo chmod 777 /var/run/docker.sock
		
# Install Maven 
		sudo apt update -y
		sudo apt install maven -y
		mvn -version

# Install Trivy
		sudo apt-get install wget apt-transport-https gnupg lsb-release
		wget -qO - https://aquasecurity.github.io/trivy-repo/deb/public.key | sudo apt-key add -
		echo deb https://aquasecurity.github.io/trivy-repo/deb $(lsb_release -sc) main | sudo tee -a /etc/apt/sources.list.d/trivy.list
		sudo apt-get update
		sudo apt-get install trivy


----> Download Sonarcube in Docker Container
		>  docker run -d --name sonarqube -p 9000:9000 -p 9092:9092 sonarqube
   
#### Login Jenkins  && Login Sonarcube respectively
		and Generate Token for jenkins from Sonarcube

### Plugins Install On Jenkins From Root User For This Project
	1.	Artifactory
    2.  Maven Integration
    3.  Pipeline Maven Integration 
    4   Pipeline Maven Plugin API
    5.  Pipeline: Stage View
    6.  Generic WebHook Trigger
    7.  Loding Plugin extensions
    8.  Quality Gates
    9.  Gerrit Trigger
    10. sonar Gerrit
    11. JFrog
    12. Coverage
    13. Code Coverage
    14. SonarQube Generic Coverage
    15. Eclipse Temurin Installer
    16. OWASP-Dependancy Check
    17. SonarQube Scanner
    18. Email Extension
    19. Pipeline 
    20. GitHub
    21. 
	
# History

    cd /home/ubuntu/
    ls
    git clone https://github.com/praveen1994dec/Java_app_3.0.git
    ls
    sudo  apt update -y
    sudo apt install apt-transport-https ca-certificates curl software-properties-common -y
    curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
    sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable" -y
    sudo apt update -y
    apt-cache policy docker-ce -y
    sudo apt install docker-ce -y
    #sudo systemctl status docker
    sudo chmod 777 /var/run/docker.sock

   






