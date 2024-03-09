pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                build 'PES1UG21CS566-1'
                sh 'g++ main.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                sh './output'
            }
        }
        stage('Deploy') {
            steps {
                printf("hello")
                echo 'deploy'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
