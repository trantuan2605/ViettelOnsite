pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                dir("rikkei-operation-api") {
                    bat 'mvn clean install'
                }
            }
        }
        stage('Test') {
            steps {
                dir("rikkei-operation-api") {
                    bat 'mvn test'
                }
            }
        }
        stage('Deploy') {
            steps {
                dir("rikkei-operation-api") {
                    bat 'docker-compose up -d --build'
                }
            }
        }
    }
}