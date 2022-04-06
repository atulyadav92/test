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
		        ls
			#nc -vz localhost 3306
		'''
            }
        }
    }
}

