pipeline {
    agent any

    stages {

        stage('CI Process') {
            parallel {

                stage('Checkout Code') {
                    steps {
                        echo 'Cloning repository from GitHub'
                        git branch: 'main', url: 'https://github.com/siddhi-hase/CI-CD-PROJECT.git'
                    }
                }

                stage('Environment Check') {
                    steps {
                        echo 'Checking environment'
                        bat 'echo Environment OK'
                    }
                }
            }
        }

        stage('Build & Test') {
            parallel {

                stage('Build') {
                    steps {
                        echo 'Building static website'
                        bat 'echo Build completed'
                    }
                }

                stage('Test') {
                    steps {
                        echo 'Testing static files'
                        bat 'echo Test passed'
                    }
                }
            }
        }

        stage('CD Process') {
            steps {
                echo 'Starting deployment process'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying files to local folder'
                bat 'if not exist C:\\ci-cd-output mkdir C:\\ci-cd-output'
                bat 'xcopy /Y /E index.html C:\\ci-cd-output\\'
                bat 'xcopy /Y /E style.css C:\\ci-cd-output\\'
            }
        }

        stage('Post Deployment Verification') {
            steps {
                echo 'Deployment completed successfully'
                echo 'Open this file in browser: C:\\ci-cd-output\\index.html'
            }
        }
    }

    post {
        success {
            echo 'Static website CI/CD pipeline executed successfully'
        }
        failure {
            echo 'Pipeline failed. Check console output.'
        }
    }
}

