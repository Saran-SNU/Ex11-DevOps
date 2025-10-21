pipeline {
    agent any
    environment {
        DOCKER_IMAGE = "node-api"
    }
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Saran-SNU/Ex11-DevOps.git'
            }
        }
        stage('Install Dependencies') {
            steps {
                bat 'npm install'
            }
        }
        stage('Test') {
            steps {
                bat 'echo No tests yet'
            }
        }
        stage('Build Docker Image') {
            steps {
                bat 'docker build -t %DOCKER_IMAGE% .'
            }
        }
        stage('Run Container') {
            steps {
                bat 'docker run -d -p 3000:3000 %DOCKER_IMAGE%'
            }
        }
    }
}
