pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Compile the C++ file
                sh 'g++ main.cpp -o output'
                // Build identifier
                build 'PES1UG22AM908-1'
            }
        }

        stage('Test') {
            steps {
                // Run the compiled program
                sh './output'
            }
        }

        stage('Deploy') {
            steps {
                // Simulated deployment
                echo 'Deployment Successful'
            }
        }
    }

    post {
        failure {
            // Display message if the pipeline fails
            echo 'Pipeline failed'
        }
    }
}
