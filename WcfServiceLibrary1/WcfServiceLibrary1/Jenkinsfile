pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'dotnet build "F:/Code/Assign 2/WcfServiceLibrary1/WcfServiceLibrary1/WcfServiceLibrary1.sln"'
            }
        }
        stage('Test') {
            steps {
                sh 'dotnet test "F:/Code/Assign 2/WcfServiceLibrary1/WcfServiceLibrary1/WcfServiceLibrary1.sln"'
            }
        }
        stage('Docker Build') {
            steps {
                sh 'docker-compose build'
            }
        }
        stage('Deploy') {
            steps {
                sh 'docker-compose up -d'
            }
        }
    }
}
