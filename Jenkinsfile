@Library('devops-lib@master') _
pipeline {
    agent any
    stages {
        stage("Init") {
            checkout scm
        }

        stage("build") {
            def WORKSPACE = pwd()
            ciPipeline {
                WORKDIR = "${WORKSPACE}"
                METADATA = "src/main/resources/application.yaml"
            }
        }
    }
}