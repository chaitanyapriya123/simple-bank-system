pipeline {
  agent any
  stages {
    stage('code checkout') {
      steps {
        git(url: 'https://github.com/chaitanyapriya123/simple-bank-system.git', branch: 'master')
        echo 'code checkout done'
      }
    }
    stage('installing dependencies') {
        steps {

        sh 'npm i'
        echo 'Dependencies installed'
      }

    }
    stage('run') {
      steps {
        sh 'curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash'
        sh 'nvm install 14.17.2'
        echo 'installed latest version '
        sh 'npm start'

        echo 'successfully run'
      }

    }
  }
}
