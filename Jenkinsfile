pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat 'dotnet build "F:/Code/Assign 2/WcfServiceLibrary1/WcfServiceLibrary1/WcfServiceLibrary1.sln"'
            }
        }
        stage('Test') {
            steps {
                bat 'dotnet test "F:/Code/Assign 2/WcfServiceLibrary1/WcfServiceLibrary1/WcfServiceLibrary1.sln"'
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
