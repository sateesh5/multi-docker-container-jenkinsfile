pipeline {
    agent none 
    stages {
        stage('Build') {
            agent {
                docker { image 'maven:3.9.9-eclipse-temurin-21-alpine'}

            }
            steps {
                script {
                    sh 'mvn clean package'
                }
            }
        }
        stage ('Test') {
            agent {
                docker { image 'maven:3.9.9-eclipse-temurin-21-alpine'}
            }
            steps {
                script {
                    sh 'mvn test'
                }
            }
        }
    }
}
