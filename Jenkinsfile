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

        stage('Test') {
            steps {
                sh 'echo test'
            }
        }

        stage('Delivery for development') {
            when {
                branch 'development'
            }
            steps {
                echo 'Delivery for development'
            }
        }

        stage('Delivery for production') {
            when {
                branch 'production'
            }
            steps {
                echo 'Delivery for production'
            }
        }
      }
    }
  }
  environment {
    DISABLE_AUTH = 'true'
  }
}