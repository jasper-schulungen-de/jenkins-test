/* Requires the Docker Pipeline plugin */
pipeline {
    agent { docker { image 'maven:3.9.11-eclipse-temurin-21-alpine' } }
    tools { dockerTool jenkins-biosdb-docker }
    environment { PATH = "${dockertool}/bin:${PATH}" }
    stages {
        stage('build') {
            steps {
                sh 'mvn --version'
            }
        }
    }
}
