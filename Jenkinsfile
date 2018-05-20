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
        script {
          sh './gradlew check'

          junit 'build/reports/**/*.xml'
        }

      }
    }
  }
}