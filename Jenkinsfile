pipeline {
    agent any

    environment {
        DOCKER_IMAGE = "node-api"
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/<username>/node-api.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                sh 'echo "No tests yet"'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t $DOCKER_IMAGE .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 3000:3000 $DOCKER_IMAGE'
            }
        }
    }
}
