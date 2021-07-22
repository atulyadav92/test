
#hello world we are making changes to jenkinsfile



pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                    echo "HELLO"
		    echo "${BUILD_NUMBER}"
		    echo "${TAG}" 
            }
        }
        stage('Deploy') {
            steps {
                sh '''
			#/usr/local/bin/aws lambda --region ${region} update-function-code --function-name Test01 --zip-file fileb://lambda_function${BUILD_NUMBER}.zip
		'''
            }
        }
    }
}

