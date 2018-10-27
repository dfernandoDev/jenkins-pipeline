pipeline {
    agent { docker { image 'maven:3.3.3' } }
    currentBuild.result = 'SUCCESS'
    stages {
        stage('build') {
            steps {
                sh 'mvn --version'
            }
        }
    }
}
