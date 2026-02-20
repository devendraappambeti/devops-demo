pipeline {
    agent any
    
    stages {
        stage('Build Docker Image') {
            steps {
                bat 'docker build -t devops-app .'
            }
        }
        
        stage('Deploy to Kubernetes') {
            steps {
                bat 'kubectl apply -f k8s/deployment.yaml'
                bat 'kubectl apply -f k8s/service.yaml'
            }
        }
    }
}