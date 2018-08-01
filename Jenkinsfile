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
            node(label 'TEST_461v0') {
              customWorkspace 'D:\\Repository\\YoTestRepo\\src\\build'
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
