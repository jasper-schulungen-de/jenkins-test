/* Requires the Docker Pipeline plugin */
pipeline {
    agent none
    stages {
        stage('build') {
            agent { docker { image 'maven:3.9.11-eclipse-temurin-21-alpine' } }
            steps {
                dockerHome = tool 'jenkins-biosdb-docker'
                PATH = "${dockerHome}/bin:${PATH}"
                sh 'mvn --version'
            }
        }
    }
}
