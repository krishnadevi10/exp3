pipeline {
    agent any

    environment {
        // Define any environment variables here
        APP_NAME = "MyApp"
    }

    stages {

        stage('Checkout') {
            steps {
                echo 'Checking out source code...'
                // Example Git checkout
                git url: 'https://github.com/your-repo/your-project.git', branch: 'main'
            }
        }

        stage('Build') {
            steps {
                echo 'Building the application...'
                // Example: Use Maven
                sh 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                echo 'Running unit tests...'
                // Example: Run tests
                sh 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                // Example deploy command
                sh 'scp target/${APP_NAME}.jar user@server:/opt/app/'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
