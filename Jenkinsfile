@Library('devops-lib@master') _

node {
    WORKSPACE = pwd()

    ciPipeline{
        WORKDIR = "${WORKSPACE}"
        METADATA = "src/main/resources/application.yaml"
    }
}
