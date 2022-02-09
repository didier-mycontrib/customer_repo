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
				checkout scm
			}
		}
    }
}
