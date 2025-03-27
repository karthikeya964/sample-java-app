pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                withCredentials([usernamePassword(credentialsId: 'Github', usernameVariable: 'GIT_USERNAME', passwordVariable: 'GIT_PASSWORD')]) {
                    sh 'git clone https://${GIT_USERNAME}:${GIT_PASSWORD}@github.com/karthikeya964/sample-java-app.git'
                }
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }
}
