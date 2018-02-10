pipeline {
  agent any
  stages {
    stage('echo') {
      agent {
        node {
          label 'ec2linux'
        }
        
      }
      steps {
        sh 'echo hostname'
      }
    }
  }
}