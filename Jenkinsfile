pipeline {
    agent any

    stages {
        stage('NPM install') {
            steps {
               bat 'npm install'
            }
        }

        stage('NPM audit') {
            steps {
               bat 'npm audit'
            }
        }
        
        stage('Run integration tests') {
            steps {
               bat 'npm test'
            }
        }
    }
}
