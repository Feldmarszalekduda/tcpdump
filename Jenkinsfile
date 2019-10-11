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
        sh 'env'
        sh 'apt list --instaled'
        sh 'apt update'
        sh 'apt install -y gcc make libpcap-dev'
        sh './configure'
        sh 'make'
      }
    }
  }
}