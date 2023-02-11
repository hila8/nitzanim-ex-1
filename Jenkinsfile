pipeline {
    agent any
    stages {
        stage('Checkout Source Code') {
            steps {
                git 'https://github.com/hila8/nitzanim-ex-1.git'
            }
        }
        stage('Create Docker Image') {
            steps {
                sh 'docker build -t myimage .'
            }
        }
        stage('Push Docker Image') {
            steps {
                sh 'docker push myimage'
            }
        }
    }
}

