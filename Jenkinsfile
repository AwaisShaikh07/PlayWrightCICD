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
                sh 'docker exec -it -u 0 66ecc04f3ce290939a521df79d99252512bd51a1ac7bf4f431ba6dbfc6f28608 /PlayWrightCICD'
                sh 'pytest -v'
            }
    }
}
}