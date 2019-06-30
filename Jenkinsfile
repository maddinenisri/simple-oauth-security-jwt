@Library('devops-lib@master') _
pipeline {
    agent any
    checkout scm
    def WORKSPACE = pwd()
    ciPipeline {
        WORKDIR = "${WORKSPACE}"
        METADATA = "src/main/resources/application.yaml"
    }
}