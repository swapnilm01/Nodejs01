pipeline {
    agent any

    tools {
        nodejs 'nodejs-ci-cd'
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

        stage('Deploy') {
            steps {
                sh '''
                pm2 stop nodejs-app || true
                pm2 delete nodejs-app || true
                pm2 start npm --name nodejs-app -- start
                pm2 save
                '''
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
