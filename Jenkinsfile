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
        sh 'npm run'

        echo 'successfully run'
      }

    }
  }
}
