pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            sh 'printenv'
            sh 'echo \'hello, world\''
          }
        }
        stage('Compile') {
          steps {
            sh 'echo \'compiling\''
          }
        }
      }
    }
    stage('Test') {
      steps {
        sh 'echo \'Testing\''
      }
    }
  }
  environment {
    DISABLE_AUTH = 'true'
  }
}