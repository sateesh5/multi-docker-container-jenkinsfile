pipeline {
    agent none 
    stages {
        stage('Build') {
            agent {
                docker { image 'maven:3.9.9-eclipse-temurin-21-alpine'}

            }
            steps {
                script {
                    sh 'mvn --version'
                }
            }
        }
        stage ('Test') {
            agent {
                docker { image 'node:22.14.0-alpine3.21'}
            }
            steps {
                script {
                    sh 'node --version'
                }
            }
        }
    }
}
