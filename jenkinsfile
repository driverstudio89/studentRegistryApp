pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout code from a Git repository
                checkout scm
                git 'https://github.com/driverstudio89/studentRegistryApp'
            }
        }

        
        stage('Build') {
            steps {
                npm install
            }
        }
        
        stage('Test') {
            steps {
                npm test
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
