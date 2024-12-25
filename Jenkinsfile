pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat 'dotnet build ./MyApiProject/MyApiProject.sln'
                bat 'dotnet build ./GRPC/GRPC.sln'
            }
        }
        stage('Test') {
            steps {
                // Specify each solution or test project file explicitly
                bat 'dotnet test ./MyApiProject/MyApiProject.sln'
                bat 'dotnet test ./GRPC/GRPC.sln'
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
