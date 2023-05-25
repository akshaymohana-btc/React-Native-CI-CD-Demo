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
    stage('Sonarqube Scanning'){
      steps {
        def scannerHome = tool 'Jenkins SonarQube Scanner';
        withSonarQubeEnv() {
          bat "${scannerHome}/bin/sonar-scanner"
        }
      }
    }
//     stage('Install npm dependencies') {
//       steps {
//         echo 'Installing dependencies...'
//         bat 'npm install'
//       }
//     }
  }
}
