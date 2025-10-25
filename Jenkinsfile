pipeline {
    agent any

    stages {
        stage('Checkout code') {
            steps {
                git branch: 'main', url: 'https://github.com/CecoIvanow/SeleniumIde.git'
            }
        }

        stage('Install dependencies') {
            steps {
                bat 'dotnet build' //no manual dotnet restore as per specifications
            }
        }
        stage('Test') {
            steps {
                bat 'dotnet test'
            }
        }
    }
}