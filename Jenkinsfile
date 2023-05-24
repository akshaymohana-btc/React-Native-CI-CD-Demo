pipeline {
  agent any
  stages {
    stage('Git Checkout') {
      echo 'Cloning github repository'
      git 'https://github.com/akshaymohana-btc/React-Native-CI-CD-Demo'
    }
    stage('Install npm dependencies') {
      steps {
        echo 'INstalling dependencies...'
      }
    }
  }
}
