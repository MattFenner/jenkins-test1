pipeline {
  agent any
  stages {
    stage('info') {
      parallel {
        stage('hostname 1') {
          agent {
            node {
              label 'ecslinux'
            }
            
          }
          steps {
            sh 'hostname'
            sleep 50
            timeout(time: 5, unit: 'MINUTES') {
              sh 'hostname'
              sleep 50
            }
            
          }
        }
        stage('hostname2') {
          agent {
            node {
              label 'ecslinux'
            }
            
          }
          steps {
            sh 'hostname'
            writeFile(file: 'test.txt', text: 'test')
            sleep 5
            archiveArtifacts '.'
          }
        }
        stage('hostname 3') {
          agent {
            node {
              label 'ecslinux'
            }
            
          }
          steps {
            sh 'hostname'
            input 'continue?'
          }
        }
      }
    }
  }
}