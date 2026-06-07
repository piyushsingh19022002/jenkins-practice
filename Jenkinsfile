pipeline {
    agent any
    environment {
        IMAGE_NAME = "docker-jenkins:latest"
    }
    
    stages {
        // Tip: Aap is pure 'Checkout Code' stage ko ab delete bhi kar sakte hain
        stage('Checkout Code'){
             steps {
                git branch: 'main', url: 'https://github.com/piyushsingh19022002/jenkins-practice.git'
            }
        }
       
        stage('Build Docker Image'){
            steps {
                // 🛠️ docker ke pehle poora path (/usr/local/bin/) likh diya
                sh "docker build -t ${IMAGE_NAME} ."
            }
        }
        
        stage('Show Docker Images'){
            steps {
                // 🛠️ Yahan bhi full path de diya
                sh 'docker images'
            }
        }
    }
}