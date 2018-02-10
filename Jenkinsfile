pipeline {
  agent any
  stages {
    stage('info') {
      parallel {
        stage('hostname 1') {
          agent any
          steps {
            sh 'hostname'
            sleep 5
          }
        }
        stage('hostname2') {
          steps {
            sh 'hostname'
            sleep 5
          }
        }
        stage('hostname 3') {
          steps {
            sh 'hostname'
            sleep 5
          }
        }
      }
    }
  }
}