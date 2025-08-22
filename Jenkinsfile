pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/krishnadevi10/exp3.git'
            }
        }

        stage('Build') {
            steps {
                sh 'echo Building the project...'
                // Replace with actual build command, e.g. sh 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                sh 'echo Running tests...'
                // Replace with actual test command
            }
        }

        stage('Deploy') {
            steps {
                sh 'echo Deploying the application...'
                // Replace with actual deploy commands
            }
        }
    }
}
