pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
		retry(3) {
                    sh 'echo "hello, world"; exit 1'
                }
            }
        }
    }
}
