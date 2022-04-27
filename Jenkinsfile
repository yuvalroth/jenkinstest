pipeline {
//     agent { docker { image 'python:3.10.1-alpine' } }
    agent none
    stages {
    stage ('build all') {
    parallel {
                stage('build fe'){
                agent { docker { image 'python:3.10.1-alpine' } }

                    steps {
                        sh 'python --version'
                            sh 'echo "FE"'
                            sh 'sleep 10'
                          }
                    }
                stage('build integration')
                {
                agent { docker { image 'alpine' } }
                    steps {

                            sh 'echo "Integration"'
                            sh 'sleep 20'
                           }
                }
                stage('build backend')
                {
                agent { docker { image 'node' } }
                    steps {
                        sh 'node --version'
                        sh 'echo "Backend"'
                        sh 'sleep 15'
                         }
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
