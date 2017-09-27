pipeline {

    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'msbuild JenkinsTest.sln'
            }
        }
    }
}
