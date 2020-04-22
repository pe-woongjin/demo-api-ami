pipeline {
  agent any
  stages {
    stage('Pre-Process') {
      steps {
        echo 'configure variables'
      }
    }

    stage('Build') {
      steps {
        echo 'packer build and deploy ami to aws'
        sh '''packer --version


cd packer/build-awslinux2

pwd


packer build demo-api-prod-ami.json'''
      }
    }

    stage('Post-Process') {
      steps {
        echo 'Completing Pipeline'
      }
    }

  }
}