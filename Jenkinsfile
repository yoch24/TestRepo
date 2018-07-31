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
        node(label 'TEST_461v0') {
           stage('Test461') {
              steps {
                dir(path: 'D:\\Repository\\YoTestRepo\\src\\build') {
                  bat 'test.bat'
                }
              }
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
