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
			nc -vz localhost 3306
		'''
            }
        }
    }
}

