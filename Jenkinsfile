pipeline {
    agent any
    environment {
        BUILD_TOOL = "Maven"   // Example variable for build tools
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building the project...'
                sh 'echo "Compiling code..."'
                sh 'mkdir -p build && echo "Build Complete" > build/output.txt'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing the project...'
                sh 'echo "Running tests..."'
                sh 'sleep 2 && echo "Tests passed successfully!"'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying the artifact...'
                sh 'echo "Deploying to target environment..."'
                sh 'cp build/output.txt /tmp/deployment_output.txt'
            }
        }
    }
    post {
        always {
            echo 'Pipeline execution completed!'
        }
    }
}
