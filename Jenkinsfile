pipeline {
    agent any
    tools {
        maven 'Maven'
    }
    stages {
        stage ('Build') {
            steps {
                script {
                    echo 'Building Java application'
                    sh 'mvn clean install package'
                }
            }
        }
        stage ('Deploy') {
            steps {
                script {
                    echo 'Deploying applicationn'
                }
            }
        }
    }
}