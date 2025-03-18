pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ main/hello.cpp -o main/PES1UG22CS494'
            }
        }
        stage('Test') {
            steps {
                sh './main/PES1UG22CS494'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying Application...'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
