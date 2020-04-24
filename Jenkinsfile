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
        echo 'Discovery ami images'
        sh aws ec2 describe-images --owners self --filters "Name=name,Values=demo-api-ami*" > discovery.log
        sh echo discovery.log
      }
    }

  }
}