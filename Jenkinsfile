pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('echo') {
          agent any
          steps {
            sh 'echo "aaa"'
            sh 'echo "bbb"'
          }
        }
        stage('message') {
          agent any
          steps {
            echo 'ccc'
          }
        }
      }
    }
    stage('Test') {
      agent any
      steps {
        timestamps() {
          echo 'any'
        }

      }
    }
  }
}