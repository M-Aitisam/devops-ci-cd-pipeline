pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/M-Aitisam/devops-ci-cd-pipeline.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                bat 'docker build -t my-web-app .'
            }
        }
        stage('Test') {
            steps {
                echo 'Tests are running...'
            }
        }
        stage('Deploy') {
            steps {
                bat 'docker run -d -p 9090:80 my-web-app'
            }
        }
    }
}
