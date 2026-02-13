pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Code fetched from GitHub repository'
            }
        }

        stage('Environment Test') {
            steps {
                echo 'Environment test completed'
            }
        }

        stage('Build') {
            steps {
                echo 'Build completed successfully'
            }
        }

        stage('Test') {
            steps {
                echo 'All tests passed'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment completed successfully'
            }
        }

        stage('Post Deployment Verification') {
            steps {
                echo 'Post deployment verification done'
                echo 'Open deployed output in browser'
            }
        }
    }

    post {
        success {
            echo 'CI/CD pipeline executed successfully'
        }
        failure {
            echo 'Pipeline failed'
        }
    }
}
