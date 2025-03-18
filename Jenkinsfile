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
                sh './main/nonexistentfile' // Invalid file to trigger failure
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
