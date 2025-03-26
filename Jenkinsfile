pipeline {
    agent any

    environment {
        NODE_VERSION = '16'
    }

    stages {
        stage('Checkout') {
            steps {
                script {
                    // Log thay vì checkout thực tế
                    echo "Simulating checkout from repository"
                    sh 'pwd && ls -la'
                }
            }
        }

        stage('Install Dependencies') {
            steps {
                script {
                    // Log các bước cài đặt dependencies
                    echo "Running npm ci"
                    sh 'echo "Installing dependencies..."'
                    // Không chạy thực npm ci
                }
            }
        }

        stage('Lint') {
            steps {
                script {
                    // Giả lập quá trình lint
                    echo "Running eslint"
                    sh 'echo "Linting completed"'
                }
            }
        }

        stage('Unit Tests') {
            steps {
                script {
                    // Log thay vì chạy test
                    echo "Running unit tests"
                    sh '''
                        echo "Test suite starting..."
                        echo "✓ Test Case 1: Passed"
                        echo "✓ Test Case 2: Passed"
                        echo "✓ Test Case 3: Passed"
                        echo "Test suite completed successfully"
                    '''
                }
            }
        }

        stage('Build') {
            steps {
                script {
                    // Log quá trình build
                    echo "Building application"
                    sh '''
                        echo "Compiling source code..."
                        echo "Creating production build..."
                        echo "Build artifacts generated"
                    '''
                }
            }
        }

        stage('Docker Build') {
            steps {
                script {
                    // Log build Docker image
                    echo "Building Docker image"
                    sh '''
                        echo "Dockerfile analysis..."
                        echo "Building image: my-nodejs-app:${BUILD_NUMBER}"
                        echo "Docker image built successfully"
                    '''
                }
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully 🎉'
        }

        failure {
            echo 'Pipeline failed ❌'
        }
    }
}