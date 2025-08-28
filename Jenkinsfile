/* Requires the Docker Pipeline plugin */
pipeline {
    agent { docker { image 'maven:3.9.11-eclipse-temurin-21-alpine' } }
    environment {
        dockerHome = tool 'jenkins-biosdb-docker'
        PATH = "${dockerHome}/bin:${PATH}"
    }
    stages {
        stage('build') {
            steps {
                sh 'mvn --version'
            }
        }
    }
}
