pipeline {
  agent any
  stages {
    stage('Build alpine') {
      agent {
        docker {
          image 'ubuntu'
        }

      }
      steps {
        sh 'echo ${ENV}'
        sh 'apt install gcc make libpcap-dev'
        sh './configure'
        sh 'make'
      }
    }
  }
}