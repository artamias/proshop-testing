pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'testing', url: 'https://github.com/artamias/proshop-testing.git'
            }
        }

        stage('Build') {
            steps {
                sh 'docker compose build'
            }
        }

        stage('Deploy') {
            steps {
                sh 'docker compose up -d'
            }
        }
    }
}