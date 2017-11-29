pipeline {
	agent any

	stages {
		stage('Checkout') {
			steps {
				git 'https://github.com/VeridicSolutionsOrg/Veridic_Atlanta.git'
			}
		}
		stage('Build') {
			steps {
				withmaven(maven:'maven_3_5_2') {
					sh 'mvn clean compile'
				}
			}
		}
		stage('Deploy') {
			steps {
				withmaven(maven: 'maven_3_5_2') {
					sh 'mvn deploy'
				}
			}
		}
	}
}
