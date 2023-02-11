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
                sh 'docker build -t hila8/myimage:tagname .' //myimage- name of the continer , tagname- the num of the version
            }
        }
        stage('Push Docker Image') {
            steps {
                sh 'docker login -u hila8 -p Nithilatavdi8'
                sh 'docker push hila8/myimage:tagname'
            }
        }
         stage('Run Docker Container') {
            steps {
                sh 'docker run -p 5000:5000 hila8/myimage:tagname'
            }
        }  
    }
}

