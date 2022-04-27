pipeline {
    agent { docker { image 'python:3.10.1-alpine' } }
    stages {
    stage ('build all')
    {
                stage('build fe')
                    {
                    steps {
                        sh 'python --version'
                            sh 'echo "FE"'
                            sh 'sleep 10'
                          }
                    }
                stage('build integration')
                {
                    steps {
                            sh 'python --version'
                            sh 'echo "Integration"'
                            sh 'sleep 20'
                           }
                }
                stage('build backend')
                {
                    steps {
                        sh 'python --version'
                        sh 'echo "Backend"'
                        sh 'sleep 15'
                         }
                }
           }
        }
        post {
        always {
            sh 'echo "Run at the end"'
        }
    }
}
