@Library('piper-lib-os') _

node() {
    stage('setup') {
        deleteDir()
        checkout scm
        setupCommonPipelineEnvironment script: this
    }
    stage('CloudPlatformSteps'){
        fioriOnCloudPlatformPipeline script:this
    }
}
