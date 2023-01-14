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
        sh 'curl -sL https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.0/install.sh -o install_nvm.sh'

        sh 'bash install_nvm.sh'

         sh 'export NVM_DIR="$HOME/.nvm'

  [ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm

  [ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"  # This loads nvm bash_completion'

  sh 'source ~/.bash_profile'

  sh 'command -v nvm'
        sh 'nvm install 14.17.2'
        echo 'installed latest version '
        sh 'npm start'

        echo 'successfully run'
      }

    }
  }
}
