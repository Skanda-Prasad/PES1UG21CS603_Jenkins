pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        script {
          // Assuming "PES1UG21CS603-1" is a Jenkins job name, you should trigger it instead of just calling build
          build "PES1UG21CS603-69"
          sh 'g++ newfile.cpp -o output'
        }
      }
    }
    stage('Test') {
      steps {
        script{
        sh './output'
        }
      }
    }
    stage('Deploy') {
      steps {
        echo 'deploy'
      }
    }
  }
  post {
    failure {
      echo 'Pipeline Failed'
    }
  }
}
