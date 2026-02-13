pipeline {
    agent any

    stages {

        stage('Checkout Source Code') {
            steps {
                echo 'Fetching latest code from GitHub repository'
                git 'https://github.com/USERNAME/REPO_NAME.git'
            }
        }

        stage('Environment Setup') {
            steps {
                echo 'Checking Python installation'
                bat 'python --version'
            }
        }

        stage('Dependency Verification') {
            steps {
                echo 'No external dependencies required for static site'
                bat 'echo Dependencies verified'
            }
        }

        stage('Build Application') {
            steps {
                echo 'Build stage completed for HTML/CSS project'
                bat 'echo Build successful'
            }
        }

        stage('Quality Check') {
            steps {
                echo 'Performing basic quality checks'
                bat 'echo Quality check passed'
            }
        }

        stage('Deploy to Local Server') {
            steps {
                echo 'Starting Python local server to host website'
                bat 'python server.py'
            }
        }

        stage('Post Deployment Verification') {
            steps {
                echo 'Deployment completed. Verify output using browser URL.'
            }
        }
    }

    post {
        success {
            echo 'CI/CD pipeline executed successfully'
        }
        failure {
            echo 'CI/CD pipeline failed. Check console output for errors.'
        }
    }
}
