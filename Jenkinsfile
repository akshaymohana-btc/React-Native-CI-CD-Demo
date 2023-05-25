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
        script {
          // requires SonarQube Scanner 2.8+
          scannerHome = tool 'Jenkins SonarQube Scanner'
        }
        withSonarQubeEnv(installationName: 'Jenkins SonarQube Scanner') {
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
