pipeline {
    agent {
		node {
			label 'my-defined-label'
			customWorkspace '/var/jenkins_home/w1'
		}
	}

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World from customer_repo'
            }
		}
		stage('Checkout code') {
			steps {
				checkout scm
			}
		}
		stage('recompose docker container') {
			steps {
				sh('./build.sh')
			}
		}
    }
}
