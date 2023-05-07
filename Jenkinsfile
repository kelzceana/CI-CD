pipeline {
    agent any
    tools {
        maven 'Maven'
    }
    stages {
        stage ('Build') {
            steps {
                script {
                    echo 'Build stage'
                    echo 'Building Java application'
                    sh 'mvn clean install package'
                }
            }
        }
        stage ('Deploy') {
            steps {
                sshagent(['webapp']) {
                    // copying build artifact to tomcat server
                    sh 'scp StrictHostKeyChecking=no webapp/target/webapp.war ubuntu@ec2-44-206-250-102.compute-1.amazonaws.com:/var/lib/tomcat9/webapps'
                }
            }
        }
    }
}