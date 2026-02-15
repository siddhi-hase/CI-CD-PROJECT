pipeline {
    agent any

    stages {

        stage('CI - Phase 1') {
            parallel {
                stage('Checkout') {
                    steps {
                        echo 'Code fetched from GitHub'
                    }
                }
                stage('Environment Test') {
                    steps {
                        echo 'Environment verified'
                    }
                }
            }
        }
        stage('CI - Phase 2') {
            parallel {
                stage('Build') {
                    steps {
                        echo 'Build completed'
                    }
                }
                stage('Test') {
                    steps {
                        echo 'Tests passed'
                    }
                }
            }
        }

        stage('CD - Phase') {
            parallel {
                stage('Deploy') {
                    steps {
                        echo 'Deployment done'
                    }
                }
                stage('Post Deployment Verification') {
                    steps {
                        echo 'Post deployment verification done'
                    }
                }
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
