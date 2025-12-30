pipeline {
    agent any

    tools {
        nodejs 'nodejs-ci-cd'   // this must match the NodeJS name you saved in Jenkins
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/swapnilm01/Nodejs01.git'
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
