pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Install') {
            steps {
                sh 'npm install1'
            }
        }

        stage('Test') {
            steps {
                sh 'npm test1'
            }
        }

        stage('Start') {
            when {
                branch 'main'
            }
            steps {
                sh 'npm start'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully.'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}