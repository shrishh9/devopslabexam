pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo "----- BUILD STAGE -----"
                echo "Building application from branch: ${env.GIT_BRANCH}"
                sh 'echo "Simulating build..."'
            }
        }

        stage('Test') {
            steps {
                echo "----- TEST STAGE -----"
                echo "Running tests for branch: ${env.GIT_BRANCH}"
                sh 'echo "All tests passed successfully!"'
            }
        }

        stage('Deploy') {
            steps {
                echo "----- DEPLOY STAGE -----"
                echo "Deploying application from branch: ${env.GIT_BRANCH}"
                sh 'echo "Deployment completed!"'
            }
        }
    }

    post {
        success {
            echo "✅ Pipeline executed successfully for ${env.GIT_BRANCH}"
        }
        failure {
            echo "❌ Pipeline failed for ${env.GIT_BRANCH}"
        }
    }
}
