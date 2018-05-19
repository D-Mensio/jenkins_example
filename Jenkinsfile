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
          steps {
            echo 'ccc'
          }
        }
      }
    }
    stage('Test') {
      agent any
      steps {
        timestamps()
      }
    }
  }
}