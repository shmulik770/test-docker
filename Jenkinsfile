#!/usr/bin/env groovy
pipeline {
     agent {
         docker { image 'circleci/python:3.7' }
     }

        stages {
        stage('Run Tests') {
            parallel {
                stage('parallel 1') {
                    steps {
                        sh 'python --version'
                        // sh 'pytest'
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