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
			   ws("/conf-docker/w1") {
				  checkout scm
			   }
			}
		}
		stage('recompose docker container') {
			steps {
			    ws("/conf-docker/w1") {
				     sh('./build.sh')
				}
			}
		}
    }
}
