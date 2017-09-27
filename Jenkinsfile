pipeline {

    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'msbuild JenkinsTest.sln'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
                sh 'ssh jenkins@76.89.239.141 -p 8022 mkdir -p /home/jenkins-test'
                sh 'scp -P 8022 -r /var/lib/jenkins/workspace/JenkinsTest jenkins@76.89.239.141:/home/jenkins0test'
            }
        }
    }
}
