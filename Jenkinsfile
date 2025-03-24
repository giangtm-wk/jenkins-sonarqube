pipeline {
    agent { docker { image 'node:20.19-alpine3.20' } }
    stages {
        stage('build') {
            steps {
                sh 'node --version'
            }
        }
    }
}