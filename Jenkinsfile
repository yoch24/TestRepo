pipeline {
  agent none
  stages {
    stage('Build') {
      steps {
        echo 'Build done..!!'
        sleep 10
      }
    }
    stage('Post Build') {
      parallel {
        stage('Test') {
          steps {
            echo 'Testing done..!!'
          }
        }
        stage('Deploy') {
          steps {
            echo 'Deployment done..!!'
          }
        }
      }
    }
    stage('Report') {
      steps {
        bat 'https://github.com/yoch24/YoTestRepo/blob/master/test.bat'
        node(label: 'master')
      }
    }
  }
}