pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout your code from GitHub
                git branch: 'main', url: 'https://github.com/AnnaReddybandi/devops-demo2.git'
            }
        }

        stage('Build') {
            steps {
                echo 'No build required for static HTML/CSS, skipping...'
            }
        }

        stage('Test') {
            steps {
                echo 'Optional: Add HTML/CSS validation steps here'
            }
        }

        stage('Package') {
            steps {
                echo 'Packaging HTML/CSS files...'
                // Archive your HTML/CSS files as artifacts
                archiveArtifacts artifacts: '**/*', fingerprint: true
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploy stage - optionally copy files to server or hosting platform'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
