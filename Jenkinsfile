pipeline {
    agent any
    stages {
        stage('initial') {
            steps {
                sh 'ls -alh /'
                sh 'echo "Done!"'
                sh 'ls -a ~'
            }
        }
    }
    post {
      success {
        echo 'Goooooood:)'
      }
      failure {
        echo 'Oh, noooooo!'
      }
    }
}
