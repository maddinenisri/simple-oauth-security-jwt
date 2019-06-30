@Library('devops-lib@master') _
pipeline {
    environment {
        WORKSPACE = pwd()
    }
    agent any
    stages {
        stage("Init") {
            steps {
                checkout scm
            }
        }

        stage("build") {
            steps {
                ciPipeline WORKDIR: "${WORKSPACE}",  METADATA: "src/main/resources/application.yaml"
            }
        }
    }
}