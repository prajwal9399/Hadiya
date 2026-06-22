pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/prajwal9399/Hadiya.git'
            }
        }

        stage('Docker Compose Build') {
            steps {
                sh 'docker compose up -d --build'
            }
        }

    }
}
