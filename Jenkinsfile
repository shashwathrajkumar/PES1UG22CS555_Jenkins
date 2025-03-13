pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                build 'PES1UG22CS555-1'
                sh 'g++ main/new.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                sh './utput'
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }
    post {
        failure {
            error 'Pipeline failed'
        }
    }
}
