pipeline {
  agent none
  stages {
    stage('Build') {
      steps {
        echo 'Build Done..!!'
      }
    }
    stage('PostBuild') {
      parallel {
        stage('PostBuild') {
          steps {
            bat 'D:\\Repository\\src\\Build\\test.bat'
          }
        }
        stage('Test461') {
          steps {
            bat 'G:\\workdir\\buildconfig\\test.bat'
          }
        }
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploy Done..!!'
      }
    }
  }
}