pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/prajwal9399/Hadiya.git'
            }
        }
        stage('Build Images') {
            steps {
                sh 'docker-compose build'
            }
        }
        stage('Stop Old Containers') {
            steps {
                sh 'docker-compose down || true'
            }
        }
        stage('Deploy') {
            steps {
                sh 'docker-compose up -d'
            }
        }
        stage('Verify') {
            steps {
                sh 'sleep 10 && docker ps'
            }
        }
    }
}
