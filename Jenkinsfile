pipeline {
  agent { label : master}
  git url : https://github.com/yoch24/YoTestRepo.git
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
        agent { label: 'master'}
        bat 'D:/Repository/src/Build/test.bat'

      }
    }
  }
}
