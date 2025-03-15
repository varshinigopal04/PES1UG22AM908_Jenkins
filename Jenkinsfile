pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Intentional error: Incorrect compiler command (g++x does not exist)
                sh 'g++x main.cpp -o output'
                build 'YOUR_SRN-1'
            }
        }

        stage('Test') {
            steps {
                sh './output'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment Successful'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
