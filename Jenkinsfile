pipeline {
  agent any
  stages {
    stage('Git Checkout') {
      steps {
        echo 'Cloning github repository'
        git url: 'https://github.com/akshaymohana-btc/React-Native-CI-CD-Demo'
      }
    }
    stage('Install npm dependencies') {
      steps {
        echo 'INstalling dependencies...'
        npm install
      }
    }
  }
}
