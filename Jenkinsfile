pipeline {
    agent any
    
    stages {
        stage('Cleanup') {
            steps {
                cleanWs()  // Deletes the workspace
            }
        }
        
        stage('Checkout') {
            steps {
                git 'https://github.com/karthikeya964/sample-java-app.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
    }
}
