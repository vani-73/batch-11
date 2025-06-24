pipeline {
    agent any
    stages {
        stage('Release Preparation') {
            steps {
                echo 'Preparing for release build...'
            }
        }
        stage('Build') {
            steps {
                echo 'Building the release version...'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploying release build...'
                // In real-world: deploy to production or staging environment
            }
        }
    }
    post {
        success {
            echo 'Release pipeline completed successfully.'
        }
        failure {
            echo 'Release pipeline failed.'
        }
    }
}
