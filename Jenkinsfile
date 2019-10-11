pipeline {
  agent any
  stages {
    stage('Build ubuntu') {
      agent {
        docker {
          image 'ubuntu'
          args '-u 0'
        }

      }
      steps {
        sh 'echo ${ENV}'
        sh 'apt update'
        sh 'apt install gcc make libpcap-dev'
        sh './configure'
        sh 'make'
      }
    }
  }
}