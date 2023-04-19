pipeline {
    agent any

    stages {
        stage('Git Checkout Project Directory') {
            steps {
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'Git_New', url: 'https://github.com/aryandvn/BackUp.git']])
            }
        }
        stage('Trigger Build of UseCase Job') {
            steps {
                build 'UseCase'
            }
        }
    }
}
