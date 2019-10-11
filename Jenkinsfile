pipeline {
  agent any
  stages {
    stage('Build alpine') {
      agent {
        docker {
          image 'alpine'
        }

      }
      steps {
        sh 'pwd; ls -l;'
        sh './configure'
      }
    }
  }
}