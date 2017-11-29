pipeline {
	agent any

	stages {
		stage('Checkout') {
			steps {
				git clone 'https://github.com/VeridicSolutionsOrg/Veridic_Atlanta.git'
				cd Veridic_Atlanta/
				git checkout shasiteja
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
				withMaven(maven: 'maven_3_0_5') {
					sh 'mvn deploy'
				}
			}
		}
	}
}
