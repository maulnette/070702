@Library('piper-lib-os') _

node() {
    stage('setup') {
        checkout scm
        setupCommonPipelineEnvironment script: this
    }
    stage('CloudPlatformSteps'){
        fioriOnCloudPlatformPipeline script:this
    }
}
