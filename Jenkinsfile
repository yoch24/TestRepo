pipeline
{
    agent none
    stages {
        stage('Build') { 
            steps {
                echo "Build done..!!"
            }
        }
        stage('Post Build') {
            parallel{
                stage('Test') { 
                    steps {
                        echo "Testing done..!!"
                    }
                }
                stage('Deploy') { 
                    steps {
                        echo "Deployment done..!!"
                    }
                }
            }
        }
    }
}
