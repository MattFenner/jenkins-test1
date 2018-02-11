pipeline {
  agent {
    node {
      label 'ecslinux'
    }
    
  }
  stages {
    stage('info') {
      parallel {
        stage('hostname 1') {
          agent any
          steps {
            timeout(time: 5, unit: 'MINUTES') {
              sh 'hostname'
              sleep 50
            }
            
          }
        }
        stage('hostname2') {
          steps {
            timeout(time: 2, unit: 'MINUTES') {
              sh 'hostname'
            }
            
          }
        }
        stage('hostname 3') {
          steps {
            timeout(time: 1, unit: 'MINUTES') {
              sh 'hostname'
            }
            
          }
        }
      }
    }
  }
}