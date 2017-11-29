#!/usr/bin/env groovy
pipeline {
    agent any

    stages {
        stage('Build') { 
            steps { 
              echo "first step"
            }
        }
        stage('Test'){
            steps {
               echo "second step" 
            }
        }
        stage('Deploy') {
            steps {
                echo "third step"
            }
        }
    }
}
