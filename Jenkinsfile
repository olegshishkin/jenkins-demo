pipeline {
    agent {
        label 'docker'
    }
    agent {docker {image 'maven:latest'}}
    stages {
        stage('docker test') {
            agent {
                docker {
                    label 'docker'
                    image 'maven:latest'
                }
            }
            steps {
                sh 'docker --version'
            }
        }
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
