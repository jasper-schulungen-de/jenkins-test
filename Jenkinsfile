/* Requires the Docker Pipeline plugin */
pipeline {
    environment {
        dockerHome = tool 'jenkins-biosdb-docker'
        PATH = "${dockerHome}/bin:${PATH}"
    }
    stages {
        stage('build') {
            agent { docker { image 'maven:3.9.11-eclipse-temurin-21-alpine' } }
            steps {
                sh 'mvn --version'
            }
        }
    }
}
