pipeline {
    agent any

    stages {
        stage('Setup Environment') {
            steps {
                // Ensure Python3 is available in the Jenkins container
                sh 'apt-get update && apt-get install -y python3'
            }
        }
        stage('Test') {
            steps {
                // Run our Python unit tests
                sh 'python3 -m unittest test_app.py'
            }
        }
        stage('Deploy') {
            steps {
                echo 'All tests passed successfully on Jenkins!'
                echo 'Deploying application to production... 🚀'
            }
        }
    }
}