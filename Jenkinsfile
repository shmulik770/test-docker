#!/usr/bin/env groovy
pipeline {
     agent {
         docker { image 'python:3.8-slim' }
     }

        stages {
        stage('Run Tests') {
            parallel {
                stage('parallel 1') {
                    steps {
                        sh 'pytest'
                    }
                }
                stage('parallel 2') {
                    steps {
                        echo "parallel 2"
                    }
                }
            }
        }
    }
}