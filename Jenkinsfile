pipeline {
    agent any
    stages {
        stage('Test') {
            steps {
                //sh 'echo "Test Fail!"; exit 1'
                sh "echo count is " + getCount()
                sh 'echo "Test Pass!"'
            }
        }
        stage('UAT') {
            steps {
                //sh 'echo "UAT Fail!"; exit 1'
                sh 'echo "UAT Pass!"; exit 0'
            }
        }
    }
    post {
        always {
            echo 'This will always run'
        }
        success {
            echo 'This will run only if successful'
        }
        failure {
            echo 'This will run only if failed'
        }
        unstable {
            echo 'This will run only if the run was marked as unstable'
        }
        changed {
            echo 'This will run only if the state of the Pipeline has changed'
            echo 'For example, if the Pipeline was previously failing but is now successful'
        }
    }
}

@NonCPS
def int getCount()
{
    retrun 5
}
