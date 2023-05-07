# maven-project

This maven project wrritten by ValaxyTech will be deployed to an Tomcat server from a jenkins pipeline

#Technologiesused:
<br>
AWS, Jenkins, Docker, Ubuntu, Git, Java, Maven, Tomcat
 
# Setup
Jenkins is installed as a Docker container on the AWS server
<br>
Tomcart server is installed on ubuntu OS
<br>
The build artifcat from the build stage in the pipeline is copied to the tomcat server using the ssh agent plugin on jenkins
<br>
Configured security group on EC2 Instance to allow access to web application
