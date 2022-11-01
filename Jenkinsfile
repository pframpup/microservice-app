pipeline {
    agent any
    
    stages {
        stage('Test') {
            steps {
                sh 'docker --version'
            }
        }
        stage('Build'){
            steps {
                dir('auth-api'){
                    sh 'docker build -t dprampup/auth:v1 .'
                }    
            }
        }
        stage('Push dockerhub'){
            steps {
                withCredentials([usernamePassword(credentialsId: 'dockerhub-cred', passwordVariable: 'password', usernameVariable: 'username')]) {
                    sh 'docker login -u $username -p $password'
                    sh 'docker push dprampup/auth:v1' 
                }
            }
        }
        /*stage('Push'){
            when {false}
        }*/
    }
}