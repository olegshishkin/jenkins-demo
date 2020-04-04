pipeline {
    agent {docker {image 'maven:latest'}}
    stages {
        stage('initialize') {
            def dockerHome = tool 'myDocker'
            env.PATH = "${dockerHome}/bin:${env.PATH}"
        }
        stage('build') {
            steps {
                sh 'mvn --version'
            }
        }
    }
}
