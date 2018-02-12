pipeline {
  agent any
  stages {
    stage('checkout') {
      parallel {
        stage('6.5-Build') {
          steps {
            sh 'test'
          }
        }
        stage('6.0 Build') {
          steps {
            sh 'echo checkout'
          }
        }
      }
    }
    stage('6.5 Deploy') {
      parallel {
        stage('6.5 Deploy') {
          steps {
            sh 'echo 6.5 Deploy'
          }
        }
        stage('6.0 Deploy') {
          steps {
            sh 'echo 6.0 Deploy'
          }
        }
      }
    }
  }
}