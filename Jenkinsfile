pipeline {
  agent {
    node {
      label 'ecs-linux'
    }
    
  }
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