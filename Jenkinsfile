pipeline {
    agent {
        label 'docker'
    }
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
        stage('build') {
            steps {
                sh 'mvn --version'
            }
        }
    }
}
