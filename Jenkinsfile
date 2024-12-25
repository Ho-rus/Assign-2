pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat 'dotnet build ./WcfServiceLibrary1/WcfServiceLibrary1.sln'
            }
        }
        stage('Test') {
            steps {
                bat 'dotnet test'
            }
        }
        stage('Docker Build') {
            steps {
                bat 'docker-compose build'
            }
        }
        stage('Deploy') {
            steps {
                bat 'docker-compose up -d'
            }
        }
    }
}
