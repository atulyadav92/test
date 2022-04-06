pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                    echo "HELLO"
		    ls
            }
        }
        stage('Deploy') {
            steps {
                sh '''
			#nc -vz localhost 3306
		'''
            }
        }
    }
}

