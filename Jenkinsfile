pipeline {
  agent { label : master}
  stages {
    stage('Build') {
      steps {
        echo 'Build done..!!'
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
        bat 'D:/Repository/src/Build/test.bat'

      }
    }
  }
}
