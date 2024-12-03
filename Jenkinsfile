
pipeline {
    agent any
    tools {
        maven 'Maven3.8.5'  // Reference the Maven installation name from Global Tool Configuration
    }
    
    
    stages {
        stage('git checkout') {
            steps {
                git credentialsId: 'jenkinspassword', url: 'https://github.com/DeviSriKannan/CI_CD_Integration.git'
            }
        }
        stage('mvn build') {
            steps {
                sh 'mvn --version'  // Verifies the Maven version being used
                sh 'mvn clean install'  // Runs the Maven build
            }
        }
    
    }
}
