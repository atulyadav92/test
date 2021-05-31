pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh '''
			cd lambda
			echo ${BUILD_NUMBER}
			pip3 install requests -t .
			zip -r lambda_function${BUILD_NUMBER}.zip .
            		echo ${region}
			/usr/local/bin/aws cp lambda_function${BUILD_NUMBER}.zip s3://mygreenbucket/
			whoami
            		/usr/local/bin/aws s3 ls
		'''
            }
        }
        stage('Deploy') {
            steps {
                sh '''
			/usr/local/bin/aws lambda --region ${region} update-function-code --function-name Test01 --zip-file fileb://lambda_function${BUILD_NUMBER}.zip
		'''
            }
        }
    }
}

