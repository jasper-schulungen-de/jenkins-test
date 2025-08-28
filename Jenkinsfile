/* Requires the Docker Pipeline plugin */
pipeline {
    agent none
    node {
        environment {
            dockerHome = tool 'jenkins-biosdb-docker'
            PATH = "${dockerHome}/bin:${PATH}"
        }
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
