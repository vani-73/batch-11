pipeline {
    agent any
    stages {
        stage('Release Preparation') {
            steps {
                sh 'mvn compile'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean install'
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
