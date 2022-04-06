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
			echo ${GIT_BRANCH}
			#nc -vz localhost 3306
		'''
            }
        }
    }
}
