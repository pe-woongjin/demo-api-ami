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
        sh 'ls'
        dir(path: 'packer/build-awslinux2') {
          sh '/opt/packer/packer build ./demo-api-ami.json'
        }

      }
    }

    stage('Post-Process') {
      steps {
        echo 'Completing Pipeline'
      }
    }

  }
}