# jenkins-installation

## Installation on Centos7

### Prerequisite 

##### Java
yum install java-1.8.0-openjdk.x86_64 -y

##### Once the installation is completed , Issue the below command , To check the Java version Installed on the system.
java -version

### Jenkins
Now Lets go ahead and Install Jenkins on Centos 7.

##### Installing Jenkins
The default repository of the System will have the outdated version of Jenkins.
To install the latest version of Jenkins with the latest features and fixes , We are going to add the latest Jenkins repository to the server.

##### Adding the key and the Jenkins repository to the system using the below commands.
sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo
sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io.key

##### Install the jenkins package using the below command.
yum install jenkins

##### Once the Jenkins is successfully installed on the server , Start the Jenkins service using the below command.
sudo systemctl start jenkins

##### To check the status of the Jenkins ,Use the below command,
sudo systemctl status jenkins

##### To start the jenkins service automatically on system boot , Enable the Jenkins service using the below command.
sudo systemctl enable jenkins
