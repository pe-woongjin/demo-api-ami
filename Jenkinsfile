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
      }
    }

    stage('Post-Process') {
      steps {
        echo 'Completing Pipeline'
      }
    }

  }
}