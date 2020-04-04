pipeline {
    agent {
        none
    }
    stages {
        stage('docker test') {
            agent {
                docker {
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
