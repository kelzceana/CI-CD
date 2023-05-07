pipeline {
    agent any
    tools {
        maven 'maven-3.9'
    }
    stages {
        stage ('Build') {
            steps {
                script {
                    echo 'building maven application'
                    sh 'mvn clean install package'
                }
            }
        }
        stage ('Deploy') {
            steps {
                sshagent(['tomcart-server']) {
                    // coping WAR files from jenkins server to tomcat server
                   sh "scp -o StrictHostKeyChecking=no webapp/target/webapp.war ubuntu@ec2-44-202-13-129.compute-1.amazonaws.com:/var/lib/tomcat9/webapps"
                }
            }
        }
    }
}