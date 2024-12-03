def mvnHome
pipeline {
    agent any
    
    
    stages {
        stage('git checkout') {
            steps {
                git credentialsId: 'jenkinspassword', url: 'https://github.com/DeviSriKannan/CI_CD_Integration.git'
            }
        }
        stage('git checkout') {
            steps {
                mvnHome=tool 'maven-3.2.5'
                sh "${mvnHome}/bin/mvn --version"
                sh "${mvnHome}/bin/mvn clean test surefire-report:report"
            }
        }
    
    }
}
