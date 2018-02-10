pipeline {
  agent any
  stages {
    stage('echo') {
      agent {
        node {
          label 'ecslinux'
        }
        
      }
      steps {
        sh 'echo \'Hello World\''
      }
    }
  }
}