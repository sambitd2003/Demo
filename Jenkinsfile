pipeline {
    agent any

    stages {
        stage('Development') {
            steps {
                git 'https://github.com/AdminTurnedDevOps/go-webapp-sample.git'
                // bat 'go test ./...'
            }
        }

        stage('Building our image') {
            steps {
                script {
                    app = docker.build("adminturneddevops/go-webapp-sample")
                }
            }
        }
    }
}