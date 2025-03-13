pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                build 'PES1UG22CS555-1'
                sh 'g++ new.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                sh './output'
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
