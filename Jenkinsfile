pipeline {
    agent any
    stages {
        stage('Build') {
          steps {
            sh 'java --version'
          }
        }
        stage('Test') {
          steps {
            sh 'echo "Test step"'
          }
        }
        stage('Check') {
          steps {
            input "Is's alright?"
          }
        }
        stage('Deploy') {
          steps {
            sh 'echo "Deploy step"'
          }
        }
    }
    post {
      success {
        sh 'echo "Done"'
      }
      unstable {
        sh 'echo "Uups"'
      }
      failure {
        sh 'echo "Not done"'
      }
    }
}
