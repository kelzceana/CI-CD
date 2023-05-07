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
                script {
                    echo 'Deploying application to web server'
                }
            }
        }
    }
}