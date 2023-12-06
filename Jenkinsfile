pipeline {
    agent any

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