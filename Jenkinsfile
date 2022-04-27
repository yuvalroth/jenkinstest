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
                agent {
                        label "linux"
                    }
                    steps {
                            sh 'python --version'
                            sh 'echo "Integration"'
                            sh 'sleep 20'
                           }
                }
                stage('build backend')
                {
                agent {
                        label "linux"
                    }
                    steps {
                        sh 'python --version'
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
