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
            readFile 'D:\\Repository\\src\\Build\\test.bat'
          }
        }
        stage('Test') {
          steps {
            readTrusted 'D:\\Repository\\src\\Build\\temp.pl'
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