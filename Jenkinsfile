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
                sh 'ps aux'
            }
        }
        stage('Unit test'){
            when {false}
        }
        stage('Deplyment'){
            when {false}
        }
    }
}