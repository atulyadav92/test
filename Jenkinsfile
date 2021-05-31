pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh '''
			cd lambda
			pip3 install requests -t .
			zip lambda_function.zip lambda_function.py
            		echo ${region}
		'''
            }
        }
        stage('Deploy') {
            steps {
                sh '''
			aws lambda --region ${region} update-function-code --function-name Test01 --zip-file fileb://lambda.zip
		'''
            }
        }
    }
}

