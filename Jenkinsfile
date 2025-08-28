/* Requires the Docker Pipeline plugin */
pipeline {
    agent { docker { image 'maven:3.9.11-eclipse-temurin-21-alpine' } }
    tools { docker jenkins-biosdb-docker }
    stages {
        stage('build') {
            steps {
                sh 'mvn --version'
            }
        }
    }
}
