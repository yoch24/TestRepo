pipeline {
  agent {
    node {
      label 'master'
    }

  }
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
        stage('Test') {
          steps {
            bat 'D:\\Repository\\src\\Build\\test.bat'
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