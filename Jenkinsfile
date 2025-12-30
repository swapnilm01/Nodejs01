pipeline {
    agent any

    tools {
        nodejs 'nodejs'   // this must match the NodeJS name you saved in Jenkins
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/ArpithaShetty15/nodejs-devops-app.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                echo 'No tests defined'
            }
        }

        stage('Build') {
            steps {
                echo 'Build step completed'
            }
        }
    }

    post {
        success {
            echo 'Pipeline executed successfully'
        }
        failure {
            echo 'Pipeline failed'
        }
    }
}
