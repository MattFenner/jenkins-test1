pipeline {
  agent any
  stages {
    stage('echo') {
      agent {
        node {
          label 'ecs-linux-test1'
        }
        
      }
      steps {
        sh 'echo \'Hello World\''
      }
    }
  }
}