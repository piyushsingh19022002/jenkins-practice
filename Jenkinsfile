pipeline {
    agent any
    environment {
        IMAGE_NAME = "docker-jenkins:latest"
    }
    
    stages {
        stage('Checkout Code')
        steps {
            git 'https://github.com/piyushsingh19022002/jenkins-practice.git'
        }
        stage('Build Docker Image')
        steps {
            bat 'docker build -t %IMAGE_NAME% .'
        }
        stage('Show Docker Images')
        steps {
            bat 'docker images'
        }
    }
}