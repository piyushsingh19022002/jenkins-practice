pipeline {
    agent any
    environment {
        IMAGE_NAME = "docker-jenkins:latest"
    }
    
    stages {
        stage('Checkout Code'){
             steps {
                git 'https://github.com/piyushsingh19022002/jenkins-practice.git'
            }
        }
       
        stage('Build Docker Image'){
            steps {
                sh 'docker build -t %IMAGE_NAME% .'
            }
        }
        
        stage('Show Docker Images'){
            steps {
                sh 'docker images'
            }
        }
        
    }
}