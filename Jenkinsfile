pipeline {
    agent {
        docker {
            image 'python:latest'
        }
    }

    stages {
        stage('Compile') {
            steps {
                sh 'python3 -m compileall subtractor.py'
            }
        }

        stage('Run') {
            steps {
                sh 'python3 subtractor.py 13 5'
            }
        }

        stage('Unit test') {
            steps {
                sh 'python3 -m unittest subtractor.py'
            }
        }
    }
}
