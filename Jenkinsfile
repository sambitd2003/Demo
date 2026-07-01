pipeline {
    agent any

    stages {
        stage('Development') {
            steps {
                git 'https://github.com/AdminTurnedDevOps/go-webapp-sample.git'
                // bat 'go test ./...'
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    docker.build("my-app:latest")
                    // app = docker.build("adminturneddevops/go-webapp-sample")
                }
            }
        }
    }
}