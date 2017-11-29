pipeline {
	agent any

	stages {
		stage('Checkout') {
			steps {
				echo 'checkout'
			}
		}
		stage('Build') {
			steps {
				withMaven(maven:'maven_3_0_5') {
					sh 'mvn clean compile'
				}
			}
		}
		stage('Deploy') {
			steps {
				echo 'deploy'
			}
		}
	}
}
