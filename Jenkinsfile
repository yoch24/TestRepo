pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            bat(returnStatus: true, returnStdout: true, script: 'test.bat')
          }
        }
        stage('') {
          steps {
            sh 'test.sh'
          }
        }
      }
    }
  }
}