pipeline {
    agent any

    stages {

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t cicd-app:latest .'
            }
        }

        stage('Deploy to Kubernetes') {
            steps {
                bat 'kubectl apply -f k8s/'
            }
        }
    }
}
