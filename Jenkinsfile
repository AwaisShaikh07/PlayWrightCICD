pipeline {
   agent { docker { image 'mcr.microsoft.com/playwright/python:v1.40.0-jammy' } }

    stages {
        stage('Checkout') {
            steps {
                checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/AwaisShaikh07/PlayWrightCICD.git']])
            }
        }
        stage('Build') {
            steps {
                git 'https://github.com/AwaisShaikh07/PlayWrightCICD.git'
            }
    }
    stage('Test') {
            steps {
                sh 'pytest -v'
            }
    }
}
}