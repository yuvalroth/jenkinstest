pipeline {
    agent { docker { image 'python:3.10.1-alpine' } }
    stages {
        stage('build fe') {
            steps {
                sh 'python --version'
                sh 'echo "FE"'

                  }
            }
        stage('build integration') {
            steps {
                sh 'python --version'
                sh 'echo "Integration"'

            }
                }
        stage('build backend') {
            steps {
                sh 'python --version'
                sh 'echo "Backend"'

            }


        }
    }
}