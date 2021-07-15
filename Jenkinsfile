@Library('piper-lib-os') _

node(){
  stage('Prepare')   {
      deleteDir()
      checkout scm
      setupCommonPipelineEnvironment script:this
  }

  stage('Build')   {
      mtaBuild script:this
  }

  stage('Deploy')   {
      agent {
          docker {
              image ppiper/cf-cli:latest
          }
      }
      cloudFoundryDeploy script:this, deployTool:'mtaDeployPlugin'
  }
  }