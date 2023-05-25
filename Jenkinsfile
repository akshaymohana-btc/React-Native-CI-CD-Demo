pipeline {
  agent any
  tools {
    nodejs "node"
  }
  stages {
    stage('Git Checkout') {
      steps {
        echo 'Cloning github repository'
        git branch: 'develop', url: 'https://github.com/akshaymohana-btc/React-Native-CI-CD-Demo'
      }
    }
    stage('Install npm dependencies') {
      steps {
        echo 'Installing dependencies...'
        bat 'npm install'
      }
    }
  }
}
