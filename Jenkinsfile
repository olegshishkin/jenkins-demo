pipeline {
    agent {
        label 'myDocker'
    }
    stages {
        stage('docker test') {
            agent {
                docker {
                    label 'myDocker'
                    image 'maven:latest'
                }
            }
            steps {
                sh 'docker --version'
            }
        }
        stage('build') {
            steps {
                sh 'mvn --version'
            }
        }
    }
}
