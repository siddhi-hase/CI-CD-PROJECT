pipeline {
    agent any

    stages {

        stage('CI Stages') {
            parallel {
                stage('Checkout') {
                    steps { echo 'Checkout done' }
                }
                stage('Environment Test') {
                    steps { bat 'echo Environment OK' }
                }
            }
        }

        stage('Build & Test') {
            parallel {
                stage('Build') {
                    steps { bat 'echo Build OK' }
                }
                stage('Test') {
                    steps { bat 'echo Test OK' }
                }
            }
        }

        stage('CD Process') {
            stages {
                stage('Deploy') {
                    steps { bat 'echo Deploy OK' }
                }
                stage('Post Deployment Verification') {
                    steps { bat 'echo Post deploy OK' }
                }
            }
        }
    }
}