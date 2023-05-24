pipeline {
    agent any

    stages {
        stage('Git Checkout') {
            steps {

            }
        }
    }

    stages {
        stage('SonarQube Scan') {
            steps {
                def scannerHome = tool 'Jenkins SonarQube Scanner';
                withSonarQubeEnv() {
                    bat "${scannerHome}/bin/sonar-scanner"
                }
            }
        }
        stage('SonarQube Quality Gate') {
            timeout(time: 2, unit: 'MINUTES') {
                waitForQualityGate abortPipeline: true
            }
        }
    }
}