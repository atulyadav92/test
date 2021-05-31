pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'zip lambda_function.zip lambda_function.py'
            }
        }
    }
}

