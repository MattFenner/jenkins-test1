pipeline {
  agent any
  stages {
    stage('info') {
      parallel {
        stage('hostname 1') {
          agent any
          steps {
            sh 'hostname'
          }
        }
        stage('hostname2') {
          steps {
            sh 'hostname'
          }
        }
        stage('hostname 3') {
          steps {
            sh 'hostname'
          }
        }
      }
    }
  }
}