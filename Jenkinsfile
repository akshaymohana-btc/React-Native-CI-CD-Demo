pipeline {
    agent any

    stages {
        stage('Git Checkout') {
            steps {
                git url: 'git@github.com:akshaymohana-btc/React-Native-CI-CD.git'
            }
        }
//         stage('SonarQube Scan') {
//             steps {
//                 withSonarQubeEnv('Jenkins SonarQube Scanner') {
//                     bat "${scannerHome}/bin/sonar-scanner"
//                 }
//             }
//         }
//         stage('SonarQube Quality Gate') {
//             steps {
//                 timeout(time: 2, unit: 'MINUTES') {
//                     waitForQualityGate abortPipeline: true
//                 }
//             }
//         }
    }
}
