pipeline {
  agent any 
  tools {
    nodejs 'nodejs'
  }
  stages {
    stage('Clone Repo'){
      steps {
        git 'https://github.com/swapnilm01/Repo.git'
      }
    }
    stage('Test') {
      steps {
          sh 'npm test || true'
      }
    }
    stage('Deploy') {
      steps {
        sh '''
        npm install -g pm2
        npm2 stop nodeapp || true
        pm2 start npm --name
        nodeapp -- start
                       '''
      }
    }
  }
}
