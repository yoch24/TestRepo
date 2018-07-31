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
        stage('Test461') {
          steps {
            node(label: 'TEST_461v0')
            echo 'On node machine'
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