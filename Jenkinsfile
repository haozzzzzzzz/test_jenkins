pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'printenv'
        sh 'echo \'hello, world\''
      }
    }
  }
  environment {
    DISABLE_AUTH = 'true'
  }
}