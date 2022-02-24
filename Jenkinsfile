pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                    echo "HELLO"
            }
        }
        stage('Deploy') {
            steps {
                sh '''
			nc -vz localhost 3306 #/usr/local/bin/aws lambda --region ${region} update-function-code --function-name Test01 --zip-file fileb://lambda_function${BUILD_NUMBER}.zip
		'''
            }
        }
    }
}

