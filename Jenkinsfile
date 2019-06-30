@Library('devops-lib@master') _
pipeline {
    agent any
    stages {
        stage("Init") {
            steps {
                checkout scm
            }
        }

        stage("build") {
            steps {
                def WORKSPACE = pwd()
                ciPipeline {
                    WORKDIR = "${WORKSPACE}"
                    METADATA = "src/main/resources/application.yaml"
                }
            }
        }
    }
}