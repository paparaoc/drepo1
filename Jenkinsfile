pipeline {
    agent {
  label 'node1'
}
	
	tools {
  git 'Default'
}

    stages {
        stage('Pull From Git') {
            steps {
                git branch: 'main', credentialsId: 'd98fd9f9-af42-4c21-98ae-0e1ce30f54f0', url: 'https://github.com/paparaoc/drepo1'
            }
        }
        stage('Docker build') {
            steps {
                
                sh 'sudo chmod 666 /var/run/docker.sock'
                
				sh '''sudo docker build -t paparaoc/jenkinsrepo1:latest .
'''
            }
        }
    }
}
