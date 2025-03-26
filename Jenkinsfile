pipeline {
    agent {
        docker {
            image 'node:20.19-alpine3.20'
        }
    }
    stages {
        stage('build') {
            steps {
                sh 'node --version'
            }
        }
        stage('test') {
            steps {
                sh 'npm test'
            }
        }
        stage('sonar') {
            steps {
                sh 'sonar-scanner'
            }
        }
        stage('deploy') {
            steps {
                sh 'npm run deploy'
            }
        }
    }
}