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
          agent {
            node {
              label 'ecslinux'
            }
            
          }
          steps {
            sh 'hostname'
            sleep 50
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