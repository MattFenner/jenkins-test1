pipeline {
  agent any
  stages {
    stage('1') {
      agent { docker 'alpine' }
      steps {
        lsb_release -a
      }
    }
  }
}