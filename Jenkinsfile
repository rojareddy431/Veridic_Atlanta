pipeline {
	agent any

	stages {
		stage('Checkout') {
			steps {
				sh 'git clone https://github.com/VeridicSolutionsOrg/Veridic_Atlanta.git'
				sh 'cd Veridic_Atlanta/'
				sh 'git checkout shasiteja'
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
