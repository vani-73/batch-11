pipeline {
    agent any
    stages {

        stage('pull scm') {
            steps {
                git branch: 'main', url: 'https://github.com/PraveenKuber/Amazon-Jenkins.git'
            }
        }
         stage('validate') {
            steps {
                sh 'mvn validate'
            }
        }
        stage('compile') {
            steps {
                sh 'mvn compile'
            }
        }
         stage('test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('build') {
            steps {
                 sh 'mvn clean install'
            }
        }

        
    }

  post{

  success{
     echo 'Build success'
  }
    
  failure{
       echo 'Failure in the build'
   }

  }


}
