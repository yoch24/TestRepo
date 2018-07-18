pipeline {
  agent none
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            bat(returnStatus: true, returnStdout: true, script: 'test.bat')
          }
        }
        stage('test') {
          steps {
            sh 'test.sh'
          }
        }
      }
    }
  }
}
