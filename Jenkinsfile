pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World from customer_repo'
            }
		}
		stage('Checkout code') {
			steps {
			   ws("/var/jenkins_home/w1") {
				  checkout scm
			   }
			}
		}
		stage('recompose docker container') {
			steps {
			    ws("/var/jenkins_home/w1") {
				     sh('./build.sh')
				}
			}
		}
    }
}
