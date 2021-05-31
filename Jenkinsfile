pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'cd lambda || pip3 install -t . || zip lambda_function.zip lambda_function.py'
            }
        }
    }
}

